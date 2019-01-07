# Notification - Webhook

---

支援Webhook通知。使用者可以透過設定呼叫第三方系統提供的Web Service或RESTful API。.

### Webhook 參數說明

| Parameter | Description |
| --- | --- |
| HTTP Method | HTTP request method. \(目前支援GET, POST, PUT, DELETE\) |
| Waiting Time | HTTP request waiting time. \(Dafault: 30, Unit: second\) |
| URL | Target API URL. |
| Parameters | HTTP request parameters \(Query string\). |
| Headers | HTTP request headers. |
| Body | HTTP request body. \(Only POST, PUT, DELETE\) |

### 

### 增加 Webhook

以GET為例:

PARAMETERS設定: 加入desc=false, count=1000, 和index=1.



![](/assets/webhook_get1.PNG)

HEADER設定: 加入 Authorization

![](/assets/webhook_get2.PNG)



