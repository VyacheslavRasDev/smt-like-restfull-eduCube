## Роуты  
GET '/orders' - страница заказов пользователя     
GET '/orders/{id}' - просмотр одного заказа     
POST '/orders' - запрос на создание заказа   
POST '/orders/{id}' - запрос на отмену заказа (изменение статуса)

## Запрос на создание заказа

**Метод:** POST  
**URL:** /orders

Создание заказа на основе текущей корзины:
- для гостя;
- для пользователя.

Пример запроса: https://educube.ru/orders 

## Гость   
**Request:**
```
{
  "customer": {
    "name": "Ivan Ivanov",
    "email": "ivan@example.com",
    "phone": "+7..."
  },
  "items": {
    "product_id": "int",
    "quantity": "int"
  },
  "shipping_address": {
    "country": "string",
    "city": "string",
    "street": "string",
    "house": "int",
    "apartment": "int",
    "postal_code": "int"
  },
  "shipping_method_id": "id",
  "payment_method_id": "int",
  "comment": "Доставка...",
}

```
## Авторизованный пользователь
**Request:**

```
{
  "items": [
    {
      "product_id": "int",
      "quantity": "int"
    }
  ],
  "shipping_method_id": "int",
  "payment_method_id": "int",
  "comment": "Доставка...", 
  "use_profile_addresses": true
}
```
Response:  
201 - created;
```
{
  "success": true,
  "order": {
    "id": "int",
    "status": "pending",
    "total_price": "5499",
    "currency": "RUB",
    "items": [
      {
        "product_id": "id",
        "name": "string",
        "quantity": "int",
        "price": "5499"
      }
    ],
    "customer": {
      "id": "int", || nullable 
      "email": "ivan@example.com"
    },
    "address": {
      "city": "string",
      "street": "string"
    },
    "payment_details": {
      "method": "string",
      "amount": "5499"
    },
    "created_at": "..."
  },
  "next_actions": {
    "payment_url": "https://payment.gateway.com/order/ORD-123456",  || для отплаты, если нужна
    "confirmation_email_sent": true
  }
}

```


**Errors:**  
400 - ошибка валидации    
409 - конфликт данных   
500

