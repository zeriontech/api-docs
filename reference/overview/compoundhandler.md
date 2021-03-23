# CompoundHandler

## Payload

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| currency | [PriceCurrency](compoundhandler.md#PriceCurrency) | usd |

## Messages

| Scope | Result |
| :--- | :--- |
| info | [CompoundInfo](compoundhandler.md#CompoundInfo) |
| assets | List\[[CompoundAsset](compoundhandler.md#CompoundAsset)\] |
| actions | List\[[CompoundAction](compoundhandler.md#CompoundAction)\] |
| deposits | List\[[CompoundDeposit](compoundhandler.md#CompoundDeposit)\] |
| loans | List\[[CompoundLoan](compoundhandler.md#CompoundLoan)\] |

