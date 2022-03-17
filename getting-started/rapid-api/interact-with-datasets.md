# Interact with Datasets

on Rapid API you have direct access to any dataset's information. To query a dataset follow this instructions:

1. Go to [https://rapidapi.com/aletheia-data-aletheia-data-default/api/aletheia2/](https://rapidapi.com/aletheia-data-aletheia-data-default/api/aletheia2/)
2. Open up the V1 dropdown and select SEARCH - IPFS endpoint (V1)
3. Scroll down to fill all the needed parameters

{% swagger method="get" path="" baseUrl="https://aletheia2.p.rapidapi.com/v1/_search/<host>/<format>/<CID>" summary="Example Parameter" %}
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
What is the format of the required asset
{% endswagger-parameter %}

{% swagger-parameter in="path" name="cid" required="true" %}
CID of the asset required
{% endswagger-parameter %}
{% endswagger %}

### Query Dataset

1. To find a dataset to query, **go to**: [https://app.aletheiadata.org/dashboard](https://app.aletheiadata.org/dashboard)
2. Search for a Dataset. **Example**: [https://app.aletheiadata.org/single/dep/bafkreigihqba7uy6rnwyfsn2tlkflrfzk3zeebzxp2lnquq6wpa3o6vdaa](https://app.aletheiadata.org/single/dep/bafkreigihqba7uy6rnwyfsn2tlkflrfzk3zeebzxp2lnquq6wpa3o6vdaa)
3. Click on **IPFS** under **Connect**. This will copy in your clipboard the asset's CID

![](../../.gitbook/assets/app.aletheiadata.org\_single\_dep\_bafkreigihqba7uy6rnwyfsn2tlkflrfzk3zeebzxp2lnquq6wpa3o6vdaa.png)

&#x20;  4\. **Enter CID** in the CID field in the **API's required field**

&#x20;  5\. Add any other required parameter **(see above)**

&#x20;  6\. Press **Test Endpoint**

![](<../../.gitbook/assets/rapidapi.com\_aletheia-data-aletheia-data-default\_api\_aletheia2 (1) (1).png>)

You can also copy the **Code Snippets** available in _**many different programming languages**_.

To **learn more** go to [https://docs.rapidapi.com/docs/consumer-quick-start-guide](https://docs.rapidapi.com/docs/consumer-quick-start-guide)



