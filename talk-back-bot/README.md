---
description: A Programable Virtual Assistant
---

# Talk-Back-Bot

## Usage

```bash
$ npm i talk-back-bot
```

```bash
$ npm i compilerBot
```

{% hint style="info" %}
This App can be used  in browser as well as the server
{% endhint %}

Once installed create a file named `commands.json`

{% code-tabs %}
{% code-tabs-item title="commands.json" %}
```javascript
[
    {
        "q":"What is your name?",
        "a": "Roby"
    }
]
```
{% endcode-tabs-item %}
{% endcode-tabs %}

`commands.json` is an `array` of `objects` each `object` being a question/answer pare.

Lets say you wanted to make a chat bot like Siri. You might start with the name.

{% code-tabs %}
{% code-tabs-item title="commands.json" %}
```javascript
[
    {
        "q": "What is your name?",
        "a": "Roby"
    }
]
```
{% endcode-tabs-item %}
{% endcode-tabs %}

You could do it like that. But it would be better to access the information object like this.

{% code-tabs %}
{% code-tabs-item title="commands.json" %}
```javascript
[
    {
        "q": "What is your name?",
        "a": ":name:"
    }
]
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Methods

### Colon

| Action | Selector | Example |
| :--- | :--- | :--- |
| Accesses the information object | colon | `:name:` |

For more information see:

{% page-ref page="accessing-the-information-object.md" %}

### Dot

| Action | Selector | Example |
| :--- | :--- | :--- |
| Checks wether the `q` contains what is inside the dots | dot | `.name.` |

### Semi

| Action | Selector | Example |
| :--- | :--- | :--- |
| Use AI to determine if the command \(`q`\) is a question | semi-colon | `;?;` |

