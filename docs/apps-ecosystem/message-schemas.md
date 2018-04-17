---
description: A list of JSON data structures agreed all over the ecosystem
---

# Message schemas

{% api-method method="get" host="https://api.example.com" path="/v1/event/:id" %}
{% api-method-summary %}
Get Event
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID of the event to get.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Event successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "type": "economic-event",
    "provider": "Bob",
    "receiver": "Lynn",
    "action": "work",
    "affectedQuantity": {
      "quantity": 3,
      "unit": {
        "name": "hour",
        "id": 1
      }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



