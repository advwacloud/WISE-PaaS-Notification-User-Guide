# Notification - Email

---

Support for Email notifications. Users can use their own mail server or mail service provided by a third-party company \(Google, Microsoft\).

### E-mail Service Setting Parameters

| Parameter | Description |
| --- | --- |
| SMTP Server | Mail server IP address. |
| SMTP Port | Mail server Port. |
| Secure | SSL or TLS |
| SMTP Account | Mail server account. |
| SMTP Password | Mail server password. |
| Sender Email | The Email address of sender. |
| E-Mail Subject | Email subject. |

For example \(Gmail setting\):  
![](/assets/email_setting.png)

### Group Level
Choose a defined level according to your notification strategy. Default is "Critical" means notifying message in time.

### Templcate
Support `HTML` and `Text` content. You can pre-define your message template here. When you call `/send` API, you don't need to send entire message string every time, just send the variables.

For example, we pre-define a sentence contains a variable {cocktail} and a picture.

![](/assets/email_template1.png)

So, when you call `/send` API, you just need to send the following body, you will receive a email with entire message.
```
[
  {
    "groupId": "yer8agvrjl4b",
    "useTemplate": true,
    "variables": {"cocktail": "Negroni"}
  }
]
```

![](/assets/email_template2.png)


### Add a Member

![](/assets/email_add_member1.png)

You can assign the recipient type (To/CC/BCC) to a new member.

![](/assets/email_add_member2.png)

