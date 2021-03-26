# (/assets)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} prices {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["prices"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="asset_codes" type="list" %}
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
            "received assets prices",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "prices": Dict[str, Asset]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} explore-sections {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["explore-sections"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="explore_sections" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="explore_sections_aliases" type="list" %}
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
            "received assets explore-sections",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "explore-sections": List[ExploreSection]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
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
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="limit" type="int" %}
Default: 10000
{% endapi-method-parameter %}
{% api-method-parameter name="offset" type="int" %}
Default: 0
{% endapi-method-parameter %}
{% api-method-parameter name="explore_section" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="order_by" type="dict" %}
Default: {}
{% endapi-method-parameter %}
{% api-method-parameter name="category_id" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="search_query" type="str" %}
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
            "received assets info",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "info": List[AssetInfo]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} full-info {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["full-info"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="asset_code" type="str" %}
Default: -
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
            "received assets full-info",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "full-info": Optional[zerion_api.entities.socketio.AssetFullInfo]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
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
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="charts_type" type="str" %}
Default: d
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
            "received assets charts",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "charts": Dict[str, List[Tuple[int, float]]]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} tags {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["tags"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="tags_group" type="str" %}
Default: all
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
            "received assets tags",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "tags": List[AssetTag]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} actions {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["actions"],
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
{% api-method-parameter name="asset_code" type="str" %}
Default: -
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
            "received assets actions",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "actions": List[AssetAction]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} stats {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["stats"],
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
{% api-method-parameter name="asset_code" type="str" %}
Default: -
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
            "received assets stats",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "stats": AssetStats
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} list {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["list"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="order_by" type="dict" %}
Default: {}
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
            "received assets list",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "list": List[AssetInfo]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} tokenlists {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["tokenlists"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="asset_code" type="str" %}
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
            "received assets tokenlists",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "tokenlists": List[Tokenlist]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="assets" %}
{% api-method-summary %} categories {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["categories"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

        [
            "received assets categories",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "categories": List[Category]
                }
            }
        ]

        ```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

