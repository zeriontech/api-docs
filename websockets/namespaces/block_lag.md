# /block\_lag

## Scopes

Here you can find all the scopes available in this particular namespace.

{% swagger baseUrl="wss://api-v4.zerion.io/" path="block_lag" method="ws" summary="block-lag" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["block-lag"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-response status="200" description="Successful result." %}
```
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
{% endswagger-response %}
{% endswagger %}
