# Return Types

## AddressArbitrumAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [L2Asset](#l2asset) |  |
 | quantity | str |  |
## AddressAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [Asset](#asset) |  |
 | quantity | str |  |
## AddressAvalancheAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [L2Asset](#l2asset) |  |
 | quantity | str |  |
## AddressBSCAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [L2Asset](#l2asset) |  |
 | quantity | str |  |
## AddressFantomAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [L2Asset](#l2asset) |  |
 | quantity | str |  |
## AddressInfo
| Name | Type | Optional |
| ---  | ---  | -------- |
 | address | str |  |
 | type | str |  |
 | proxies | str | yes |
 | cdps | int | yes |
 | vaults | int | yes |
 | aggregated_at | int | yes |
## AddressL2Asset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [L2Asset](#l2asset) |  |
 | quantity | str |  |
## AddressNFT
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | asset | [NFTAsset](#nftasset) |  |
 | amount | str |  |
 | section | str |  |
 | section_tokens_count | int |  |
 | standard | str |  |
 | displayed_on_chart | bool |  |
 | value | float | yes |
## AddressOptimismAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [L2Asset](#l2asset) |  |
 | quantity | str |  |
## AddressPolygonAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [L2Asset](#l2asset) |  |
 | quantity | str |  |
## Asset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | asset_code | str |  |
 | name | str |  |
 | symbol | str |  |
 | decimals | int |  |
 | implementations | Mapping[str, [AssetImplementation](#assetimplementation)] |  |
 | type | AssetType |  |
 | icon_url | str | yes |
 | price | [Price](#price) | yes |
 | is_displayable | bool |  |
 | is_verified | bool |  |
## AssetImplementation
| Name | Type | Optional |
| ---  | ---  | -------- |
 | address | str | yes |
 | decimals | int |  |
## AssetAction
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | transaction_hash | str |  |
 | type | [AssetActionType](#assetactiontype) |  |
 | value | float | yes |
 | quantity | str |  |
 | price | float | yes |
 | datetime | int |  |
 | asset | [Asset](#asset) |  |
 | status | [TransactionStatus](#transactionstatus) |  |
 | direction | [Direction](#direction) |  |
 | fee | [AssetActionFee](#assetactionfee) | yes |
## AssetActionAmount
| Name | Type | Optional |
| ---  | ---  | -------- |
 | base | float |  |
 | currency | float | yes |
## AssetActionFee
| Name | Type | Optional |
| ---  | ---  | -------- |
 | quantity | str |  |
 | value | float |  |
## AssetComponent
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [Asset](#asset) |  |
 | quantity | float |  |
 | share | float |  |
 | allocation | float |  |
## AssetDescription
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset_code | str |  |
 | full | str | yes |
## AssetFullInfo
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [Asset](#asset) |  |
 | title | str |  |
 | stats | [AssetFullInfoStats](#assetfullinfostats) |  |
 | components | str | yes |
 | gradient_color | str | yes |
 | explore_sections | int | yes |
 | subtitle | str | yes |
 | tagline | str | yes |
 | market_cap | float | yes |
 | fully_diluted_valuation | float | yes |
 | total_supply | float | yes |
 | circulating_supply | float | yes |
 | relative_changes | str | yes |
 | description | str | yes |
 | relevant_resources | [AssetRelevantResource](#assetrelevantresource) | yes |
 | tags | str | yes |
 | is_tradable | bool |  |
## AssetFullInfoStats
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset_code | str |  |
 | year_min | float | yes |
 | year_max | float | yes |
 | volume_24h | float | yes |
## AssetInfo
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [Asset](#asset) |  |
 | title | str |  |
 | gradient_color | str | yes |
 | explore_sections | int | yes |
 | subtitle | str | yes |
 | tagline | str | yes |
 | market_cap | float | yes |
 | total_supply | float | yes |
 | circulating_supply | float | yes |
 | relative_changes | str | yes |
 | tags | str | yes |
## AssetRelevantResource
| Name | Type | Optional |
| ---  | ---  | -------- |
 | name | str |  |
 | url | str |  |
 | displayable_name | str | yes |
## AssetStats
| Name | Type | Optional |
| ---  | ---  | -------- |
 | total_returned | float | yes |
 | total_returned_net | float | yes |
 | total_returned_change | float | yes |
 | total_fee_spent | float | yes |
 | avg_buy_price | float | yes |
 | avg_buy_price_net | float | yes |
 | avg_sell_price | float | yes |
 | avg_sell_price_net | float | yes |
## AssetTag
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
## AssetType
| Name | Type | Optional |
| ---  | ---  | -------- |
## BlockLag
| Name | Type | Optional |
| ---  | ---  | -------- |
 | block_lag | int | yes |
## Category
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | title | str |  |
 | tagline | str |  |
 | order_by | str | yes |
 | display_type | [CategoryDisplayType](#categorydisplaytype) |  |
## CompoundAction
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | type | [TransactionAction](#transactionaction) |  |
 | transaction_hash | str |  |
 | status | [TransactionStatus](#transactionstatus) |  |
 | ctoken | str | yes |
 | ctoken_value | float | yes |
 | underlying_value | float | yes |
 | datetime | datetime |  |
## CompoundAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | underlying | [Asset](#asset) |  |
 | underlying_eth_price | float |  |
 | asset | [Asset](#asset) |  |
 | borrow_rate | float | yes |
 | supply_rate | float | yes |
 | exchange_rate | float | yes |
## CompoundDeposit
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [CompoundAsset](#compoundasset) |  |
 | deposited | float |  |
 | earned_interest | float |  |
 | ctokens | int |  |
## CompoundInfo
| Name | Type | Optional |
| ---  | ---  | -------- |
 | loans | [CompoundLoan](#compoundloan) | yes |
 | deposits | [CompoundDeposit](#compounddeposit) | yes |
 | total_debt | float |  |
 | total_collateral | float |  |
## CompoundLoan
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [CompoundAsset](#compoundasset) |  |
 | borrowed | float |  |
 | accrued_interest | float |  |
## Deposit
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | asset | [Asset](#asset) |  |
 | deposited | float |  |
 | value | float |  |
 | supply_rate | float | yes |
 | section | str |  |
 | protocol | str |  |
 | displayed_on_chart | bool |  |
## DyDxAccountBalance
| Name | Type | Optional |
| ---  | ---  | -------- |
 | owner | str |  |
 | account_number | str |  |
 | normalized_balance | float |  |
 | balance | float |  |
 | asset | [Asset](#asset) |  |
## ExploreSection
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | int |  |
 | title | str |  |
 | tagline | str |  |
 | order | int |  |
 | alias | str | yes |
## GasPriceInfo
| Name | Type | Optional |
| ---  | ---  | -------- |
 | rapid | int | yes |
 | fast | int | yes |
 | standard | int | yes |
 | slow | int | yes |
 | source | [GasPriceSource](#gaspricesource) |  |
 | datetime | datetime |  |
## L2Asset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset_code | str |  |
 | name | str |  |
 | symbol | str |  |
 | decimals | int |  |
 | icon_url | str | yes |
 | value | float | yes |
## LiquityTroveAction
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | trove | int |  |
 | type | str |  |
 | transaction_hash | str |  |
 | debt_change | float | yes |
 | collateral_change | float | yes |
 | datetime | datetime |  |
## Loan
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | asset | [Asset](#asset) |  |
 | borrowed | float |  |
 | value | float |  |
 | borrow_rate | float | yes |
 | section | str |  |
 | protocol | str |  |
 | displayed_on_chart | bool |  |
## LockedAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | asset | [Asset](#asset) |  |
 | locked | float |  |
 | value | float |  |
 | section | str |  |
 | protocol | str |  |
 | displayed_on_chart | bool |  |
## MakerCDP
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | int |  |
 | owner | str |  |
 | debt | float |  |
 | collateral | float |  |
## MakerCDPAction
| Name | Type | Optional |
| ---  | ---  | -------- |
 | type | str |  |
 | transaction | str |  |
 | timestamp | int |  |
 | dai_value | float | yes |
 | eth_value | float | yes |
 | peth_value | float | yes |
 | owner | str | yes |
 | new_owner | str | yes |
## MakerVault
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | int |  |
 | owner | str |  |
 | normalized_debt | float |  |
 | outstanding_debt | float |  |
 | total_borrowed | float |  |
 | total_repaid | float |  |
 | accrued_interest | float |  |
 | collateral | float |  |
 | collateral_type | str |  |
## MakerVaultAction
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | vault | int |  |
 | type | [MakerDSSActionType](#makerdssactiontype) |  |
 | transaction_hash | str |  |
 | normalized_debt_change | float | yes |
 | debt_change | float | yes |
 | collateral_change | float | yes |
 | owner | str | yes |
 | new_owner | str | yes |
 | datetime | datetime |  |
## NFTAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset_code | str |  |
 | symbol | str |  |
 | contract_address | str |  |
 | token_id | str |  |
 | interface | str |  |
 | preview | [NFTContent](#nftcontent) |  |
 | detail | [NFTContent](#nftcontent) |  |
 | name | str | yes |
 | type | AssetType |  |
 | tags | str | yes |
 | price | [Price](#price) | yes |
 | is_displayable | bool |  |
 | is_verified | bool |  |
## NFTAttribute
| Name | Type | Optional |
| ---  | ---  | -------- |
 | key | str |  |
 | value | str |  |
## NFTCollection
| Name | Type | Optional |
| ---  | ---  | -------- |
 | name | str |  |
 | description | str | yes |
 | icon_url | str | yes |
## NFTContent
| Name | Type | Optional |
| ---  | ---  | -------- |
 | url | str | yes |
## NFTInfo
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [NFTAsset](#nftasset) |  |
 | collection | [NFTCollection](#nftcollection) |  |
 | description | str | yes |
 | attributes | [NFTAttribute](#nftattribute) | yes |
 | relevant_urls | [NFTRelevantURL](#nftrelevanturl) | yes |
## NFTRelevantURL
| Name | Type | Optional |
| ---  | ---  | -------- |
 | name | str |  |
 | url | str |  |
## Portfolio
| Name | Type | Optional |
| ---  | ---  | -------- |
 | assets_value | float |  |
 | deposited_value | float |  |
 | borrowed_value | float |  |
 | locked_value | float |  |
 | staked_value | float |  |
 | arbitrum_assets_value | float |  |
 | bsc_assets_value | float |  |
 | polygon_assets_value | float |  |
 | optimism_assets_value | float |  |
 | total_value | float |  |
 | absolute_change_24h | float |  |
 | relative_change_24h | float | yes |
## PositionDetail
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset_code | str |  |
 | amount | int |  |
 | tokens_owed | int |  |
 | fee_growth | int |  |
## Price
| Name | Type | Optional |
| ---  | ---  | -------- |
 | value | float |  |
 | relative_change_24h | float | yes |
 | changed_at | int |  |
## PriceStat
| Name | Type | Optional |
| ---  | ---  | -------- |
 | min | float |  |
 | max | float |  |
 | relative_change | float |  |
## StakedAsset
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | asset | [Asset](#asset) |  |
 | staked | float |  |
 | value | float |  |
 | section | str |  |
 | protocol | str |  |
 | displayed_on_chart | bool |  |
## Tokenlist
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | name | str |  |
 | icon_url | str |  |
 | total_tokens | int |  |
 | has_asset_code | bool |  |
## Transaction
| Name | Type | Optional |
| ---  | ---  | -------- |
 | id | str |  |
 | type | [RDBTransactionType](#rdbtransactiontype) |  |
 | protocol | str |  |
 | mined_at | int |  |
 | block_number | int |  |
 | status | [TransactionStatus](#transactionstatus) |  |
 | hash | str |  |
 | direction | [Direction](#direction) | yes |
 | address_from | str | yes |
 | address_to | str | yes |
 | contract | str | yes |
 | nonce | int | yes |
 | changes | [TransactionChange](#transactionchange) | yes |
 | fee | [TransactionFee](#transactionfee) | yes |
 | meta | str | yes |
## TransactionChange
| Name | Type | Optional |
| ---  | ---  | -------- |
 | asset | [Asset](#asset) |  |
 | value | int |  |
 | direction | [Direction](#direction) |  |
 | address_from | str |  |
 | address_to | str |  |
 | price | float | yes |
## TransactionFee
| Name | Type | Optional |
| ---  | ---  | -------- |
 | value | int |  |
 | price | float |  |
