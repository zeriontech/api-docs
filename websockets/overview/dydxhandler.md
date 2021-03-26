# DyDxHandler

## Payload

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| currency | [PriceCurrency](dydxhandler.md#PriceCurrency) | usd |

## Messages

| Scope | Result |
| :--- | :--- |
| deposits | List\[[DyDxAccountBalance](dydxhandler.md#DyDxAccountBalance)\] |
| loans | List\[[DyDxAccountBalance](dydxhandler.md#DyDxAccountBalance)\] |

