# Notification - WhatsApp \(Clickatell\)

---

Support WhatsApp, we used Clickatell to implement.

Clickatell is WhatsApp Cloud API, and we choose Clickatell for support WhatsApp notification function

### Website

Clickatell : [https://clickatell.com](https://console.wassenger.com/)

\(Note: Register WhatsApp and Clickatell account, here we demo register Clickatell account only\)

### Clickatell - WhatsApp Cloud API

* Create new account

  -After register \(about 10 minutes\), we would receive the verification letter.

* Apply WhatsApp

  ![](/assets/擷取.PNG)

* Then fill the form content ![](/assets/擷取1.PNG)

* When you complete the application, you will receive a mail from Clickatell, Clickatell will verify the company's website and facebook business ID. \(About one day Clickatell will response in e-mail \)

* Before received the status is pending.

![](/assets/擷取2.PNG)

* If this apply is success, you can use the WhatsApp API key to send test.

![](/assets/complete.png)

### Group Level

Choose a defined level according to your notification strategy. Default is "Critical" means notifying message in time.

### Template

Support `Text` content. You can pre-define your message template here. When you call `/send` API, you don't need to send entire message string every time, just using the variables.

For example, we pre-define a sentence contains a variable {name}.

![](/assets/Template2.png)So, when you call `/send` API, you just need to send the following body, you will receive a notification with entire message.

```
[
  {
    "groupId": "bHltGj3P6aIs",
    "useTemplate": true,
    "variables": {"name": "demo"}
  }
]
```

### 

### Notification- Add a Member

Type into the Clicktell API key and fill in other information

* Add New number:

  Phone number example: 886902345678 \(without "+"\)

![](/assets/whatsapp_addMember.PNG)

