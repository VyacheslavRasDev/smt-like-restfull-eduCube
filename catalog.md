## Каталог

**Метод:** GET  
**URL:** /catalog/

Отображение каталога товаров. При обращении к /catalog/ пользователь
перенаправляется в основной раздел каталога.

Пример запроса: 
https://educube.ru/catalog/
-----------------------------------------

## Раздел каталога

**Метод:** GET  
**URL:** /catalog/{section}/

Отображение подразделов раздела каталога, товаров, которые к нему относятся.

Пример запроса: https://educube.ru/catalog/lego-education/

**Response:**  
200 - OK;  
302 - Redirect;

**Errors:**  
404 -  not found;  
400 - bad request;  
500 - server error;







