# Query Datasets

on Rapid API you have direct access to any dataset's information. To query a dataset follow this instructions:

1. Go to [https://rapidapi.com/aletheia-data-aletheia-data-default/api/aletheia2/](https://rapidapi.com/aletheia-data-aletheia-data-default/api/aletheia2/)
2. Open up the V1 dropdown and select SEARCH - IPFS endpoint (V1)
3. Scroll down to fill all the needed parameters

{% swagger method="get" path="" baseUrl="https://aletheia2.p.rapidapi.com/v1/_search/ipfs/csv/%7Bcid%7D" summary="Example Parameter" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" required="false" name="start" %}
Start point of the query. Default: 0
{% endswagger-parameter %}

{% swagger-parameter in="query" name="limit" required="false" %}
Limit point of the query. Default: 25
{% endswagger-parameter %}

{% swagger-parameter in="query" name="info" required="false" %}
Return information about this asset
{% endswagger-parameter %}

{% swagger-parameter in="query" name="fields" %}
Fields required by the user
{% endswagger-parameter %}

{% swagger-parameter in="query" name="value" %}
Value the user is looking for
{% endswagger-parameter %}

{% swagger-parameter in="query" name="order" %}
Order of the result (format: <field>:<asc/desc>). Default: id:asc
{% endswagger-parameter %}

{% swagger-parameter in="path" name="host" required="true" %}
Service where the asset is located
{% endswagger-parameter %}

{% swagger-parameter in="path" name="format" required="true" %}
What is the format of the required file
{% endswagger-parameter %}

{% swagger-parameter in="path" name="cid" required="true" %}
CID of the asset required
{% endswagger-parameter %}
{% endswagger %}
