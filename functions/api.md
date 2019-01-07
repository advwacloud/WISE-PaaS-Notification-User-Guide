# API

---

* Current Version: V1.0

### Get Group List

\[GET\] /groups

Get the group list that you have permission to access.

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

### Send notification

\[POST\] /Groups/send

Send notifications to specific groups. \(Support for sending to multiple groups at once\)

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



