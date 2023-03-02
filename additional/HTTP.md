# HTTP

## URL (aka URI)

URL идва от Universal Resource Locator. Дефиниран е в стандарт [RFC 3986](https://tools.ietf.org/html/rfc3986).

URLа се декомпозира на следните части:    
`protocol://host[:port][/path][?query][#fragment]`

Например:      
`https://www.google.bg/search?q=test`    
`http://localhost:8080/servlet-jsp-demo/welcome?name=web+programming-course`

## HTTP

HTTP идва от Hypertext Transfer Protocol. Дефиниран е в стандарт [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)

HTTP протокола може да се опише като:
- клиент/сървър (client/server) - клиента е активната част. Праща заявки, сървъра отговаря
- заявка/отговор (request/response) - клиента праща заявки, сървъра отговаря
- текстов - заявката и отговора предствляват текстови съобщения
- stateless - всяка двойка заявка и отговор е независими една от друга. С помоща на cookies е възможно да се подържа сесия и заявките да споделят информация (състояние)

Заявката се декомпозира по следният начин:
```
POST /api/courses HTTP/1.1
Host: localhost
Accept: application/json
Content-type: application/json;charset=UTF-8
CRLF
{ course: 'Web programming course" }
```
Първият ред наречен request line е съставен от:
* метод - `POST`
* път - `/api/courses`
* версия - `HTTP/1.1`

Най-използваните методи са:
* `GET`
* `POST`
* `PUT`
* `PATCH` - ново дефиниран метод за целите на комуникация в REST стил
* `DELETE`

Следват header-и във формата `име: стойност`. Най-често срещаните са:
* `Host` - показва host-а към който е адресирана заявката
* `Accept` - индикира форматите които клиента който изпраща заявката разбира или очаква
* `Content-type` - за заявките които имат съдуржание (message body) показва типа на съдържанието и евентуално encoding-а ако е текстов тип

Отговора има сходна структира:
```
HTTP/1.1 201 Created
Location: http://localhost:8080/api/courses/123
Content-type: application/json;charset=UTF-8
CRLF
{ id: 123, course: 'Web programming course" }
```
Първият ред наречен status line е съставен от:
* версия - `HTTP/1.1`
* статус код - `201`
* статус фраза - `Created`

Възможните статус кодове са дефинирани във стандарта и се разделят в 5 големи групи. За целите на нащият курс интерес представляват:
* 2xx - кодове индикиращи успешно обработена заявка. По известни са `200 OK`, `201 Created` и `204 No Content`
* 3xx - по-специално тук значение има 302 Temporary Moved, който се използва в комбинация с Location хедъра. По този начин сървъра може да накара browser-a да зареди друга страниця. Известен още като client side redirect
* 4xx - кодове индикиращи проблем в заявката на клиента. Най-известния код е `404 Not Found`. Други често срещани са `400 Bad Request`, `401 Unauthorized` и `403 Forbidden`
* 5xx - кодове индикиращи проблем от страната на сървъра. Любимият на всички програмисти е `500 Internal Server Error`

Другата част от отговора не се отличава съществено от структурата на заявката, а имено хедъри и евентуално съдържание.

# REST

[REST](https://en.wikipedia.org/wiki/Representational_state_transfer) е сравнително нова концепция за реализиране на web услуги (web services) използващи максимално функционалноста на HTTP протокола, т.е. методите предоставени от HTTP (`GET`, `POST`, `PUT`, etc.) приложени върху ресурси (URL).

За сравнение SOAP web услугите използват само `POST` метод към определен URL, като описанието на действието и даните за него са част от съдържанието на заявката.

Съответствието на така нареяените CRUD (create, read, update, delete) операции в REST е както следва:
* Create - `POST`
* Read - `GET`
* Update - `PUT` или `PATCH` ([idempotent](http://javarevisited.blogspot.bg/2016/05/what-are-idempotent-and-safe-methods-of-HTTP-and-REST.html))
* Delete - `DELETE`

Кратко въведение в REST може да се намери [тук](https://www.infoq.com/articles/rest-introduction)