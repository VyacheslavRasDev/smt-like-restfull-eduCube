## Роуты
GET '/register' - отображение страницы регистрации   
POST '/register' - запрос на регистрацию пользователя

## Страница регистрации

**Метод:** GET  
**URL:** /register

Пример запроса:  
https://educube.ru/register  

Response:  
200  
404   
500
----------
## Запрос на регистрацию пользователя

**Метод:** POST  
**URL:** /register

Пример запроса:  
https://educube.ru/register  

**Request** 
```
{
    "name": "Ivanov Ivan Ivanovich",
    "login": "IvanVan",
    "email": "ivan@example.com",
    "password": "*********",
    "password_confirmation": "*********"
}
```

**Response**  
201
```
{
    "status": "success",
    "data": {
        "user": {
            "id": 15,
            "name": "Ivanov Ivan Ivanovich",
            "login": "IvanVan",
            "email": "ivan@example.com",
            "created_at": "2023-10...."
        },
        "token": "..."
    }
}
```
Errors:  
404   
422   
400   
500


