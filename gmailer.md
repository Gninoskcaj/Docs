---
description: Interact with the Gmail API
---

# Gmailer

## Installation

Install the package into your project:

### npm

```
$ npm i gmail-api
```

### yarn

```
$ yarn add gmail-api
```

## API

### `sendMail(options)`

`options: <Object>`

All options are required

| Option | Type | Description |
| :--- | :--- | :--- |
| `username` |  `String` | Your gmail username |
| `password` | `String` | Your gmail password. If you have 2FA this needs to be an [App Password](https://myaccount.google.com/apppasswords?utm_source=google-account&utm_medium=web&rapt=AEjHL4PF6gZJQaty6YPxHvAxr2rquv_z7k-7DnEfSd786uc8jA1ayfWlInV9ZCn1st4VQ32qL63MpDQLbsv-FAfSmjR93ZLBtA) |
| `from` | `String` | Senders email address |
| `to` | `String`, `List` or `Array` | Who to send the email to. |
| `subject` | `String` | Subject of the email |
| `body` | `String` | Body of the email. Accepts `html` |

Example:

    const { sendMail, file } = require('gmail-api');

    sendMail({
        username: 'jackson.mooring@gmail.com',
        password: 'MyTopSecret:-)'
        from: '"John Doe" <john@doe.com>',

        // <Array> Sends an individual email to each person.

        // <List> Sends one email to all recipients
        // (e. g. 'my@email.com, your@email.com')

        // <String> Send one email to the recipient
        // (e. g. 'my@email.com')
        to: [ "myfriend@yahoo.com", "yourfriend@hotmail.com" ], 
        subject: 'Node.js Email',

        // `file(url)` Sends the contents of the file url
        body: file('../email.html')
    })

### `file(url)`

 `url: <String> or <Url>`

Sends the contents of the url.

```
const { file } = require('gmail-api')

// Accepts absolute and relative paths
file('https://example.com/myfile.html');
file('../myfile.js');
```

{% hint style="success" %}
Questions? Feel free to contact me by **email**, **`jackson.mooring@gmail.com`** or ping me **Discord**,**`Gninoskcaj#7292`**
{% endhint %}

