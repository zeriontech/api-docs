# (/address)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} info {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["info"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address info",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "info": AddressInfo
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} portfolio {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["portfolio"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="nft_price_type" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address portfolio",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "portfolio": Portfolio
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} portfolio-decomposition {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["portfolio-decomposition"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="nft_price_type" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address portfolio-decomposition",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "portfolio-decomposition": PortfolioDecomposition
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} transactions {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["transactions"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="transactions_limit" type="int" %}
Default: 50
{% endapi-method-parameter %}
{% api-method-parameter name="transactions_offset" type="int" %}
Default: 0
{% endapi-method-parameter %}
{% api-method-parameter name="transactions_search_query" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="asset_types" type="set" %}
Default: set()
{% endapi-method-parameter %}
{% api-method-parameter name="transaction_types" type="set" %}
Default: set()
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address transactions",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "transactions": list[Transaction]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} charts {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["charts"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="charts_max_assets" type="int" %}
Default: 0
{% endapi-method-parameter %}
{% api-method-parameter name="charts_min_percentage" type="int" %}
Default: 100
{% endapi-method-parameter %}
{% api-method-parameter name="charts_type" type="str" %}
Default: d
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address charts",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "charts": Chart]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} deposits {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["deposits"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address deposits",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "deposits": list[Deposit]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} loans {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["loans"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address loans",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "loans": list[Loan]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} nft {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["nft"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="nft_asset_code" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="nft_limit" type="int" %}
Default: 100
{% endapi-method-parameter %}
{% api-method-parameter name="nft_offset" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="sorted_by" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="mode" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="contract_addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address nft",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "nft": list[AddressNFT]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} nft-limited-per-contract {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["nft-limited-per-contract"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="nft_limit_per_contract" type="int" %}
Default: 6
{% endapi-method-parameter %}
{% api-method-parameter name="sorted_by" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="contract_addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address nft-limited-per-contract",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "nft-limited-per-contract": list[AddressNFT]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} nft-total-value {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["nft-total-value"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="value_type" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address nft-total-value",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "nft-total-value": float
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} nft-full-total-value {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["nft-full-total-value"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address nft-full-total-value",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "nft-full-total-value": FullTotalValue
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} nft-contracts {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["nft-contracts"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="sorted_by" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="contract_addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address nft-contracts",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "nft-contracts": list[NFTServiceContract]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %} positions {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["positions"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="assets" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="chains" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="protocols" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received address positions",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "positions": AddressPositions
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


