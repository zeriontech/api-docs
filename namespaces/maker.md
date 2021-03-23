# (/maker)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WEBSOCKET" host="" path="/maker" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
[MakerCDP](#makercdp){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/maker" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
[MakerVault](#makervault){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/maker" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[MakerCDPAction](#makercdpaction)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/maker" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[MakerVaultAction](#makervaultaction)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### vault-actions
