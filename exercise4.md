**Тестирование API с Postman**  
# Activities #     
## 1. GET /api​/v1​/Activities
- URL: {{URL_API}}/Activities
- Ожидаемый результат: вывод всех активностей.
- Заголовки запроса:
```
Accept: text/plain
User-Agent: PostmanRuntime/7.32.3
Cache-Control: no-cache
Postman-Token: 4ef39ac5-601d-4b93-b853-8011fe95af38
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive 
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:50:47 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
[
    {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-09-07T05:50:47.6423353+00:00",
        "completed": false
    },
    {
        "id": 2,
        "title": "Activity 2",
        "dueDate": "2023-09-07T06:50:47.6423375+00:00",
        "completed": true
    },...]
```
## 2. GET /api/v1/Activities/{id}
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: вывод активности с заданным activity_id.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 12c4e820-2ab5-4311-bab2-3f3c3504b455
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:58:40 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 10,
    "title": "Activity 10",
    "dueDate": "2023-09-07T14:58:40.4066794+00:00",
    "completed": true
}
```
## 3. POST /api/v1/Activities
- URL: {{URL_API}}/Activities
- Ожидаемый результат: создание и вывод новой активности с заданным телом.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b8332f72-0746-417b-844f-f748838f16e8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 6,
  "title": "string",
  "dueDate": "2023-09-05T11:37:10.836Z",
  "completed": true
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:00:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 6,
    "title": "string",
    "dueDate": "2023-09-05T11:37:10.836Z",
    "completed": true
}
```
## 4. PUT /api/v1/Activities/{id}
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: редактирование и вывод активности с заданным телом и activity_id.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: da69a663-0a7a-48fc-91c7-443966ed8479
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-09-05T02:20:08.768Z",
  "completed": true
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:12:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-09-05T02:20:08.768Z",
    "completed": true
}
```
## 5. DELETE /api/v1/Activities/{id}
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: удаление активности с заданным activity_id.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 57fe00e9-55d5-47be-b016-62b948232695
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса: отсутствует.
- Заголовки ответа:
```
Content-Length: 0
Date: Thu, 07 Sep 2023 05:13:25 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: отсутствует.
# Authors # 
## 1. GET /api/v1/Authors
- URL: {{URL_API}}/Authors  
- Ожидаемый результат: отображение списка всех существующих в системе авторов  
- Заголовки запроса: 
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2c90757c-1a12-4716-b8c6-ab259a40025d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса - отсутствует
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 01:26:13 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },
    ...
        {
        "id": 606,
        "idBook": 200,
        "firstName": "First Name 606",
        "lastName": "Last Name 606"
    }
]
```
## 2. POST /api/v1/Authors
- URL: {{URL_API}}/Authors  
- Ожидаемый результат: создание нового автора  
- Заголовки запроса: 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 8ab65b58-0856-4aec-8dd4-d0cf4d9e4b66
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: 
```
{
    "id": 3,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 01:44:59 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 3,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
}
```

## 3. GET /api/v1/Authors/authors/books/{idBook}
- URL: {{URL_API}}/Authors/authors/books/{{books_id}}
- Ожидаемый результат: вывод данных об авторе с заданным books_id книги.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 51a50132-9ad2-448a-a4b4-e401c0c09bbe
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 17:12:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
[
    {
        "id": 11,
        "idBook": 4,
        "firstName": "First Name 11",
        "lastName": "Last Name 11"
    },
    {
        "id": 12,
        "idBook": 4,
        "firstName": "First Name 12",
        "lastName": "Last Name 12"
    }
]
```
## 4. GET /api/v1/Authors/{id}
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: вывод данных об авторе с заданным authors_id.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3f7f67a0-88c1-4621-95dd-e51ad78e910c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 17:15:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 3,
    "idBook": 2,
    "firstName": "First Name 3",
    "lastName": "Last Name 3"
}
```
## 5. PUT /api/v1/Authors/{id}  
- URL: {{URL_API}}/Authors/{{authors_id}} 
- Ожидаемый результат: редактирование и вывод данных об авторе с заданным телом и authors_id.
- Заголовки запроса:  
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 25076347-17c6-4eb8-a06b-515eca2349bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 17:17:27 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
}
```
## 6. DELETE /api/v1/Authors/{id}  
- URL: {{URL_API}}/Authors/{{authors_id}}  
- Ожидаемый результат: удаление данных об авторе с заданным authors_id.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 8532e6c8-197c-42a1-bf8f-54e1fc6f1e40
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует.  
- Заголовки ответа:  
```
Content-Length: 0
Date: Thu, 07 Sep 2023 17:19:06 GMT
Server: Kestrel
api-supported-versions: 1.0
```
# Books # 
## 1. GET​/api​/v1​/Books
- URL: {{URL_API}}/Books  
- Ожидаемый результат: отображается список всех существующих в системе книг  
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b38007ce-3484-4652-8a8e-3c56e6c1948f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive  
```  
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```  
- Тело ответа:  
```
    {
        "id": 1,
        "title": "Book 1",
        "description": "Diam accumsan esse labore sit autem commodo et duo voluptua. Sed accusam ut lorem sed duis dolore dolores.\n",
        "pageCount": 100,
        accusam feugiat lorem blandit.\n",
        "publishDate": "2023-02-19T04:14:01.3327479+00:00"
    }
```  
## 2. POST​/api​/v1​/Books
- URL: {{URL_API}}/Books  
- Ожидаемый результат: создание и вывод новой книги с заданным телом в теле ответа.  
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive   
```
- Тело запроса:  
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:  
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "title": null,
    "description": null,
    "pageCount": 0,
    "excerpt": null,
    "publishDate": "0001-01-01T00:00:00"
}
```
## 3. GET​/api​/v1​/Books​/{id}  
- URL: {{URL_API}}Books/{{books_id}}  
- Ожидаемый результат: вывод книги с заданным books_id в теле ответа.  
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive  
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```  
- Тело ответа: 
```
 {
 "id": 3,
    "title": "Book 3",
    "description": "Vero sadipscing stet dolor odio feugiat. No tempor sed nonumy. Nobis dolor ea wisi tempor. . Lorem magna consetetur minim lorem gubergren qui.\n",
    "pageCount": 300,
    "excerpt": "Amet sanctus nonumy dolore rebum dolor congue justo duis clita ut et dolores euismod gubergren amet luptatum.
    }
```
## 4. PUT​/api​/v1​/Books​/{id}
- URL: {{URL_API}}/Books/{{books_id}}  
- Ожидаемый результат: редактирование и вывод книги с заданным телом и books_id в теле ответа.  
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```  
- Заголовки ответа:  
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "title": null,
    "description": null,
    "pageCount": 0,
    "excerpt": null,
    "publishDate": "0001-01-01T00:00:00"
}
```
## 5. DELETE​/api​/v1​/Books​/{id}  
- URL: {{URL_API}}/Books/{{books_id}}  
- Ожидаемый результат: удаление книги с заданным books_id.  
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:  
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
# CoverPhotos #    
## 1. GET /api/v1/CoverPhotos
- URL: {{URL_API}}/CoverPhotos
- Ожидаемый результат: вывод всех данных о фото.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6521e181-6c6d-4273-8f9a-730323509f26
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive 
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:25:59 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    {
        "id": 2,
        "idBook": 2,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
    },...]
```
## 2. POST /api/v1/CoverPhotos
- URL: {{URL_API}}/CoverPhotos
- Ожидаемый результат: создание и вывод данных о новом фото.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7d3c2400-572f-4c60-9899-618c4ad4b35c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:27:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "url": "string"
}
```
## 3. GET /api/v1/CoverPhotos/books/covers/{idBook}
- URL: {{URL_API}}/CoverPhotos/books/covers/{{books_id}}
- Ожидаемый результат: вывод данных о фото книги с заданным books_id.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ddb3c9f5-a6cd-4663-a98f-49f846c1ef06
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:32:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
[
    {
        "id": 10,
        "idBook": 10,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 10&w=250&h=350"
    }
]
```
## 4. GET /api/v1/CoverPhotos/{id}
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: вывод данных о фото с заданным CoverPhotos_id.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a9dc314b-19bd-48f0-8be5-32ff906fc5d5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:34:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 11,
    "idBook": 11,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 11&w=250&h=350"
}
```
## 5. PUT ​/api​/v1​/CoverPhotos/{id}  
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}} 
- Ожидаемый результат: редактирование и вывод данных о фото с заданным телом и CoverPhotos_id.
- Заголовки запроса:  
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0d6fe313-f142-41bc-94f9-cddaf5a3213c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 16:55:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```
## 6. DELETE ​/api​/v1​/CoverPhotos/{id}  
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}  
- Ожидаемый результат: удаление данных о фото с заданным CoverPhotos_id.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0a1befed-467b-4707-a6c3-6a72d9571109
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса: отсутствует.  
- Заголовки ответа:  
```
Content-Length: 0
Date: Thu, 07 Sep 2023 17:02:50 GMT
Server: Kestrel
api-supported-versions: 1.0
```
# Users #
## 1. GET​/api​/v1​/Users  
- URL: {{URL_API}}/Users    
- Ожидаемый результат: вывод всех пользователей.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive  
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
[
    {
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
    },
    {
        "id": 2,
        "userName": "User 2",
        "password": "Password2"
    },
    ]
```
## 2. POST​/api​/v1​/Users  
- URL: {{URL_API}}/Users  
- Ожидаемый результат: создание и вывод нового пользователя с заданным телом.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:  
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```
## 3. GET​/api​/v1​/Users​/{id}   
- URL: {{URL_API}}/Users/{{users_id}}    
- Ожидаемый результат: вывод данных о пользователе с заданным users_id в теле ответа.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 16730567-a547-4018-b8ce-7c00b80ef6df
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 16:30:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 2,
    "userName": "User 2",
    "password": "Password2"
}
```
## 4. PUT​/api​/v1​/Users​/{id}  
- URL: {{URL_API}}/Users/{{users_id}}  
- Ожидаемый результат: редактирование и вывод данных о пользователях с заданным телом и users_id.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```
## 5. DELETE​/api​/v1​/Users​/{id}  
- URL: {{URL_API}}/Users/{{users_id}}  
- Ожидаемый результат: удаление пользователя с заданным users_id.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:  
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
# *Негативное тестирование.*
## Activities
### 1. Activities.POST - ввод неверного типа поля в тело запроса.
- URL: {{URL_API}}/Activities  
- Ожидаемый результат: ошибка создания активности при вводе неверного типа поля в тело запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b8f49b71-a834-4b95-bb2f-7c0203b84f9d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
 {
  "id": "string",
  "title": "string",
  "dueDate": "2023-09-03T04:02:57.169Z",
  "completed": true
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 07 Sep 2023 11:56:27 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8a4ad66b6a591c44be467b2a9812ee5a-739af5e0af861e44-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 16."
        ]
    }
}
```
### 2. Activities.POST - ввод тела запроса с допущенной синтаксической ошибкой.
- URL: {{URL_API}}/Activities
- Ожидаемый результат: ошибка создания активности при вводе тела запроса с допущенной синтаксической ошибкой.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 042ffbd4-4dbd-499b-b915-cee339e44c34
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
"id": 0,
  "title": "string",
  "dueDate": "2023-09-03T04:02:57.169Z",
  "completed": true
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 07 Sep 2023 11:59:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a8f74c306c45334c95a268f58188b32f-644e6f74f71c2646-00",
    "errors": {
        "$": [
            "The JSON value could not be converted to FakeRestAPI.Models.Activity. Path: $ | LineNumber: 0 | BytePositionInLine: 4."
        ]
    }
}
```
### 3. Activities.POST - ввод пустого тела запроса.
- URL: {{URL_API}}/Activities
- Ожидаемый результат: создание пустой активности.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 042ffbd4-4dbd-499b-b915-cee339e44c34
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Thu, 07 Sep 2023 11:59:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "id": 0,
    "title": null,
    "dueDate": "0001-01-01T00:00:00",
    "completed": false
}
```
### 4. Activities.GET.{id} - ввод в activity_id отрицательного числа.
- URL: {{URL_API}}/Activities/{{activity_id}}  
- Ожидаемый результат: ошибка получения активности при вводе в activity_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0cb679c7-13bd-4bdd-aaa8-7dfd6c12e6c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 12:11:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-1887faf555bc3944b936bfb33afd9813-01cc29d6bc32214e-00"
}
```
### 5. Activities.GET.{id} - ввод в activity_id числа больше 8 разрядов.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: ошибка получения активности при вводе в activity_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0cb679c7-13bd-4bdd-aaa8-7dfd6c12e6c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 12:11:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3641f32f8dcaf74c922a2198326bebf7-88a540222ff4d944-00",
    "errors": {
        "id": [
            "The value '123456789456123' is not valid."
        ]
    }
}
```
### 6. Activities.PUT.{id} - ввод в activity_id отрицательного числа.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: ошибка редактирования активности при вводе в activity_id отрицательного числа.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: da69a663-0a7a-48fc-91c7-443966ed8479
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-09-05T02:20:08.768Z",
  "completed": true
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:12:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-09-05T02:20:08.768Z",
    "completed": true
}
```
### 7. Activities.PUT.{id} - ввод в activity_id числа больше 8 разрядов.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: ошибка редактирования активности при вводе в  activity_id числа больше 8 разрядов.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: da69a663-0a7a-48fc-91c7-443966ed8479
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-09-05T02:20:08.768Z",
  "completed": true
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:12:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8e44b1c855a7764db762e1cc7cd8f289-435989326ba14b4a-00",
    "errors": {
        "id": [
            "The value '123456789456123' is not valid."
        ]
    }
}
```
### 8. Activities.PUT.{id} - ввод неверного типа поля в тело запроса.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: ошибка при вводе неверного типа поля в тело запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: da69a663-0a7a-48fc-91c7-443966ed8479
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "title": "string",
  "dueDate": "2023",
  "completed": true
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:12:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6b8e22ca855e89429860a093e7644562-fadccbf0bcb2274a-00",
    "errors": {
        "$.dueDate": [
            "The JSON value could not be converted to System.DateTime. Path: $.dueDate | LineNumber: 3 | BytePositionInLine: 19."
        ]
    }
}
```
### 9. Activities.PUT.{id} - ввод тела запроса с допущенной синтаксической ошибкой.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: ошибка редактирования активности при вводе тела запроса с допущенной синтаксической ошибкой.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: da69a663-0a7a-48fc-91c7-443966ed8479
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "title": "string",
  "dueDate": "2023",
  "completed": true,
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:12:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8e5d6bc71d06fc4289cc5d1642e6317a-6c6ea4387af3ae4f-00",
    "errors": {
        "$.dueDate": [
            "The JSON value could not be converted to System.DateTime. Path: $.dueDate | LineNumber: 3 | BytePositionInLine: 19."
        ]
    }
}
```
### 10. Activities.PUT.{id} - ввод пустого тела запроса.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: вставка пустых значений.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: da69a663-0a7a-48fc-91c7-443966ed8479
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:12:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "title": null,
    "dueDate": "0001-01-01T00:00:00",
    "completed": false
}
```
### 11. Activities.DELETE.{id} - ввод в activity_id числа больше 8 разрядов.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: ошибка удаления активности при вводе в activity_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 57fe00e9-55d5-47be-b016-62b948232695
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса: отсутствует.
- Заголовки ответа:
```
Content-Length: 0
Date: Thu, 07 Sep 2023 05:13:25 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: 
``` 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-07e14a3203a1e746bdd8b2f870e2f578-a3e84806d89a994f-00",
    "errors": {
        "id": [
            "The value '456789456123465' is not valid."
        ]
    }
}
``` 
### 12. Activities.DELETE.{id} - ввод в activity_id отрицательного числа.
- URL: {{URL_API}}/Activities/{{activity_id}}
- Ожидаемый результат: ошибка удаления активности при вводе в activity_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 57fe00e9-55d5-47be-b016-62b948232695
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса: отсутствует.
- Заголовки ответа:
```
Content-Length: 0
Date: Thu, 07 Sep 2023 05:13:25 GMT
Server: Kestrel
api-supported-versions: 1.0
```
## Authors
### 1. Authors.POST - ввод неверного типа поля в тело запроса
- URL: {{URL_API}}/Authors
- Ожидаемый результат: ошибка создания автора при вводе ошибочного типа поля в теле запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b7ac77c7-f142-4bda-9325-b8c4b4922b70
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": "string",
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 16:13:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-87fa727fedd21544b4b113aa399f326d-657578d3ea561649-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 16."
        ]
    }
}
```
### 2. Authors.POST - ввод тела с допущенной синтаксической ошибкой
- URL: {{URL_API}}/Authors
- Ожидаемый результат: ошибка при создании автора с допущенной синтаксической ошибкой в описании тела запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 49c1c02e-fd74-410c-ad66-b0e4744bf8d9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
"id": 0,
"idBook": 0
"firstName": "string",
"lastName": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 16:15:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-af99623ee8eee24ca94f495f9c59d04a-dc7556e4c547ff4a-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 0."
        ]
    }
}
```
### 3. Authors.POST - ввод пустого тела запроса
- URL: {{URL_API}}/Authors
- Ожидаемый результат: создание автора с незаполненным телом запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 490fe57e-55eb-4c8e-b621-aeca0bac1ae0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 08 Sep 2023 16:19:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "firstName": null,
    "lastName": null
}
```
### 4. Authors.GET.{idBook}  - ввод в books_id отрицательного числа
- URL: {{URL_API}}/Authors/authors/books/{{books_id}}
- Ожидаемый результат: ошибка вывода данных об авторе при вводе в books_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e1a9cb49-b567-4647-914e-dbfea30f738a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 16:39:06 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
[
]
```
### 5. Authors.GET.{idBook} - ввод в books_id числа больше 8 разрядов
- URL: {{URL_API}}/Authors/authors/books/{{books_id}}
- Ожидаемый результат: ошибка вывода данных об авторе при вводе в books_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0cb679c7-13bd-4bdd-aaa8-7dfd6c12e6c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 12:11:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3641f32f8dcaf74c922a2198326bebf7-88a540222ff4d944-00",
    "errors": {
        "id": [
            "The value '123456789456123' is not valid."
        ]
    }
}
```
### 6. Authors.GET.{id}  - ввод в authors_id отрицательного числа
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка вывода данных об авторе при вводе в authors_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: bf6b1ae4-92a2-412b-9953-19b0fc2b40a7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 16:48:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-285d81759a3f814d873b041f74c000fd-4f42f0d3babdd341-00"
}
```
### 7. Authors.GET.{id} - ввод в authors_id числа больше 8 разрядов
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка вывода данных об авторе при вводе в authors_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 43653f85-5016-4745-8954-c2a56e3db617
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 16:49:59 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-ccfb403c35ad494ebdbcd6b3a812ea21-be482c07e12d6a48-00"
}
```
### 8. Authors.PUT.{id} - ввод в authors_id отрицательного числа.
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка редактирования автора при вводе в authors_id отрицательного числа.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9d9067db-7886-4209-ad32-ffed6a2b4bd1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 17:02:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
### 9. Authors.PUT.{id} - ввод в authors_id числа больше 8 разрядов.
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка редактирования автора при вводе в authors_id числа больше 8 разрядов.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9d9067db-7886-4209-ad32-ffed6a2b4bd1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 17:02:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
### 10. Authors.PUT.{id} - ввод неверного типа поля в тело запроса.
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка редактирования автора при вводе неверного типа поля в тело запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 972cfcfa-9c98-4588-b89b-eeb1a025d8ec
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "idBook": 0,
  "firstName": 0,
  "lastName": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 09 Sep 2023 17:07:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-905068ae8767674d811224a5efff7641-dd348186f0384647-00",
    "errors": {
        "$.firstName": [
            "The JSON value could not be converted to System.String. Path: $.firstName | LineNumber: 3 | BytePositionInLine: 16."
        ]
    }
}
```
### 11. Authors.PUT.{id} - ввод тела запроса с допущенной синтаксической ошибкой.
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка редактирования автора при вводе тела запроса с допущенной синтаксической ошибкой.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e23c3f02-0243-4767-836f-cf28d8b23e39
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "idBook": 0,,
  "firstName": "string",
  "lastName": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 09 Sep 2023 17:10:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-7bcb82596fe06b45a5ae57a4e82a1f92-af7f8f714df17047-00",
    "errors": {
        "$": [
            "',' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 2 | BytePositionInLine: 14."
        ]
    }
}
```
### 12. Authors.PUT.{id} - ввод пустого тела запроса.
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: редактирование автора с пустым телом запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3d603523-d4e7-4c32-a735-6c2cfdf273ba
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 17:15:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "firstName": null,
    "lastName": null
}
```
### 13. Authors.DELETE.{id} - ввод в authors_id числа больше 8 разрядов.
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка удаления автора при вводе в authors_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b0e67b6c-2a3f-488f-a122-2585f0f5d483
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса: отсутствует.
- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 09 Sep 2023 17:19:15 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: отсутствует.
### 12. Authors.DELETE.{id} - ввод в authors_id отрицательного числа.
- URL: {{URL_API}}/Authors/{{authors_id}}
- Ожидаемый результат: ошибка удаления автора при вводе в authors_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: fbabaf6f-ab67-430c-984c-19ebbcdd6433
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса: отсутствует.
- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 09 Sep 2023 17:18:26 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: отсутствует.
## CoverPhotos
### 1. CoverPhotos.POST - ввод неверного типа поля в тело запроса.
- URL: {{URL_API}}/CoverPhotos
- Ожидаемый результат: ошибка создания записи о фото при вводе неверного типа поля в тело запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7d3c2400-572f-4c60-9899-618c4ad4b35c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
```
{
  "id": 0,
  "idBook": 0,
  "url": 0
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:27:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-c502b67371bae94d85c7ffacc88c1b2c-4d73072dd5462545-00",
    "errors": {
        "$.url": [
            "The JSON value could not be converted to System.Uri. Path: $.url | LineNumber: 3 | BytePositionInLine: 10."
        ]
    }
}
```
### 2. CoverPhotos.POST - ввод тела запроса с допущенной синтаксической ошибкой.
- URL: {{URL_API}}/CoverPhotos
- Ожидаемый результат: ошибка создания записи о фото при вводе тела запроса с допущенной синтаксической ошибкой.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7d3c2400-572f-4c60-9899-618c4ad4b35c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
```
 {
  "id": 0,
  "idBook": 0
  "url": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:27:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e3dd970b46df0b4f9b7dfd8afe84b3c1-c941aa2babebd14d-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 2."
        ]
    }
}
```
### 3. CoverPhotos.POST - ввод пустого тела запроса.
- URL: {{URL_API}}/CoverPhotos
- Ожидаемый результат: создание пустой записи о фото.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7d3c2400-572f-4c60-9899-618c4ad4b35c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
```
{
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:27:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "url": null
}
```
### 4. CoverPhotos.GET.{idBook} - ввод в books_id отрицательного числа.
- URL: {{URL_API}}/CoverPhotos/books/covers/{{books_id}}
- Ожидаемый результат: ошибка получения данных при вводе в books_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ddb3c9f5-a6cd-4663-a98f-49f846c1ef06
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:32:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
[
]
```
### 5. CoverPhotos.GET.{idBook} - ввод в books_id числа больше 8 разрядов.
- URL: {{URL_API}}/CoverPhotos/books/covers/{{books_id}}
- Ожидаемый результат: ошибка получения данных при вводе в books_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ddb3c9f5-a6cd-4663-a98f-49f846c1ef06
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:32:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-20ca6f597582924a976f9518bb458b9e-059d08e4f7f8664e-00",
    "errors": {
        "idBook": [
            "The value '123456789456123' is not valid."
        ]
    }
}
```
### 6. CoverPhotos.GET.{id} - ввод в CoverPhotos_id отрицательного числа.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка получения данных при вводе в CoverPhotos_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a9dc314b-19bd-48f0-8be5-32ff906fc5d5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:34:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-05de45ce6fb7bf43a79e41d730de31f7-4ddc1a36f96c064c-00"
}
```
### 7. CoverPhotos.GET.{id} - ввод в CoverPhotos_id числа больше 8 разрядов.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка получения данных при вводе в CoverPhotos_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a9dc314b-19bd-48f0-8be5-32ff906fc5d5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса - отсутствует.
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 05:34:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5ad114614e1cc44481c8548dd64dd0ee-e2708afd69760d4f-00",
    "errors": {
        "id": [
            "The value '123456789456123' is not valid."
        ]
    }
}
```
### 8. CoverPhotos.PUT.{id} - ввод в CoverPhotos_id отрицательного числа.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка редактирования данных о фото при вводе в CoverPhotos_id отрицательного числа.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: fcd00982-3eed-426e-bfb2-10a831dbbdb3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 17:26:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "url": "string"
}
```
### 9. CoverPhotos.PUT.{id} - ввод в CoverPhotos_id числа больше 8 разрядов.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка редактирования данных о фото при вводе в CoverPhotos_id числа больше 8 разрядов.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 4b4589d3-6852-4a06-b1da-2bd448cefc8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
    "id": 0,
    "idBook": 0,
    "url": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 17:27:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "url": "string"
}
```
### 10. CoverPhotos.PUT.{id} - ввод неверного типа поля в тело запроса.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка редактирования данных о фото при вводе неверного типа поля в тело запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: acae4cd7-766e-4258-aa3f-6fd1f04f3be7
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,
  "idBook": "string",
  "url": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 09 Sep 2023 17:28:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3341cbedf5178d489ea731afce9fa5ad-d77491ee2bc30042-00",
    "errors": {
        "$.idBook": [
            "The JSON value could not be converted to System.Int32. Path: $.idBook | LineNumber: 2 | BytePositionInLine: 20."
        ]
    }
}
```
### 11. CoverPhotos.PUT.{id} - ввод тела запроса с допущенной синтаксической ошибкой.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка редактирования данных о фото при вводе тела запроса с допущенной синтаксической ошибкой.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 5ecbdf29-bcb0-4b6a-85ee-ea1c7abb17ab
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
  "id": 0,-
  "idBook": 0,
  "url": "string"
}
``` 
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Sat, 09 Sep 2023 17:29:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f3eb904ef11ae84991c4d3eb94f7afcc-70d10217b9af1c49-00",
    "errors": {
        "$": [
            "'-' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 1 | BytePositionInLine: 10."
        ]
    }
}
```
### 12. CoverPhotos.PUT.{id} - ввод пустого тела запроса.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: редактирование данных о фото с пустым телом запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3d603523-d4e7-4c32-a735-6c2cfdf273ba
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса:
``` 
{
}
``` 
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 09 Sep 2023 17:15:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "idBook": 0,
    "url": null
}
```
### 13. CoverPhotos.DELETE.{id} - ввод в CoverPhotos_id числа больше 8 разрядов.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка удаления данных о фото при вводе в CoverPhotos_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: be732e55-85d3-4052-a6cd-57110e1603fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса: отсутствует.
- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 09 Sep 2023 17:35:31 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: отсутствует.
### 12. CoverPhotos.DELETE.{id} - ввод в CoverPhotos_id отрицательного числа.
- URL: {{URL_API}}/CoverPhotos/{{CoverPhotos_id}}
- Ожидаемый результат: ошибка удаления данных о фото при вводе в CoverPhotos_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9d29e60b-c48f-40f6-b144-00c622ab7760
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
``` 
- Тело запроса: отсутствует.
- Заголовки ответа:
```
Content-Length: 0
Date: Sat, 09 Sep 2023 17:34:02 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: отсутствует.
## Books
### 1. Books.POST ввод неверного типа поля в тело запроса.
- URL: {{URL_API}}/Books
- Ожидаемый результат: ошибка создания книги при вводе неверного типа поля в тело запроса
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "0": "string",
  0: "string"
}
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a9d659ebba253c47bd27de70edc6ac4a-a7eb6754d7cdb04b-00",
    "errors": {
        "$": [
            "'0' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 3 | BytePositionInLine: 2."
        ]
    }
}
```
## 2. Books.POST ввод тела запроса с допущенной синтаксической ошибкой
- URL: {{URL_API}}/Books  
- Ожидаемый результат: ошибка создания книги при вводе тела запроса с допущенной синтаксической ошибкой
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
  "id": 0
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8bcab9d6f4c3e1439a844ec14b14e1c0-eaf4dbf09142344e-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 2."
        ]
    }
}
```
### 3. Books.POST ввод пустого тела запроса  
- URL: {{URL_API}}/Books  
- Ожидаемый результат: создание пустой книги.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "title": null,
    "description": null,
    "pageCount": 0,
    "excerpt": null,
    "publishDate": "0001-01-01T00:00:00"
}
```
### 4. Books.GET.{id} ввод в books_id числа больше 8 разрядов.
- URL: {{URL_API}}Books/{{books_id}}  
- Ожидаемый результат: ошибка получения книги при вводе в activity_id числа больше 8 разрядов.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e637ef0b36df7941a166f32310128383-e0ba61ee0d033143-00",
    "errors": {
        "id": [
            "The value '1000000000000000000' is not valid."
        ]
    }
}
```
### 5. Books.PUT.{id} ввод  Books_id отрицательного числа
- URL: {{URL_API}}/Books/{{books_id}}
- Ожидаемый результат: ошибка получения книги при вводе в books_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "id": 0,
    "title": null,
    "description": null,
    "pageCount": 0,
    "excerpt": null,
    "publishDate": "0001-01-01T00:00:00"
}
```
### 6. Books.PUT.{id} ввод в books_id числа больше 8 разрядов.
- URL: {{URL_API}}/Books/{{books_id}}
- Ожидаемый результат: ошибка редактирования книги при вводе в  books_id числа больше 8 разрядов.
- Заголовки запроса:  
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d20974d-6922-4a10-bf89-268f1082e8bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:  
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 07 Sep 2023 04:14:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-7d826bafb84e184e8979031adf369909-2fc550c6184a3a40-00",
    "errors": {
        "id": [
            "The value '100000000000000000' is not valid."
        ]
    }
}
```
### 7. Books.PUT.{id} ввод неверного типа поля в тело запроса
- URL: {{URL_API}}/Books/{{books_id}}
- Ожидаемый результат:  ошибка при вводе неверного типа поля в тело запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6d9800b0-3e75-4053-aca6-018dc5522035
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0,
  "userName": "jkhdsakdh"
  "password": "543"
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 03:19:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ba82fc4b06285941b2527fae485e7712-848939ecf7e1b046-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 2."
        ]
    }
}
```
### 8. Books.PUT.{id} ввод тела запроса с допущенной синтаксической ошибкой.
- URL: {{URL_API}}/Books/{{books_id}}
- Ожидаемый результат: ошибка редактирования книги при вводе тела запроса с допущенной синтаксической ошибкой.
- Заголовки запроса:  
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b67658e4-fb73-4f1c-bb8d-c18a097a66b0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
  "id": 0
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:  
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 03:26:22 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-309fa60921228b4a938d7d540a7f370e-acba07863c28cd4f-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 2."
        ]
    }
}
```
### 9. Books.PUT.{id}  ввод пустого тела запроса
- URL: {{URL_API}}/Books/{{books_id}}
- Ожидаемый результат: вставка пустых значений
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 84942201-8d20-41c8-a9fb-86fc045e6caa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 08 Sep 2023 03:33:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "title": null,
    "description": null,
    "pageCount": 0,
    "excerpt": null,
    "publishDate": "0001-01-01T00:00:00"
}
```
### 10. Books.DELETE.{id} ввод в books_id числа больше 8 разрядов.
- URL: {{URL_API}}/Books/{{books_id}}
- Ожидаемый результат: ошибка удаления активности при вводе в books_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 215a6749-be04-4bc4-bff6-30a52b705785
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:  
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 03:39:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-cdb2068e45ed8d4a95ef8ed516bf6b0f-82c265925aa39e4a-00",
    "errors": {
        "id": [
            "The value '1000000000000' is not valid."
        ]
    }
}
```
### 11. Books.DELETE.{id} ввод в Books_id отрицательного числа.
- URL: {{URL_API}}/Books/{{books_id}}
- Ожидаемый результат: ошибка удаления книги при вводе в books_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c8ba308f-2d29-43cb-a239-23fbf2b38507
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:  
```
Content-Length: 0
Date: Fri, 08 Sep 2023 03:45:42 GMT
Server: Kestrel
api-supported-versions: 1.0
```
##  Users ##
### 1. Users.GET.{id} ввод в users_id отрицательного числа.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка получения пользователя при вводе в users_id отрицательного числа.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 487f5c01-34f4-4166-9467-273afcdbf889
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Fri, 08 Sep 2023 03:59:46 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-00d86a347965a4418650df4a035f7b36-880f78dbcb8b454d-00"
}
```
### 2. Users.GET.{idBook}ввод в users_id числа больше 8 разрядов.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка получения активности при вводе в users_id числа больше 8 разрядов.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3a8674d3-2b7c-4b05-9620-060dc18271bd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:  
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 04:04:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2eaf8e86f7c22e48b841af4e1322cdfb-0bc7ff6285e6f44d-00",
    "errors": {
        "id": [
            "The value '1000000000000' is not valid."
        ]
    }
}
```
### 3. Users.PUT.{id} ввод в users_id числа больше 8 разрядов.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка редактирования активности при вводе в  users_id числа больше 8 разрядов.
- Заголовки запроса:  
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b59f11c3-b63e-4c9c-815b-a86189455388
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело ответа:  
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:
```
Content-Length: 0
Date: Fri, 08 Sep 2023 03:45:42 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0f36f4cf3faf234ca5781bd026f2e916-c4f722ec13089748-00",
    "errors": {
        "id": [
            "The value '1000000000000' is not valid."
        ]
    }
}
```
### 4. Users.PUT.{id} ввод в users_id отрицательного числа.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка редактирования пользователя при вводе в users_id отрицательного числа.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 77e8da82-deca-4ccf-9b12-c7e794321708
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 08 Sep 2023 04:18:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```
### 5. Users.PUT.{id}  ввод в users_id числа больше 8 разрядов.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка редактирования пользователя при вводе в  users_id числа больше 8 разрядов.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 97e24981-6d63-4613-8316-9f66eb30ceac
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:  
```
{
dfsdfsdf

  "0": "0"
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 04:26:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8cd2e4e93398a645a8c5d01e15e25a42-c2930dd687ccfe4c-00",
    "errors": {
        "$": [
            "'d' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 1 | BytePositionInLine: 0."
        ]
    }
}
```
### 6. Users.PUT.{id} ввод неверного типа поля в тело запроса.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка при вводе неверного типа поля в тело запроса.
- Заголовки запроса:
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
```
- Тело ответа:  
```
{
  "id": 0
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 04:32:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ecb6aa56d6ab344986ca1aa8ef3cdd56-59c242612616cf42-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 2."
        ]
    }
}
```
### 7. Users.PUT.{id} ввод тела запроса с допущенной синтаксической ошибкой.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка редактирования активности при вводе тела запроса с допущенной синтаксической ошибкой
- Заголовки запроса:  
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d8aabf72-3b19-46bc-884c-cdaeeda709e4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса:
```
{
}
```
- Заголовки ответа:
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Fri, 08 Sep 2023 04:38:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "userName": null,
    "password": null
}
```
### 8. Users.DELETE.{id} негативный(большое число)
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка удаления пользователя.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a474ec1e-03de-4e2a-995b-baeefd683b92
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Заголовки ответа:
```
Content-Type: application/problem+json; charset=utf-8
Date: Fri, 08 Sep 2023 04:47:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-dd82f77a7685364a8bc7a5f51257904b-18e30a600c086a49-00",
    "errors": {
        "id": [
            "The value '10000000000000' is not valid."
        ]
    }
}
```
### 9. Users.DELETE.{id} ввод в users_id отрицательного числа.
- URL: {{URL_API}}/Users/{{users_id}}
- Ожидаемый результат: ошибка удаления пользователя.
- Заголовки запроса:
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f03d5532-270b-4c0f-96c0-65255e2eac79
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- Заголовки ответа:
```
Content-Length: 0
Date: Fri, 08 Sep 2023 04:53:32 GMT
Server: Kestrel
api-supported-versions: 1.0
```