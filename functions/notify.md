# Notify

---
目前提供使用者兩種方式通知方式：
* API
* MQTT/AMQP

### API
請參考API章節中的發送通知

### MQTT/AMQP

MQTT topic:
```
/wisepaas/notify/send
```
AMQP topic:
```
.wisepaas.notify.send
```
json format:
```
[
  {
    "groupId": "string",
    "message": "string",
    "subject": "string"
  }
]
```
