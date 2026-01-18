## Каталог

**Метод:** GET  
**URL:**  
 - /catalog/

Отображение каталога товаров. При обращении к /catalog/ пользователь
перенаправляется в основной раздел каталога.

Пример запроса: 
https://educube.ru/catalog/
-----------------------------------------

## Раздел каталога

**Метод:** GET  
**URL:**
- /catalog/{section}/

Отображение подразделов раздела каталога, товаров, которые к нему относятся.

Пример запроса: 
https://educube.ru/catalog/lego-education/

**Назначение:**
- отображает подразделы;
- отображает товары раздела;
- фильтрация;
- сортировка;
- пагинация;

**Фильтрация товаров:**
- age (string);
- direction (string);
- category (string);
- series (string);

Пример запроса: 
https://educube.ru/catalog/lego-education/?age=7-10&direction=mathematical

**Сортировка товаров:**
- sort (string);
- order (string);

**Значения sort:**
- SORT - по популярности;
- NAME - по алфавиту;
- PRICE - по цене;

**Значения order;**
- asc - по возрастанию;
- desc - по убыванию;

Пример запроса: 
https://educube.ru/catalog/lego-education/?sort=PRICE&order=desc

**Response:**  
200 OK

**Errors:**  
404 not found  
400 bad request  
500 server error
---------------------------------------------------






