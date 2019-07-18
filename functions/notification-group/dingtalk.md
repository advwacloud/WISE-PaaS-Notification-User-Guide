# Notification - DingTalk

---

Support DingTalk notifications.

### 

### Register an account

DingTalk official website [https://www.dingtalk.com](https://www.dingtalk.com/)

![](/assets/dingtalk_register.png)

### Login ![](/assets/dingtalk_home.png)

### Create an application![](/assets/dingtalk_createapp1.png)

![](/assets/dingtalk_createapp2.png)

![](/assets/dingtalk_createapp3.png)  
\[註1\] 服務器公網出口IP名單請填入WISE-PaaS平台的Public IP. \(依據平台所在地而有所不同, 若不清楚請詢問平台相關人員\)

### Get DingTalk Setting

![](/assets/dingtalk_appinfo1.png)

![](/assets/dingtalk_getsetting.png)

Get UserId  
![](/assets/dingtalk_getuserId.png)

Get DepartmentId  
![](/assets/dingtalk_getdeptId.png)

### Group Level

Choose a defined level according to your notification strategy. Default is "Critical" means notifying message in time.

### Templcate

Support `Text` content. You can pre-define your message template here. When you call `/send` API, you don't need to send entire message string every time, just send the variables.

For example, we pre-define a sentence contains a variable {name}.

![](/assets/text_template.png)

So, when you call `/send` API, you just need to send the following body, you will receive a DingTalk notification with entire message.

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

1. Fill in AgentId, AppKey, and AppSecret

![](/assets/dingtalk_add_member1.png)

1. Fill in Id and recipient type

![](/assets/dingtalk_add_member2.png)



### Notice

The messages have the same contents will be sent once. It's the limitation of DingTalk.



