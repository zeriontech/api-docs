# (/assets)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
Dict[str, [Asset](#asset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'explore_sections_aliases', 'type': 'list', 'default': []}{% endapi-method-request %}
{% api-method-response %}
List[[ExploreSection](#exploresection)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'search_query', 'type': 'str', 'default': '-'}{% endapi-method-request %}
{% api-method-response %}
List[[AssetInfo](#assetinfo)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
Optional[zerion_api.entities.socketio.AssetFullInfo]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'charts_type', 'type': 'str', 'default': 'd'}{% endapi-method-request %}
{% api-method-response %}
Dict[str, List[Tuple[int, float]]]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'tags_group', 'type': 'str', 'default': 'all'}{% endapi-method-request %}
{% api-method-response %}
List[[AssetTag](#assettag)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
List[[AssetAction](#assetaction)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'currency', 'type': '[PriceCurrency](#pricecurrency)', 'default': 'usd'}{% endapi-method-request %}
{% api-method-response %}
[AssetStats](#assetstats){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'order_by', 'type': 'dict', 'default': {}}{% endapi-method-request %}
{% api-method-response %}
List[[AssetInfo](#assetinfo)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{'field': 'asset_code', 'type': 'str', 'default': '-'}{% endapi-method-request %}
{% api-method-response %}
List[[Tokenlist](#tokenlist)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} Get Cakes {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{}{% endapi-method-request %}
{% api-method-response %}
List[[Category](#category)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### categories
