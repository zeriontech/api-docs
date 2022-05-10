# (/chains)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WS" host="wss://api-v4.zerion.io/" path="chains" %}
{% api-method-summary %} info {% endapi-method-summary %}
{% api-method-description %}
Example request
`[
    "get",
    {
      "scope": ["info"],
      "payload": {
          "body parameter": "value"
      }
    }
]`
{% endapi-method-description %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
```

[
    "received chains info",
    {
        "meta": {
            "status": "ok",
            "request parameter1": "value1",
            "request parameter2": "value2"
        },
        "payload": {
            "info": List[ChainInfo]
        }
    }
]

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


