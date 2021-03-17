# AssetsHandler

## Payload

| Field | Type | Default |
| :--- | :--- | :--- |
| address | str | - |
| addresses | list | \[\] |
| asset\_code | str | - |
| asset\_codes | list | \[\] |
| currency | [PriceCurrency](assetshandler.md#PriceCurrency) | usd |
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

## Messages

| Scope | Result |
| :--- | :--- |
| prices | Dict\[str, [Asset](assetshandler.md#Asset)\] |
| info | List\[[AssetInfo](assetshandler.md#AssetInfo)\] |
| full-info | Optional\[zerion\_api.entities.socketio.AssetFullInfo\] |
| explore-sections | List\[[ExploreSection](assetshandler.md#ExploreSection)\] |
| charts | Dict\[str, List\[Tuple\[int, float\]\]\] |
| tags | List\[[AssetTag](assetshandler.md#AssetTag)\] |
| actions | List\[[AssetAction](assetshandler.md#AssetAction)\] |
| stats | [AssetStats](assetshandler.md#AssetStats) |
| list | List\[[AssetInfo](assetshandler.md#AssetInfo)\] |
| tokenlists | List\[[Tokenlist](assetshandler.md#Tokenlist)\] |
| categories | List\[[Category](assetshandler.md#Category)\] |

