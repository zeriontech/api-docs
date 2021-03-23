# (/dydx)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WEBSOCKET" host="" path="/dydx" %}
{% api-method-summary %} deposits {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[DyDxAccountBalance](#dydxaccountbalance)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/dydx" %}
{% api-method-summary %} loans {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[DyDxAccountBalance](#dydxaccountbalance)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

