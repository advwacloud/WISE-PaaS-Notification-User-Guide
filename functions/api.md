# API

---

* Current Version: V1.5

### API 1.0/1.5差異

* 客製化訊息範本
    * v1.0
        * 無
    * v1.5
        * 支援
* Email支援CC和BCC
    * v1.0
        * 無
    * v1.5
        * 支援
* Group Type數字改成文字
    * v1.0
        * ex. "type": 2
    * v1.5
        * "ex. type":"line"
* Send API request body結構修改
    * v1.0
```
[
  {
    "groupId": "string",
    "message": {},
    "subject": "string"
  }
]
```
    * v1.5
```
[
  {
    "groupId": "string",
    "useTemplate": true,
    "message": "string",
    "variables": {}
  }
]
```
* 拿掉send API subject欄位
    * v1.0
        * "subject": "string"
    * v1.5
        * 拿掉此欄位
* sendList裡的webhookCfg內容移到上一層, 並拿掉webhookCfg物件
    * v1.0
```
  "sendList": [
    {
      "target": "Webhook_POST_Test",
      "webhookCfg": {
        "method": 2,
        "url": "https://portal-technical.wise-paas.com/fake_endpoint",
        "params": {},
        "timeout": 10,
        "headers": {},
        "contentType": 2,
        "body": {}
      }
    }
  ]
```
    * v1.5
```
  "sendList": [
    {
      "target": "Webhook_POST_Test",
      "method": "post",
      "url": "https://portal-technical.wise-paas.com/fake_endpoint",
      "params": {},
      "timeout": 10,
      "headers": {},
      "contentType": 2,
      "body": {}
    }
  ]
```
* sendList的method從數字改成文字
    * v1.0
        * method: 1
    * v1.5
        * method: 'get'
* level的unit/expUnit從數字型態改成文字
    * v1.0
```
    {
      "name": "test",
      "unit": 1,
      "intervalTime": 45,
      "expTime": 6,
      "expUnit": 3,
      "batchCount": 1
    }
```
    * v1.5
```
      "name": "test",
      "unit": "second",
      "intervalTime": 45,
      "expTime": 6,
      "expUnit": "hour",
      "batchCount": 1
    }
```
