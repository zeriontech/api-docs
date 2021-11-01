# /address

## Scopes

Here you can find all the scopes available in this particular namespace.

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="info" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["info"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="assets" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["assets"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-parameter in="body" name="asset_codes" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
```
        [
            "received address assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "assets": Dict[str, AddressAsset]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="portfolio" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["portfolio"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-parameter in="body" name="portfolio_fields" type="enum" %}
**PortfolioFields**

: 

`all, assets`

. Default: assets
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="transactions" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["transactions"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
Default: []
{% endswagger-parameter %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-parameter in="body" name="transactions_limit" type="int" %}
Default: 50
{% endswagger-parameter %}

{% swagger-parameter in="body" name="transactions_offset" type="int" %}
Default: 0
{% endswagger-parameter %}

{% swagger-parameter in="body" name="transactions_search_query" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
                    "transactions": List[Transaction]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="charts" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["charts"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
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

{% swagger-parameter in="body" name="charts_max_assets" type="int" %}
Default: 0
{% endswagger-parameter %}

{% swagger-parameter in="body" name="charts_min_percentage" type="int" %}
Default: 100
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
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
                    "charts": Dict[str, List[Tuple[int, float]]]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="deposits" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["deposits"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
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
            "received address deposits",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "deposits": List[Deposit]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="loans" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["loans"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
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
            "received address loans",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "loans": List[Loan]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="locked-assets" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["locked-assets"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
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
            "received address locked-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "locked-assets": List[LockedAsset]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="staked-assets" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["staked-assets"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
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
            "received address staked-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "staked-assets": List[StakedAsset]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="bsc-assets" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["bsc-assets"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
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
            "received address bsc-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "bsc-assets": Dict[str, AddressBSCAsset]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="address" method="ws" summary="polygon-assets" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["polygon-assets"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
Default: -
{% endswagger-parameter %}

{% swagger-parameter in="body" name="addresses" type="list" %}
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
            "received address polygon-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "polygon-assets": Dict[str, AddressPolygonAsset]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}
