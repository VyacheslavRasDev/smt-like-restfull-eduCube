## Роуты
GET '/sessions' - отображение страницы авторизации   
POST '/sessions' - запрос на авторизацию пользователя
DELETE '/sessions' - запрос на прекращение сессии

## Страница авторизации

**Метод:** GET
**URL:** /sessions

Пример запроса:  
https://educube.ru/sessions

**Response:**
200

**Errors**  
404    
500
------
## Запрос на авторизацию пользователя

**Метод:** POST 
**URL:** /sessions

Пример запроса:  
https://educube.ru/sessions  

**Request** 
```
{
  "login": "IvanVan", 
  "password": "********",
  "remember": true
}
```

**Response**  
```
{
    "status": "success",
    "user": {
        "id": 15,
        "name": "Ivan Ivanov",
        "login": "IvanVan",
        "email": "ivan@example.com",
        "created_at": "2023-10...."
    },
    "token": "..."
}
```
200;

**Errors**  
401  
422
```
{
  "message": "Invalid ..." 
  "errors: {
    "email": "Invalid..."
  }
}
```
----------
## Запрос на прекращение сессии
**Метод:** POST (DELETE)
**URL:** /sessions

Пример запроса:  
https://educube.ru/sessions

Определяет пользователя по токену и завершает сессию.

**Response**
200

```
{
    "status": "success",
    "message": "Successfully logged out"
}
```
**Errors**   
401




