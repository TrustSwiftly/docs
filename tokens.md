# Tokens

{% api-method method="post" host="https://{sub-domain}.trustswiftly.com/account" path="/api/users/{id}/token" %}
{% api-method-summary %}
Create token
{% endapi-method-summary %}

{% api-method-description %}
Create a users **clientToken** to enable use of the embedded functionality.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
**Bearer token** is used for server-to-server communication to fetch sensitive data that you already have access to.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "token": "MnxMeUwxUUxUWXFQTFdObVhPTm1FYnFlU1cxZ2IwOElzcE9qUmdUN1Ra"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


