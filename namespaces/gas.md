# /gas

## Scopes

Here you can find all the scopes available in this particular namespace.

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="gas" %}
{% api-method-summary %}
price
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received gas price",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "price": GasPriceInfo
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

