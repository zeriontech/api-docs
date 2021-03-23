# (/address)
## Scopes 
Here you can find all the scopes available in this particular namespace. 
{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} info {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
[AddressInfo](#addressinfo){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} assets {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="asset_codes" type="list" %}
Default: []
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
Dict[str, [AddressAsset](#addressasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} portfolio {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="portfolio_fields" type="[PortfolioFields](#portfoliofields)" %}
Default: assets
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
[Portfolio](#portfolio){% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} transactions {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="transactions_limit" type="int" %}
Default: 50
{% endapi-method-parameter %}
{% api-method-parameter name="transactions_offset" type="int" %}
Default: 0
{% endapi-method-parameter %}
{% api-method-parameter name="transactions_search_query" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[Transaction](#transaction)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} charts {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% api-method-parameter name="charts_type" type="str" %}
Default: d
{% endapi-method-parameter %}
{% api-method-parameter name="charts_max_assets" type="int" %}
Default: 0
{% endapi-method-parameter %}
{% api-method-parameter name="charts_min_percentage" type="int" %}
Default: 100
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
Dict[str, List[Tuple[int, float]]]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} deposits {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[Deposit](#deposit)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} loans {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[Loan](#loan)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} locked-assets {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[LockedAsset](#lockedasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} staked-assets {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
List[[StakedAsset](#stakedasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} bsc-assets {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
Dict[str, [AddressBSCAsset](#addressbscasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WEBSOCKET" host="" path="/address" %}
{% api-method-summary %} polygon-assets {% endapi-method-summary %}
{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% api-method-parameter name="addresses" type="list" %}
Default: []
{% endapi-method-parameter %}
{% api-method-parameter name="currency" type="[PriceCurrency](#pricecurrency)" %}
Default: usd
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}
{% api-method-response %}
Dict[str, [AddressPolygonAsset](#addresspolygonasset)]{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

