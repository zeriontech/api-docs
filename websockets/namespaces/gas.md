# /gas

## Scopes

Here you can find all the scopes available in this particular namespace.

{% swagger baseUrl="wss://api-v4.zerion.io/" path="gas" method="ws" summary="price" %}
{% swagger-description %}
Example request 

`[ "get", { "scope": ["price"], "payload": { "body parameter": "value" } } ]`
{% endswagger-description %}

{% swagger-response status="200" description="Successful result." %}
```
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
{% endswagger-response %}
{% endswagger %}
