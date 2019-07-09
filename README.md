---
description: Send a Newsletter from your terminal
---

# Gmailer

## Usage

Clone with degit:

```bash
$ npx degit https://github.com/Gninoskcaj/Gmailer my-app
```

Create a file named  `pass.txt`. This is where the password for your gmail account lives. If you are using 2FA you will need to create an [App Password](https://myaccount.google.com/apppasswords). Use your app password instead of the password you usually use.

Next Create a file named `email-list.json` , which is a json file containing an `array`  of all your email Newsletter subscribers.

{% code-tabs %}
{% code-tabs-item title="email-list.json" %}
```javascript
 [
    "myfriend@yahoo.com",
    "john@example.com",
    "yourfriend@gmail.com"
]
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Now, create a file named`config.json`.

{% code-tabs %}
{% code-tabs-item title="config.json" %}
```javascript
{
	"from": "You <you@email.com>",
	"subject": "Gmailer",
	"gmailUserName": "YourGmailUserName"
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
If You have any errors send me an email to **me@jacksonmooring.com** or ping me on discord at **Gninoskcaj\#7292**
{% endhint %}

Once you're done, `npm run send:email`

```bash
npm run send:email
```



