# Models

## AddressAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset](models.md#asset) |  |
| quantity | str |  |

## AddressBSCAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [CovalentAsset](models.md#CovalentAsset) |  |
| quantity | str |  |

## AddressInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| address | str |  |
| type | str |  |
| proxies | str | yes |
| cdps | int | yes |
| vaults | int | yes |
| aggregated\_at | int | yes |

## AddressPolygonAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [CovalentAsset](models.md#CovalentAsset) |  |
| quantity | str |  |

## Asset

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset\_code | str |  |
| name | str |  |
| symbol | str |  |
| decimals | int |  |
| type | [AssetType](models.md#AssetType) |  |
| icon\_url | str | yes |
| price | [Price](models.md#Price) | yes |
| is\_displayable | bool |  |
| is\_verified | bool |  |

## AssetAction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| transaction\_hash | str |  |
| type | [AssetActionType](models.md#AssetActionType) |  |
| value | float | yes |
| quantity | str |  |
| price | float | yes |
| datetime | int |  |
| asset | [Asset](models.md#Asset) |  |
| status | [TransactionStatus](models.md#TransactionStatus) |  |
| direction | [Direction](models.md#Direction) |  |
| fee | [AssetActionFee](models.md#AssetActionFee) | yes |

## AssetActionAmount

| Name | Type | Optional |
| :--- | :--- | :--- |
| base | float |  |
| currency | float | yes |

## AssetActionFee

| Name | Type | Optional |
| :--- | :--- | :--- |
| quantity | str |  |
| value | float |  |

## AssetComponent

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset](models.md#Asset) |  |
| quantity | float |  |
| share | float |  |
| allocation | float |  |

## AssetDescription

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset\_code | str |  |
| full | str | yes |

## AssetFullInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset](models.md#Asset) |  |
| title | str |  |
| stats | [AssetFullInfoStats](models.md#AssetFullInfoStats) |  |
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
| relevant\_resources | [AssetRelevantResource](models.md#AssetRelevantResource) | yes |
| tags | str | yes |
| is\_tradable | bool |  |

## AssetFullInfoStats

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset\_code | str |  |
| year\_min | float | yes |
| year\_max | float | yes |
| volume\_24h | float | yes |

## AssetInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset](models.md#Asset) |  |
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

## AssetRelevantResource

| Name | Type | Optional |
| :--- | :--- | :--- |
| name | str |  |
| url | str |  |
| displayable\_name | str | yes |

## AssetStats

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

## AssetTag

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |

## BlockLag

| Name | Type | Optional |
| :--- | :--- | :--- |
| block\_lag | int | yes |

## Category

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| title | str |  |
| tagline | str |  |
| order\_by | str | yes |
| display\_type | [CategoryDisplayType](models.md#CategoryDisplayType) |  |

## CompoundAction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| type | [TransactionAction](models.md#TransactionAction) |  |
| transaction\_hash | str |  |
| status | [TransactionStatus](models.md#TransactionStatus) |  |
| ctoken | str | yes |
| ctoken\_value | float | yes |
| underlying\_value | float | yes |
| datetime | datetime |  |

## CompoundAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| underlying | [Asset](models.md#Asset) |  |
| underlying\_eth\_price | float |  |
| asset | [Asset](models.md#Asset) |  |
| borrow\_rate | float | yes |
| supply\_rate | float | yes |
| exchange\_rate | float | yes |

## CompoundDeposit

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [CompoundAsset](models.md#CompoundAsset) |  |
| deposited | float |  |
| earned\_interest | float |  |
| ctokens | int |  |

## CompoundInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| loans | [CompoundLoan](models.md#CompoundLoan) | yes |
| deposits | [CompoundDeposit](models.md#CompoundDeposit) | yes |
| total\_debt | float |  |
| total\_collateral | float |  |

## CompoundLoan

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [CompoundAsset](models.md#CompoundAsset) |  |
| borrowed | float |  |
| accrued\_interest | float |  |

## CovalentAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset\_code | str |  |
| name | str |  |
| symbol | str |  |
| decimals | int |  |
| icon\_url | str | yes |
| value | float | yes |

## Deposit

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset](models.md#Asset) |  |
| deposited | float |  |
| value | float |  |
| supply\_rate | float | yes |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

## DyDxAccountBalance

| Name | Type | Optional |
| :--- | :--- | :--- |
| owner | str |  |
| account\_number | str |  |
| normalized\_balance | float |  |
| balance | float |  |
| asset | [Asset](models.md#Asset) |  |

## ExploreSection

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | int |  |
| title | str |  |
| tagline | str |  |
| order | int |  |
| alias | str | yes |

## GasPriceInfo

| Name | Type | Optional |
| :--- | :--- | :--- |
| rapid | int | yes |
| fast | int | yes |
| standard | int | yes |
| slow | int | yes |
| source | [GasPriceSource](models.md#GasPriceSource) |  |
| datetime | datetime |  |

## Loan

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset](models.md#Asset) |  |
| borrowed | float |  |
| value | float |  |
| borrow\_rate | float | yes |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

## LockedAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset](models.md#Asset) |  |
| locked | float |  |
| value | float |  |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

## MakerCDP

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | int |  |
| owner | str |  |
| debt | float |  |
| collateral | float |  |

## MakerCDPAction

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

## MakerVault

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

## MakerVaultAction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| vault | int |  |
| type | [MakerDSSActionType](models.md#MakerDSSActionType) |  |
| transaction\_hash | str |  |
| normalized\_debt\_change | float | yes |
| debt\_change | float | yes |
| collateral\_change | float | yes |
| owner | str | yes |
| new\_owner | str | yes |
| datetime | datetime |  |

## Portfolio

| Name | Type | Optional |
| :--- | :--- | :--- |
| assets\_value | float |  |
| deposited\_value | float |  |
| borrowed\_value | float |  |
| locked\_value | float |  |
| staked\_value | float |  |
| bsc\_assets\_value | float |  |
| polygon\_assets\_value | float |  |
| total\_value | float |  |
| absolute\_change\_24h | float |  |
| relative\_change\_24h | float | yes |

## Price

| Name | Type | Optional |
| :--- | :--- | :--- |
| value | float |  |
| relative\_change\_24h | float | yes |
| changed\_at | int |  |

## PriceStat

| Name | Type | Optional |
| :--- | :--- | :--- |
| min | float |  |
| max | float |  |
| relative\_change | float |  |

## StakedAsset

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| asset | [Asset](models.md#Asset) |  |
| staked | float |  |
| value | float |  |
| section | str |  |
| protocol | str |  |
| displayed\_on\_chart | bool |  |

## Tokenlist

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| name | str |  |
| icon\_url | str |  |
| total\_tokens | int |  |
| has\_asset\_code | bool |  |

## Transaction

| Name | Type | Optional |
| :--- | :--- | :--- |
| id | str |  |
| type | [RDBTransactionType](models.md#RDBTransactionType) |  |
| protocol | str |  |
| mined\_at | int |  |
| block\_number | int |  |
| status | [TransactionStatus](models.md#TransactionStatus) |  |
| hash | str |  |
| direction | [Direction](models.md#Direction) | yes |
| address\_from | str | yes |
| address\_to | str | yes |
| contract | str | yes |
| nonce | int | yes |
| changes | [TransactionChange](models.md#TransactionChange) | yes |
| fee | [TransactionFee](models.md#TransactionFee) | yes |
| meta | str | yes |

## TransactionChange

| Name | Type | Optional |
| :--- | :--- | :--- |
| asset | [Asset](models.md#Asset) |  |
| value | int |  |
| direction | [Direction](models.md#Direction) |  |
| address\_from | str |  |
| address\_to | str |  |
| price | float | yes |

## TransactionFee

| Name | Type | Optional |
| :--- | :--- | :--- |
| value | int |  |
| price | float |  |

