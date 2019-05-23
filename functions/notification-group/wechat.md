# Notification - WeChat

---

Support WeChat notifications.

### 註冊企業微信

### 登入Wechat\(企業微信\)

登入Wechat 企業微信網頁 [https://work.weixin.qq.com/](https://work.weixin.qq.com/)  
掃描QR Code登入企業微信，進入管理頁面。

![](/assets/wechat_business_login.png)  
![](/assets/wechat_business_login_qrcode.png)

### 增加使用者

1. 點選"添加成員"

![](/assets/wechat_business_add_user.png)

1. 填入基本資料

![](/assets/wechat_business_user_info.png)

1. 取得userId

![](/assets/wechat_business_userId.png)

### 新增應用

1. 點選"應用與小程序"
2. 點選"創建應用"建立新的應用

![](/assets/wechat_business_add_application.png)

1. 填入應用資料

![](/assets/wechat_business_input_application.png)

1. 取得agentId和agentSecret

![](/assets/wechat_business_application_info.png)

### 取得cropId

1. 點選"我的企業"，並取得企業ID

![](/assets/wechat_business_info.png)

### Group Level

Choose a defined level according to your notification strategy. Default is "Critical" means notifying message in time.

### Templcate

Support `Text` content. You can pre-define your message template here. When you call `/send` API, you don't need to send entire message string every time, just send the variables.

For example, we pre-define a sentence contains a variable {name}.

![](/assets/text_template.png)

So, when you call `/send` API, you just need to send the following body, you will receive a WeChat message with entire message.

```
[
  {
    "groupId": "yer8agvrjl4b",
    "useTemplate": true,
    "variables": {"name": "Steven"}
  }
]
```

### Add a Member

1. Fill in agentId, agentSecret, and cropId

![](/assets/wechat_business_add_member1.png)

1. Fill in userId

![](/assets/wechat_business_add_member2.png)

