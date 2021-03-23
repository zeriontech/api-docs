# (/assets)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} prices {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
Dict[str, [Asset](#asset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} explore-sections {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="explore_sections" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="explore_sections_aliases" type="list" %}
Default: []
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[ExploreSection](#exploresection)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} info {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="limit" type="int" %}
Default: 10000
{% endapi-method-parameter %}
{% api-method-parameter name="offset" type="int" %}
Default: 0
{% endapi-method-parameter %}
{% api-method-parameter name="explore_section" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="order_by" type="dict" %}
Default: {}
{% endapi-method-parameter %}
{% api-method-parameter name="category_id" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="search_query" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[AssetInfo](#assetinfo)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} full-info {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="asset_code" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
Optional[zerion_api.entities.socketio.AssetFullInfo]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} charts {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="charts_type" type="str" %}
Default: d
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
Dict[str, List[Tuple[int, float]]]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} tags {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="tags_group" type="str" %}
Default: all
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[AssetTag](#assettag)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} actions {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="asset_code" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[AssetAction](#assetaction)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} stats {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="asset_code" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
[AssetStats](#assetstats){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} list {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="order_by" type="dict" %}
Default: {}
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[AssetInfo](#assetinfo)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} tokenlists {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="asset_code" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[Tokenlist](#tokenlist)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/assets" %}
{% api-method-summary %} categories {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[Category](#category)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

