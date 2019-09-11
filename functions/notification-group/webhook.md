# Notification - Webhook

---

Support Webhook notification.

We can actively call the web services or RESTful API provided by third-party system. Don't need to write any scripts !

### Webhook Parameters

| Parameter | Description |
| --- | --- |
| HTTP Method | HTTP request method. \( Currently support GET, POST, PUT, and DELETE\) |
| Waiting Time | HTTP request waiting time. \(Dafault: 30, Unit: second\) |
| URL | Target API URL. |
| Parameters | HTTP request parameters \(Query string\). |
| Headers | HTTP request headers. |
| Body | HTTP request body. \(Only POST, PUT, DELETE\) |

### 

### Create Webhook \(HTTP GET Method\)

PARAMETERS setting: add desc=false, count=1000, and index=1.

![](/assets/webhook_get1.PNG)

HEADER setting: add Authorization

![](/assets/webhook_get2.PNG)

**Variables:**

If the value of PARAMETERS, HEADERS, and BODY is dynamic, you can use {} to mark it as a variable. For example, {index} is a variable. When you call Notification API /api/Groups/send, the parameter "message" of request must be with JSON format and contains key "index", just like {"index": 1}.

![](/assets/webhook_get3.PNG)

### Create Webhook \(HTTP POST Method\)

HEADER setting: add Authorization. \(The key "Content-Type" will be generated automatically by Conten Type in BODY\)

![](/assets/webhook_post1.PNG)

BODY setting: select Application/JSON and fill up the form with JSON format.

![](/assets/webhook_post2.PNG)

Variables:

If the value of PARAMETERS, HEADERS, and BODY is dynamic, you can use {} to mark it as a variable. For example, {scadaId}, {deviceId}, and {tagName} are variables. When you call Notification API /api/Groups/send, the parameter "message" of request must be with JSON format and contains keys {scadaId}, {deviceId}, and {tagName}, just like {"scadaId": "24436be6-2e02-43a6-ad8e-ca4d395fc935", "deviceId": "Device1", "tagName": "ATag1"}.

![](/assets/webhook_post3.PNG)

