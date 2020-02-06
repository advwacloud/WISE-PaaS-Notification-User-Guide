# Notification - SMS \(Clickatell\)

---

Support SMS, we used Clickatell to implement.

Clickatell  is SMS 3rd party API, and we choose Clickatell to Support SMS notification function.

### Website

Clickatell : [https://portal.clickatell.com/\#/](https://portal.clickatell.com/#/)

### Clickatell -SMS API

1.Create new account to get started.![](/assets/0_portal.png)

After register \(about 10 minutes\) , we would receive the verification letter

And we choose "Get started with Single API for SMS only".

![](/assets/1_SMSonly.png)

Sandbox environment allows only 3 test phones at most. Production environment is unlimited.

![](/assets/integration.png)

Taiwan and China only One-way message option for choosed.

![](/assets/3_Createnewintegrate_feature.png)

It is recommended to enable message parts and at least choose 2 part messages if your message is longer.

![](/assets/4_setting_1.png)

Save integration.

![](/assets/5_save.png)

Make sure Integration API status is Activate \(or  function can't work successfully\)

![](/assets/13_SMS_intrgrations.png)

### Group Level

Choose a defined level according to your notification strategy. Default is "Critical" means notifying message in time.

### Template

Support `Text` content. You can pre-define your message template here. When you call `/send` API, you don't need to send entire message string every time, just using the variables.

For example, we pre-define a sentence contains a variable {name}.

![](/assets/Template2.png)So, when you call `/send` API, you just need to send the following body, you will receive a notification with entire message.

```
[
  {
    "groupId": "yer8agvrjl4b",
    "useTemplate": true,
    "variables": {"name": "Steven"}
  }
]
```

### 

### Notification- Add a Member

Enter the API key of your SMS integration on Clicktell

![](/assets/editscreen.png)

Phone number example: 886911960999 \(without "+"\) ![](/assets/+.png)

