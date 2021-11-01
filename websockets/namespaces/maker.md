# /maker

## Scopes

Here you can find all the scopes available in this particular namespace.

{% swagger baseUrl="wss://api-v4.zerion.io/" path="maker" method="ws" summary="cdp" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["cdp"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="cdp_id" type="str" %}
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
            "received maker cdp",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "cdp": MakerCDP
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="maker" method="ws" summary="vault" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["vault"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="vault_id" type="str" %}
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
            "received maker vault",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "vault": MakerVault
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="maker" method="ws" summary="cdp-actions" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["cdp-actions"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="cdp_id" type="str" %}
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
            "received maker cdp-actions",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "cdp-actions": List[MakerCDPAction]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="wss://api-v4.zerion.io/" path="maker" method="ws" summary="vault-actions" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["vault-actions"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-parameter in="body" name="vault_id" type="str" %}
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
            "received maker vault-actions",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "vault-actions": List[MakerVaultAction]
                }
            }
        ]
```
{% endswagger-response %}
{% endswagger %}
