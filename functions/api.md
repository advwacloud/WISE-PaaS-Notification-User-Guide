# API

---

* 目前版本: V1.0
* 呼叫範例: [https://portal-notification-{org\_name}-{space\_name}.{host\_name}/api/V1.0/{api}](https://portal-notification-{org_name}-{space_name}.{host_name}/api/V1.0/{api})

### 取得通知群組列表

\[GET\] /groups

取得所有有權限查看的通知群組列表資訊

* Response Body

```
{
  "list": [
    {
      "groupId": "string",
      "name": "string",
      "description": "string",
      "type": 0,
      "config": {
        "host": "string",
        "port": 0,
        "secure": true,
        "method": "string",
        "username": "string",
        "password": "string",
        "senderEmail": "string",
        "emailSubject": "string"
      },
      "sendList": [
        {
          "firstName": "string",
          "lastName": "string",
          "target": "string"
        }
      ]
    }
  ],
  "totalCount": 0,
  "index": 0,
  "count": 0
}
```

### 發送通知

\[POST\] /Groups/send

* Request Body

```
[
  {
    "groupId": "string",
    "message": "string",
    "subject": "string"
  }
]
```

* Response Body

```
[
  {
    "groupId": "string",
    "result": [
      {
        "target": "string",
        "isSuccess": true,
        "errMsg": "string"
      }
    ]
  }
]
```



