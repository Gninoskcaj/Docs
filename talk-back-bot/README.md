---
description: A Programable Virtual Assistant
---

# Talk-Back-Bot

## Usage

```
$ npm i talk-back-bot
```

```
$ npm i compilerBot
```

{% hint style="info" %}
This App can be used  in browser as well as the server
{% endhint %}

Once installed create a file named `commands.json`

```
[
    {
        "q":"What is your name?",
        "a": "Roby"
    }
]
```

`commands.json` is an `array` of `objects` each `object` being a question/answer pare.

Lets say you wanted to make a chat bot like Siri. You might start with the name.

```
[
    {
        "q": "What is your name?",
        "a": "Roby"
    }
]
```

You could do it like that. But it would be better to access the information object like this.

```
[
    {
        "q": "What is your name?",
        "a": ":name:"
    }
]
```

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

