# Welcome

#### This is a socket-based interactive api based on the [Socket.io](https://socket.io) library.



### Example client code 

{% tabs %}
{% tab title="JavaScript" %}
```javascript
import io from 'socket.io-client';

const FALLBACK_URL = 'wss://api-v4.zerion.io/';
const BASE_URL = process.env.API_URL || FALLBACK_URL;

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

const assetsSocket = {
  namespace: 'assets',
  socket: io(`${BASE_URL}assets`, {
    transports: ['websocket'],
    timeout: 60000,
    query: {
      api_token:
        process.env.ZERION_API_KEY_V4 ||
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

get(assetsSocket, {
  scope: ['info'],
  payload: {
    explore_section: 1,
    currency: 'usd',
    offset: 0,
    limit: 20,
  },
}).then(response => {
  console.log(response.payload.info);
});
```
{% endtab %}

{% tab title="Python" %}
```python
import asyncio
import socketio
URI = "wss://api-v4.zerion.io"
API_TOKEN = "Demo.ukEVQp6L5vfgxcz4sBke7XvS873GMYHy"
ORIGIN = "http://localhost:3000"
sio = socketio.AsyncClient()

@sio.event
async def connect():
  print("I'm connected!")

@sio.event
def connect_error():
  print("The connection failed!")

@sio.event
async def my_message(data):
    print('message received with ', data)
    await sio.emit('my response', {'response': 'my response'})

async def main():
    await sio.connect(f"{URI}/?api_token={API_TOKEN}", headers={"Origin": ORIGIN})
    await sio.wait()

if __name__ == '__main__':
    asyncio.run(main())

```
{% endtab %}
{% endtabs %}

## Overview

In order to connect, a valid `api_token` query parameter must be specified.All tokens are restricted by Origin and therefore a valid `HTTP_ORIGIN` header is expected.

```javascript
let io_options = {transports: ['websocket'], query: {api_token: 'YOUR API TOKEN'}};
socket = io('wss://api.zerion.io', io_options);
```

### Actions

There are three supported types of messages:

* `get` - requests data, returns a single response and does not emit continuous messages
* `subscribe` - returns a single response \(the same as `get`\) + creates a subscription
* `unsubscribe` - deletes the subscription

### Request

Each request has the following structure:

```text
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

```text
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

```text
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

## Handlers

#### AddressHandler \(`/address`\)

* **Payload**

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| addresses | list | \[\] |
| currency | [PriceCurrency]() | usd |
| charts\_type | str | d |
| charts\_max\_assets | int | 0 |
| charts\_min\_percentage | int | 100 |
| transactions\_limit | int | 50 |
| transactions\_offset | int | 0 |
| transactions\_search\_query | str | - |
| portfolio\_fields | [PortfolioFields]() | assets |
| asset\_codes | list | \[\] |

* **Messages**

| Scope | Result |
| :--- | :--- |
| info | [AddressInfo]() |
| assets | Dict\[str, [AddressAsset]()\] |
| portfolio | [Portfolio]() |
| transactions | List\[[Transaction]()\] |
| charts | Dict\[str, List\[Tuple\[int, float\]\]\] |
| deposits | List\[[Deposit]()\] |
| loans | List\[[Loan]()\] |
| locked-assets | List\[[LockedAsset]()\] |
| staked-assets | List\[[StakedAsset]()\] |

#### AssetsHandler \(`/assets`\)

* **Payload**

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| addresses | list | \[\] |
| asset\_code | str | - |
| asset\_codes | list | \[\] |
| currency | [PriceCurrency]() | usd |
| limit | int | 10000 |
| offset | int | 0 |
| explore\_section | str | - |
| order\_by | dict | {} |
| charts\_type | str | d |
| explore\_sections | list | \[\] |
| category\_id | str | - |
| explore\_sections\_aliases | list | \[\] |
| search\_query | str | - |
| tags\_group | str | all |

* **Messages**

| Scope | Result |
| :--- | :--- |
| prices | Dict\[str, [Asset]()\] |
| info | List\[[AssetInfo]()\] |
| full-info | Dict\[AssetFullInfo, [NoneType]()\] |
| explore-sections | List\[[ExploreSection]()\] |
| charts | Dict\[str, List\[Tuple\[int, float\]\]\] |
| tags | List\[[AssetTag]()\] |
| actions | List\[[AssetAction]()\] |
| stats | [AssetStats]() |
| list | List\[[AssetInfo]()\] |
| tokenlists | List\[[Tokenlist]()\] |
| categories | List\[[Category]()\] |

#### BlockLagHandler \(`/block_lag`\)

* **Payload**

| Field | Type | Default |
| :--- | :--- | :--- |


* **Messages**

| Scope | Result |
| :--- | :--- |
| block-lag | [BlockLag]() |

#### CompoundHandler \(`/compound`\)

* **Payload**

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| currency | [PriceCurrency]() | usd |

* **Messages**

| Scope | Result |
| :--- | :--- |
| info | [CompoundInfo]() |
| assets | List\[[CompoundAsset]()\] |
| actions | List\[[CompoundAction]()\] |
| deposits | List\[[CompoundDeposit]()\] |
| loans | List\[[CompoundLoan]()\] |

#### DyDxHandler \(`/dydx`\)

* **Payload**

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| currency | [PriceCurrency]() | usd |

* **Messages**

| Scope | Result |
| :--- | :--- |
| deposits | List\[[DyDxAccountBalance]()\] |
| loans | List\[[DyDxAccountBalance]()\] |

#### GasPriceHandler \(`/gas`\)

* **Payload**

| Field | Type | Default |
| :--- | :--- | :--- |


* **Messages**

| Scope | Result |
| :--- | :--- |
| price | [GasPriceInfo]() |

#### MakerHandler \(`/maker`\)

* **Payload**

| Field | Type | Default |
| :--- | :--- | :--- |
| cdp\_id | str | - |
| vault\_id | str | - |
| currency | [PriceCurrency]() | usd |

* **Messages**

| Scope | Result |
| :--- | :--- |
| cdp | [MakerCDP]() |
| vault | [MakerVault]() |
| cdp-actions | List\[[MakerCDPAction]()\] |
| vault-actions | List\[[MakerVaultAction]()\] |

## Models

#### AddressAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset]() |  |
| quantity | str |  |

#### AddressInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| address | str |  |
| type | str |  |
| proxies | str | yes |
| cdps | int | yes |
| vaults | int | yes |
| aggregated\_at | int | yes |

#### Asset

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset\_code | str |  |
| name | str |  |
| symbol | str |  |
| decimals | int |  |
| type | [AssetType]() |  |
| icon\_url | str | yes |
| price | [Price]() | yes |
| is\_displayable | bool |  |
| is\_verified | bool |  |

#### AssetAction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| transaction\_hash | str |  |
| type | [AssetActionType]() |  |
| value | float | yes |
| quantity | str |  |
| price | float | yes |
| datetime | int |  |
| asset | [Asset]() |  |
| status | [TransactionStatus]() |  |
| direction | [Direction]() |  |
| fee | [AssetActionFee]() | yes |

#### AssetActionAmount

| Name | Type | Optional |
| :--- | :--- | :--- |
| base | float |  |
| currency | float | yes |

#### AssetActionFee

| Name | Type | Optional |
| :--- | :--- | :--- |
| quantity | str |  |
| value | float |  |

#### AssetComponent

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset]() |  |
| quantity | float |  |
| share | float |  |
| allocation | float |  |

#### AssetDescription

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset\_code | str |  |
| full | str | yes |

#### AssetFullInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset]() |  |
| title | str |  |
| stats | [AssetFullInfoStats]() |  |
| components | str | yes |
| gradient\_color | str | yes |
| explore\_sections | int | yes |
| subtitle | str | yes |
| tagline | str | yes |
| market\_cap | float | yes |
| fully\_diluted\_valuation | float | yes |
| total\_supply | float | yes |
| circulating\_supply | float | yes |
| relative\_changes | str | yes |
| description | str | yes |
| relevant\_resources | [AssetRelevantResource]() | yes |
| tags | str | yes |
| is\_tradable | bool |  |

#### AssetFullInfoStats

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset\_code | str |  |
| year\_min | float | yes |
| year\_max | float | yes |
| volume\_24h | float | yes |

#### AssetInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset]() |  |
| title | str |  |
| gradient\_color | str | yes |
| explore\_sections | int | yes |
| subtitle | str | yes |
| tagline | str | yes |
| market\_cap | float | yes |
| total\_supply | float | yes |
| circulating\_supply | float | yes |
| relative\_changes | str | yes |
| tags | str | yes |

#### AssetRelevantResource

| Name | Type | Optional |
| :--- | :--- | :--- |
| name | str |  |
| url | str |  |
| displayable\_name | str | yes |

#### AssetStats

| Name | Type | Optional |
| :--- | :--- | :--- |
| total\_returned | float | yes |
| total\_returned\_net | float | yes |
| total\_returned\_change | float | yes |
| total\_fee\_spent | float | yes |
| avg\_buy\_price | float | yes |
| avg\_buy\_price\_net | float | yes |
| avg\_sell\_price | float | yes |
| avg\_sell\_price\_net | float | yes |

#### AssetTag

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |

#### BlockLag

| Name | Type | Optional |
| :--- | :--- | :--- |
| block\_lag | int | yes |

#### Category

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | int |  |
| title | str |  |
| tagline | str |  |
| alias | str |  |
| display\_type | [CategoryDisplayType]() |  |

#### CompoundAction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| type | [TransactionAction]() |  |
| transaction\_hash | str |  |
| status | [TransactionStatus]() |  |
| ctoken | str | yes |
| ctoken\_value | float | yes |
| underlying\_value | float | yes |
| datetime | datetime |  |

#### CompoundAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| underlying | [Asset]() |  |
| underlying\_eth\_price | float |  |
| asset | [Asset]() |  |
| borrow\_rate | float | yes |
| supply\_rate | float | yes |
| exchange\_rate | float | yes |

#### CompoundDeposit

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [CompoundAsset]() |  |
| deposited | float |  |
| earned\_interest | float |  |
| ctokens | int |  |

#### CompoundInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| loans | [CompoundLoan]() | yes |
| deposits | [CompoundDeposit]() | yes |
| total\_debt | float |  |
| total\_collateral | float |  |

#### CompoundLoan

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [CompoundAsset]() |  |
| borrowed | float |  |
| accrued\_interest | float |  |

#### Deposit

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset]() |  |
| deposited | float |  |
| value | float |  |
| supply\_rate | float | yes |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

#### DyDxAccountBalance

| Name | Type | Optional |
| :--- | :--- | :--- |
| owner | str |  |
| account\_number | str |  |
| normalized\_balance | float |  |
| balance | float |  |
| asset | [Asset]() |  |

#### ExploreSection

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | int |  |
| title | str |  |
| tagline | str |  |
| order | int |  |
| alias | str | yes |

#### GasPriceInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| rapid | int | yes |
| fast | int | yes |
| standard | int | yes |
| slow | int | yes |
| source | [GasPriceSource]() |  |
| datetime | datetime |  |

#### Loan

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset]() |  |
| borrowed | float |  |
| value | float |  |
| borrow\_rate | float | yes |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

#### LockedAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset]() |  |
| locked | float |  |
| value | float |  |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

#### MakerCDP

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | int |  |
| owner | str |  |
| debt | float |  |
| collateral | float |  |

#### MakerCDPAction

| Name | Type | Optional |
| :--- | :--- | :--- |
| type | str |  |
| transaction | str |  |
| timestamp | int |  |
| dai\_value | float | yes |
| eth\_value | float | yes |
| peth\_value | float | yes |
| owner | str | yes |
| new\_owner | str | yes |

#### MakerVault

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | int |  |
| owner | str |  |
| normalized\_debt | float |  |
| outstanding\_debt | float |  |
| total\_borrowed | float |  |
| total\_repaid | float |  |
| accrued\_interest | float |  |
| collateral | float |  |
| collateral\_type | str |  |

#### MakerVaultAction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| vault | int |  |
| type | [MakerDSSActionType]() |  |
| transaction\_hash | str |  |
| normalized\_debt\_change | float | yes |
| debt\_change | float | yes |
| collateral\_change | float | yes |
| owner | str | yes |
| new\_owner | str | yes |
| datetime | datetime |  |

#### Portfolio

| Name | Type | Optional |
| :--- | :--- | :--- |
| assets\_value | float |  |
| deposited\_value | float |  |
| borrowed\_value | float |  |
| locked\_value | float |  |
| staked\_value | float |  |
| total\_value | float |  |
| absolute\_change\_24h | float |  |
| relative\_change\_24h | float | yes |

#### Price

| Name | Type | Optional |
| :--- | :--- | :--- |
| value | float |  |
| relative\_change\_24h | float | yes |
| changed\_at | int |  |

#### PriceStat

| Name | Type | Optional |
| :--- | :--- | :--- |
| min | float |  |
| max | float |  |
| relative\_change | float |  |

#### StakedAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset]() |  |
| staked | float |  |
| value | float |  |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

#### Tokenlist

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| name | str |  |
| icon\_url | str |  |
| total\_tokens | int |  |
| has\_asset\_code | bool |  |

#### Transaction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| type | [RDBTransactionType]() |  |
| protocol | str |  |
| mined\_at | int |  |
| block\_number | int |  |
| status | [TransactionStatus]() |  |
| hash | str |  |
| direction | [Direction]() | yes |
| address\_from | str | yes |
| address\_to | str | yes |
| contract | str | yes |
| nonce | int | yes |
| changes | [TransactionChange]() | yes |
| fee | [TransactionFee]() | yes |
| meta | str | yes |

#### TransactionChange

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset]() |  |
| value | int |  |
| direction | [Direction]() |  |
| address\_from | str |  |
| address\_to | str |  |
| price | float | yes |

#### TransactionFee

| Name | Type | Optional |
| :--- | :--- | :--- |
| value | int |  |
| price | float |  |

## Structures

#### RDBTransactionType

* send
* receive
* trade
* authorize
* execution
* deployment
* cancel
* deposit
* withdraw
* borrow
* repay
* stake
* unstake
* claim

  **AssetType**

* aave
* aave-uniswap
* aave-v2
* alpha-homora
* badger-sett
* balancer
* bancor
* bitcoin
* cream
* curve
* compound
* dmm
* dodo
* enzyme
* ethereum
* fulcrum
* harvest-vault
* idle
* iearn-curve
* iearn-v2
* iearn-v3
* indexed
* keeperdao
* maker
* melon
* mooniswap
* mstable
* mushroom-vault
* nft
* one-inch
* pickle-jar
* piedao-pool
* pool-together
* realt
* snowswap
* stablecoin
* synthetix
* sushi
* swerve
* tokenset
* tokenset-v2
* trash
* uniswap
* uniswap-v2
* xsushi
* yearn-vault
* yearn-vault-v2
* None

  **GasPriceSource**

* gas-now
* eth-gas-station

  **TransactionStatus**

* confirmed
* failed
* pending

  **PriceCurrency**

* eth
* btc
* usd
* eur
* krw
* rub
* gbp
* aud
* cad
* inr
* jpy
* nzd
* try
* zar
* cny
* chf

  **CategoryDisplayType**

* short
* detailed

  **PortfolioFields**

* all
* assets

  **TransactionAction**

* Authorize
* Trade
* Deposit
* Withdraw
* Borrow
* Repay
* Liquidate
* Enable Borrowing
* Open CDP
* Close CDP
* Transfer CDP
* Migrate CDP
* Open Vault
* Close Vault
* Transfer Vault
* Migrate
* Create Exchange
* Add Liquidity
* Remove Liquidity
* Stake
* Unstake
* Claim Rewards
* Register ENS Domain
* Renew ENS Domain

  **MakerDSSActionType**

* open
* deposit
* withdraw
* borrow
* repay
* transfer
* liquidate

  **Direction**

* in
* out
* self

  **AssetActionType**

* buy
* sell
* send
* receive
* borrow
* deposit
* authorize
* withdraw
* repay
* stake
* unstake
* claim

