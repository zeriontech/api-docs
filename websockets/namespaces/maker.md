# /maker

## Scopes

Here you can find all the scopes available in this particular namespace.

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="maker" %}
{% api-method-summary %}
cdp
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["cdp"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="cdp\_id" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="maker" %}
{% api-method-summary %}
vault
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["vault"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="vault\_id" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="maker" %}
{% api-method-summary %}
cdp-actions
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["cdp-actions"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="cdp\_id" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="maker" %}
{% api-method-summary %}
vault-actions
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["vault-actions"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="vault\_id" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

