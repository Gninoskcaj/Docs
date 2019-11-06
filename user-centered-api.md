---
description: A User Centered CRUD API
---

# User-Centered API

## Get Started

1. ```
   $ npm i simple-user-api
   ```
2. ```
   $ npm run dev
   ```
3. Navigate to `localhost:8000`

_**Note: I use postman to send api requests**_

## API

Note: when using the api, send `json` in the body of the request.

This is an example user `json` file.

```
{
    "username": "Gninoskcaj",
    "password": "LetMeIn888",
    "email": "jackson.mooring@gmail.com",
    "ProUser": true
    "Bio": "Making examples is not my thing"
    "Example": "text more text so & so & so"
}
```

{% api-method method="post" host="localhost:8000" path="/users/" %}
{% api-method-summary %}
Create a User
{% endapi-method-summary %}

{% api-method-description %}
This will Create a new file in the `./users` directory containing the body of the request
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="User" type="object" required=true %}
This what will be in the file
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the created information
{% endapi-method-response-example-description %}

```
{
    "username": "Gninoskcaj",
    "password": "LetMeIn888",
    "email": "jackson.mooring@gmail.com",
    "ProUser": true
    "Bio": "Making examples is not my thing"
    "Example": "text more text so & so & so"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="localhost:8000" path="/users/:username" %}
{% api-method-summary %}
Get a User
{% endapi-method-summary %}

{% api-method-description %}
This will get the users information stored in there file.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
The users username
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the the information contents of the file requested
{% endapi-method-response-example-description %}

```
{
    "username": "Gninoskcaj",
    "password": "LetMeIn888",
    "email": "jackson.mooring@gmail.com",
    "ProUser": true
    "Bio": "Making examples is not my thing"
    "Example": "text more text so & so & so"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="localhost:8000" path="/users/:username" %}
{% api-method-summary %}
Update User
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
The users username
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="Update Information" type="object" required=true %}
This is the information to update the database with
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns The Updated information
{% endapi-method-response-example-description %}

```
{
    "username": "Gninoskcaj",
    "password": "LetMeIn888",
    "email": "jackson.mooring@gmail.com",
    "ProUser": false
    "Bio": "Making examples is not my thing"
    "Example": "text more text so & so & so"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="danger" %}
Send The Complete object

If you need to change ProUser from true to false.

**The Body of the request should look like this:**

```
{
    "username": "Gninoskcaj",
    "password": "LetMeIn888",
    "email": "jackson.mooring@gmail.com",
    "ProUser": false
    "Bio": "Making examples is not my thing"
    "Example": "text more text so & so & so"
}
```

**Not This:**

```
{
    "ProUser": false
}
```
{% endhint %}

{% api-method method="delete" host="localhost:8000" path="/users/:username" %}
{% api-method-summary %}
Delete a User
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
The username of a user
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the information of the deleted user
{% endapi-method-response-example-description %}

```
{
    "username": "Gninoskcaj",
    "password": "LetMeIn888",
    "email": "jackson.mooring@gmail.com",
    "ProUser": true
    "Bio": "Making examples is not my thing"
    "Example": "text more text so & so & so"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

