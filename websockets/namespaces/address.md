# /address

## Scopes

Here you can find all the scopes available in this particular namespace.

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
info
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["info"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address info",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "info": AddressInfo
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
assets
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["assets"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}

{% api-method-parameter name="asset\_codes" type="list" %}
Default: \[\]
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "assets": Dict[str, AddressAsset]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
portfolio
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["portfolio"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}

{% api-method-parameter name="portfolio\_fields" type="enum" %}
**PortfolioFields**: `all, assets`. Default: assets
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address portfolio",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "portfolio": Portfolio
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
transactions
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["transactions"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}

{% api-method-parameter name="transactions\_limit" type="int" %}
Default: 50
{% endapi-method-parameter %}

{% api-method-parameter name="transactions\_offset" type="int" %}
Default: 0
{% endapi-method-parameter %}

{% api-method-parameter name="transactions\_search\_query" type="str" %}
Default: -
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address transactions",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "transactions": List[Transaction]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
charts
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["charts"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}

{% api-method-parameter name="charts\_type" type="str" %}
Default: d
{% endapi-method-parameter %}

{% api-method-parameter name="charts\_max\_assets" type="int" %}
Default: 0
{% endapi-method-parameter %}

{% api-method-parameter name="charts\_min\_percentage" type="int" %}
Default: 100
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address charts",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "charts": Dict[str, List[Tuple[int, float]]]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
deposits
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["deposits"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address deposits",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "deposits": List[Deposit]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
loans
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["loans"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address loans",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "loans": List[Loan]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
locked-assets
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["locked-assets"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address locked-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "locked-assets": List[LockedAsset]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
staked-assets
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["staked-assets"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address staked-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "staked-assets": List[StakedAsset]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
bsc-assets
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["bsc-assets"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address bsc-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "bsc-assets": Dict[str, AddressBSCAsset]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="WS" host="wss://api-v4.zerion.io/" path="address" %}
{% api-method-summary %}
polygon-assets
{% endapi-method-summary %}

{% api-method-description %}
Example request `[ "get", { "scope": ["polygon-assets"], "payload": { "body parameter": "value" } } ]`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="address" type="str" %}
Default: -
{% endapi-method-parameter %}

{% api-method-parameter name="addresses" type="list" %}
Default: \[\]
{% endapi-method-parameter %}

{% api-method-parameter name="currency" type="enum" %}
**PriceCurrency**: `eth, btc, usd, eur, krw, rub, gbp, aud, cad, inr, jpy, nzd, try, zar, cny, chf`. Default: usd
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful result.
{% endapi-method-response-example-description %}

```text
        [
            "received address polygon-assets",
            {
                "meta": {
                    "status": "ok",
                    "request parameter1": "value1",
                    "request parameter2": "value2"
                },
                "payload": {
                    "polygon-assets": Dict[str, AddressPolygonAsset]
                }
            }
        ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

