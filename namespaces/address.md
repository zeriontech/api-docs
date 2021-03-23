# (/address)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'address', 'type': 'str', 'default': '-'}{% endapi-method-request %}
{% api-method-response %}
[AddressInfo](#addressinfo){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'asset_codes', 'type': 'list', 'default': []}{% endapi-method-request %}
{% api-method-response %}
Dict[str, [AddressAsset](#addressasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'portfolio_fields', 'type': '[PortfolioFields](#portfoliofields)', 'default': 'assets'}{% endapi-method-request %}
{% api-method-response %}
[Portfolio](#portfolio){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'transactions_search_query', 'type': 'str', 'default': '-'}{% endapi-method-request %}
{% api-method-response %}
List[[Transaction](#transaction)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'charts_min_percentage', 'type': 'int', 'default': 100}{% endapi-method-request %}
{% api-method-response %}
Dict[str, List[Tuple[int, float]]]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[Deposit](#deposit)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[Loan](#loan)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[LockedAsset](#lockedasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[StakedAsset](#stakedasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
Dict[str, [AddressBSCAsset](#addressbscasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
Dict[str, [AddressPolygonAsset](#addresspolygonasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### polygon-assets
