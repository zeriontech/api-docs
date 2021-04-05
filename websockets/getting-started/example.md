---
description: Fetch user's on-chain portfolio
---

# Example

The following example connects to the Zerion Websocket API and fetches the portfolio of a given Ethereum address.

{% tabs %}
{% tab title="JavaScript" %}
#### 1. Copy and paste the example below to `quickstart.js`

```javascript
let io = require('socket.io-client')

const BASE_URL = 'wss://api-v4.zerion.io/';

function verify(request, response) {
  // each value in request payload must be found in response meta
  return Object.keys(request.payload).every(key => {
    const requestValue = request.payload[key];
    const responseMetaValue = response.meta[key];
    if (typeof requestValue === 'object') {
      return JSON.stringify(requestValue) === JSON.stringify(responseMetaValue);
    }
    return responseMetaValue === requestValue;
  });
}

const addressSocket = {
  namespace: 'address',
  socket: io(`${BASE_URL}address`, {
    transports: ['websocket'],
    timeout: 60000,
    query: {
      api_token:
        'Demo.ukEVQp6L5vfgxcz4sBke7XvS873GMYHy',
    },
  }),
};

function get(socketNamespace, requestBody) {
  return new Promise(resolve => {
    const { socket, namespace } = socketNamespace;
    function handleReceive(data) {
      if (verify(requestBody, data)) {
        unsubscribe();
        resolve(data);
      }
    }
    const model = requestBody.scope[0];
    function unsubscribe() {
      socket.off(`received ${namespace} ${model}`, handleReceive);
      socket.emit('unsubscribe', requestBody);
    }
    socket.emit('get', requestBody);
    socket.on(`received ${namespace} ${model}`, handleReceive);
  });
}

get(addressSocket, {
  scope: ['portfolio'],
  payload: {
      address: '0x7e5ce10826ee167de897d262fcc9976f609ecd2b',
      currency: 'usd',
      portfolio_fields: 'all'
  },
}).then(response => {
  console.log(response.payload.portfolio);
});

```

#### 2. Run it using `node`

```text
node quickstart.js
```
{% endtab %}

{% tab title="Python" %}
#### 1. Copy and paste the example below to `quickstart.py`  

```python
import asyncio
import socketio
URI = "wss://api-v4.zerion.io/"
API_TOKEN = "Demo.ukEVQp6L5vfgxcz4sBke7XvS873GMYHy"
ORIGIN = "http://localhost:3000"
sio = socketio.AsyncClient()

@sio.event
async def connect():
  print("Connected to the Zerion Websocket API!")

@sio.event(namespace='/address')
async def connect():
  print("address namespace!")
  await sio.emit('subscribe',
      {
          "scope": ["portfolio"],
          "payload": {
              "address": "0x7e5ce10826ee167de897d262fcc9976f609ecd2b",
              "currency": "usd",
              "portfolio_fields": "all"
              }
      }, namespace='/address')


@sio.event
def connect_error():
  print("The connection failed!")


async def main():
    await sio.connect(f"{URI}/?api_token={API_TOKEN}",
        headers={"Origin": ORIGIN},
        namespaces=['/address'],
        transports=['websocket'])

    await sio.wait()

if __name__ == '__main__':
    asyncio.run(main())

```

#### 2. Run it using `python`

```bash
python3 quickstart.py
```
{% endtab %}
{% endtabs %}



