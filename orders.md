## Заявки на оформление заказа

**Метод:** POST  
**URL:** /orders

Создание заявки пользователя на оформление заказа.

Пример запроса: https://educube.ru/orders/

Request:

```
[
    "name": "string",
    "email": "string",
    "phone_number": "string",
]

```

Response:  
201 - created;
```
[
    "id": int,
    "status": "string",
    "created_at": "string",
]
```

**Errors:**  
400 - not found;  

422 - unprocessable Entity;  
500 - server error;

