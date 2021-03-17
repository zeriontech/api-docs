# MakerHandler

## Payload

| Field | Type | Default |
| :--- | :--- | :--- |
| cdp\_id | str | - |
| vault\_id | str | - |
| currency | [PriceCurrency](makerhandler.md#PriceCurrency) | usd |

## Messages

| Scope | Result |
| :--- | :--- |
| cdp | [MakerCDP](makerhandler.md#MakerCDP) |
| vault | [MakerVault](makerhandler.md#MakerVault) |
| cdp-actions | List\[[MakerCDPAction](makerhandler.md#MakerCDPAction)\] |
| vault-actions | List\[[MakerVaultAction](makerhandler.md#MakerVaultAction)\] |

