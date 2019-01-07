# Notify

---

Currently, provide user two way of notification:

* API
* MQTT

### API

Please refer chapter API.

### MQTT

MQTT topic:

```
/wisepaas/notify/send
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



