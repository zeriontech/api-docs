# (/dydx)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WS" host="wss://api-v4.zerion.io/" path="dydx" %}
{% api-method-summary %} deposits {% endapi-method-summary %}
{% api-method-description %}Example request

        [
            [
                "get",
                {
                  "scope": ["deposits"],
                  "payload": {
                      "body parameter": "value"
                  }
                }
            ]
        ]

        {% endapi-method-description %}{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="dydx" %}
{% api-method-summary %} loans {% endapi-method-summary %}
{% api-method-description %}Example request

        [
            [
                "get",
                {
                  "scope": ["loans"],
                  "payload": {
                      "body parameter": "value"
                  }
                }
            ]
        ]

        {% endapi-method-description %}{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`.
Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}
{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}
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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

