# /assets

## Scopes

Here you can find all the scopes available in this particular namespace.

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="prices" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["prices"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="asset_codes" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="explore-sections" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["explore-sections"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="explore_sections" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="explore_sections_aliases" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="info" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["info"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="asset_codes" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-parameter in="body" name="limit" type="int" %}
Default: 10000
{% endswagger-parameter %}

{% swagger-parameter in="body" name="offset" type="int" %}
Default: 0
{% endswagger-parameter %}

{% swagger-parameter in="body" name="explore_section" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="order_by" type="dict" %}
Default: {}
{% endswagger-parameter %}

{% swagger-parameter in="body" name="category_id" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="search_query" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="full-info" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["full-info"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="asset_code" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="charts" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["charts"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="asset_codes" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-parameter in="body" name="charts_type" type="str" %}
Default: d
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="tags" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["tags"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="tags_group" type="str" %}
Default: all
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="actions" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["actions"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="asset_code" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="stats" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["stats"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="asset_code" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="list" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["list"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="asset_codes" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-parameter in="body" name="order_by" type="dict" %}
Default: {}
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="tokenlists" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["tokenlists"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="asset_code" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="assets" method="ws" summary="categories" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["categories"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}
