# API

---

* Current Version: V1.5

### Difference between V1.0 and V1.5

* Custom message template
  * v1.0
    * No
  * v1.5
    * Yes
* Email notification - Recipient type CC and BCC
  * v1.0
    * No
  * v1.5
    * Yes
* Group Type
  * v1.0
    * ex. "type": 2
  * v1.5
    * "ex. type":"line"
* Send API request body

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

* Remove the parameter "subject" of send API
  * v1.0
    * "subject": "string"
  * v1.5
    * Removed
* Modify the structure of the parameter "sendList" of APIs

  * v1.0

  ```
  "sendList": [{
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
  }]
  ```

  * v1.5

  ```
  "sendList": [{
    "target": "Webhook_POST_Test",
    "method": "post",
    "url": "https://portal-technical.wise-paas.com/fake_endpoint",
    "params": {},
    "timeout": 10,
    "headers": {},
    "contentType": 2,
    "body": {}
  }]
  ```

* SendList method
  * v1.0
    * method: 1
  * v1.5
    * method: 'get'
* The parameter "unit" and "expUnit" of Level API

  * v1.0

  ```
  {
    "name": "test",
    "unit": 1,  // interger
    "intervalTime": 45,
    "expTime": 6,
    "expUnit": 3,  // interger
    "batchCount": 1
  }
  ```

  * v1.5

  ```
  {
    "name": "test",
    "unit": "second",  // string
    "intervalTime": 45,
    "expTime": 6,
    "expUnit": "hour",  // string
    "batchCount": 1
  }
  ```



