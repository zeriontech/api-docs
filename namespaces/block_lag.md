# /block\_lag

## Scopes

Here you can find all the scopes available in this particular namespace.

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="block\_lag" %}
{% api-method-summary %}
block-lag
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
            "received block_lag block-lag",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "block-lag": BlockLag
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

