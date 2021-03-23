# (/compound)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WEBSOCKET" host="" path="/compound" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
[CompoundInfo](#compoundinfo){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/compound" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[CompoundAsset](#compoundasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/compound" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[CompoundAction](#compoundaction)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/compound" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[CompoundDeposit](#compounddeposit)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/compound" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[CompoundLoan](#compoundloan)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### loans
