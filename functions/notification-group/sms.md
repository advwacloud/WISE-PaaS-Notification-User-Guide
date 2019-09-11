# Notification - SMS

---

Support SMS, we used Clicktell to implement.

Clikctell is SMS 3rd party API, and we choose Clicktell to Support SMS notification function.

### Website

Clicktell: [https://portal.clickatell.com/\#/](https://portal.clickatell.com/#/)

### Clicktell-SMS API

1.Create new account to get started.![](/assets/0_portal.png)

After register \(about 10 minutes\) , we would receive the verification letter

And we choose "Get started with Single API for SMS only".

![](/assets/1_SMSonly.png)

![](/assets/2_Createnewintegrate.png)

Taiwan and China only One-way message option for choosed.

![](/assets/3_Createnewintegrate_feature.png)In the Settings page,we can enable/disable all the setting

![](/assets/4_setting_1.png)

Save integration.

![](/assets/5_save.png)

After complete all setting, now Start the Step 1 "Setup your test phones"

![](/assets/6_setupPhone.png)

Enter Mobile phone.

![](/assets/7_addtestphone.png)

Enter verification code

![](/assets/8_uniquecode.png)

Add test phone successfully.

![](/assets/9_1ststepdone.png)

Now to the Step 2 "Create and test a SMS integration".

a. Select your integration: using the drop-down menu to choose the integrated item.

b. Select test number: enter the phone number which to receive message.

c. Sample SMS Text: type the message content what you want to received.

![](/assets/10_Create and test a SMS integration.png)

Step 3: "Setup your account "

Binding credit card \(we can pass this process, and used SMS successfully\)![](/assets/11_2ndsetupdone.png)

Now to using the left side menu: SMS Manage test phones.

SMS -&gt; Manage test phones including binding mobile detailed info \(including phone number, binding info, and mobile status.\) .![](/assets/12_Manage test phones.png)

API Key:  the API to connect wiht WISE-PaaS/Notification setting.

Make sure Integration API status is Activate \(or  function can't work successfully\)![](/assets/13_SMS intrgrations.png)Reporting : check the report \(all messages sent and received history\)

Report info:![](/assets/15_GenerateReport.png)Message ID detail: message detail \(number、message content\) ![](/assets/16_reportDetail.png)

### Group Level

Choose a defined level according to your notification strategy. Default is "Critical" means notifying message in time.

### Template

Support Text content. You can pre-define your message template here. When you call `/send` API, you don't need to send entire message string every time, just using the variables.

For example, we pre-define a sentence contains a variable {name}.

![](/assets/Template2.png)So, when you call /send API, you just need to send the following body, you will receive a WeChat notification with entire message.

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

"+" icon to create SMS Group![](/assets/SMS_portal.png)

Type into the Clicktell API and fill in other information

![](/assets/editscreen.png)

Add New number:

Phone number example: +886911960999 \(with/without "+" is all work\) ![](/assets/+.png)

