# AddressHandler

## Payload

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| addresses | list | \[\] |
| currency | [PriceCurrency](addresshandler.md#PriceCurrency) | usd |
| charts\_type | str | d |
| charts\_max\_assets | int | 0 |
| charts\_min\_percentage | int | 100 |
| transactions\_limit | int | 50 |
| transactions\_offset | int | 0 |
| transactions\_search\_query | str | - |
| portfolio\_fields | [PortfolioFields](addresshandler.md#PortfolioFields) | assets |
| asset\_codes | list | \[\] |

## Messages

| Scope | Result |
| :--- | :--- |
| info | [AddressInfo](addresshandler.md#AddressInfo) |
| assets | Dict\[str, [AddressAsset](addresshandler.md#AddressAsset)\] |
| portfolio | [Portfolio](addresshandler.md#Portfolio) |
| transactions | List\[[Transaction](addresshandler.md#Transaction)\] |
| charts | Dict\[str, List\[Tuple\[int, float\]\]\] |
| deposits | List\[[Deposit](addresshandler.md#Deposit)\] |
| loans | List\[[Loan](addresshandler.md#Loan)\] |
| locked-assets | List\[[LockedAsset](addresshandler.md#LockedAsset)\] |
| staked-assets | List\[[StakedAsset](addresshandler.md#StakedAsset)\] |
| bsc-assets | Dict\[str, [AddressBSCAsset](addresshandler.md#AddressBSCAsset)\] |
| polygon-assets | Dict\[str, [AddressPolygonAsset](addresshandler.md#AddressPolygonAsset)\] |

