# Notification - LINE

---

Support LINE notifications.

### Add LINE Notify as a friend

Scan the following QR Code to add LINE Notify as your friend to use the notification service of LINE Notify.

![](/assets/line_notify.png)

### Get LINE Token

1. Login to LINE Notify official website. [https://notify-bot.line.me/my/](https://notify-bot.line.me/my/)

2. Generate a new token.

![](/assets/line_my.png)

1. Enter the token name and select a notification group and press Generate token. \(If the selected notification group is not 1-on-1 chat with LINE Notify, you must first add LINE Notify to the group.\)

![](/assets/line_generate_token.png)

1. Fill in the token into the Member List. \(please keep the token safely, you cannot get the old one and must regenerate.\)

![](/assets/line_token.png)

### Group Level

Choose a defined level according to your notification strategy. Default is "Critical" means notifying message in time.

### Template

Support `Text` content. You can pre-define your message template here. When you call `/send` API, you don't need to send entire message string every time, just send the variables.

For example, we pre-define a sentence contains a variable {name}.

![](/assets/text_template.png)

So, when you call `/send` API, you just need to send the following body, you will receive a notification with entire message.

```
[
  {
    "groupId": "yer8agvrjl4b",
    "useTemplate": true,
    "variables": {"name": "Steven"}
  }
]
```

### Notification - Add a Member

### ![](/assets/lineno.png)![](/assets/linegroup.png)

### 



