# Zerion Websocket API

#### This is a socket-based interactive api based on the [Socket.io](https://socket.io) library.
## Overview
In order to connect, a valid `api_token` query parameter must be specified.All tokens are restricted by Origin and therefore a valid `HTTP_ORIGIN` header is expected.
Feel free to get started with `http://localhost:3000` as an origin and a Demo Key: `Demo.ukEVQp6L5vfgxcz4sBke7XvS873GMYHy`. 
```javascript
let io_options = {transports: ['websocket'], query: {api_token: 'YOUR API TOKEN'}};
socket = io('wss://api.zerion.io', io_options);
```

### Actions

There are three supported types of messages:

 - `get` - requests data, returns a single response and does not emit continuous messages
 - `subscribe` - returns a single response (the same as `get`) + creates a subscription
 - `unsubscribe` - deletes the subscription


### Request

Each request has the following structure:

```
[
    "{action}",
    {
      "scope": ["scope1", "scope2"],
      "payload": {
          "parameter1": "value1",
          "parameter2": "value2"
      }
    }
]
```


### Response

```
[
    "received {namespace} {model}",
    {
       "meta": {
           "status": "ok",
           "request parameter1": "value1",
           "request parameter2": "value2"
       },
       "payload": {
           "{scope}": "__result__"
       }
    }
]
```


### Change

```
[
    "changed|appended|removed {namespace} {model}",
    {
       "meta": {
           "subscription parameter1": "value1",
           "subscription parameter2": "value2"
       },
       "payload": {
           // changed model
       }
    }
]
```

