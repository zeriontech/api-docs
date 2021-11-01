# /compound

## Scopes

Here you can find all the scopes available in this particular namespace.

{% swagger baseUrl="wss://api-v4.zerion.io/" path="compound" method="ws" summary="info" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["info"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
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
            "received compound info",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "info": CompoundInfo
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="compound" method="ws" summary="assets" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["assets"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="currency" type="enum" %}
**PriceCurrency**

: 

`eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`

. Default: usd
{% endswagger-parameter %}

{% swagger-response status="200" description="Successful result." %}
```
        [
            "received compound assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "assets": List[CompoundAsset]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="compound" method="ws" summary="actions" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["actions"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
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
            "received compound actions",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "actions": List[CompoundAction]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="compound" method="ws" summary="deposits" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["deposits"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
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
            "received compound deposits",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "deposits": List[CompoundDeposit]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="compound" method="ws" summary="loans" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["loans"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="address" type="str" %}
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
            "received compound loans",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "loans": List[CompoundLoan]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}
