# /dydx

## Scopes

Here you can find all the scopes available in this particular namespace.

{% swagger baseUrl="wss://api-v4.zerion.io/" path="dydx" method="ws" summary="deposits" %}
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
            "received dydx deposits",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "deposits": List[DyDxAccountBalance]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="dydx" method="ws" summary="loans" %}
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
            "received dydx loans",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "loans": List[DyDxAccountBalance]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}
