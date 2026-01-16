## Раздел каталога

**Метод:** GET  
**URL:** /catalog/{section}/

**Пример запроса на сервер:**  
https://educube.ru/catalog/lego-education/

**Фильтрация товаров:**
- price (string);
- age (string);
- direction (string);
- category (string);
- series (string);

**Пример запроса:**  
https://educube.ru/catalog/lego-education/?age=7-10&direction=mathematical

**Сортировка товаров:**
- sort (string);
- order (string);

**Значения sort:**
- SORT - по популярности;
- NAME - по алфавиту;
- ORDER - по цене;

**Значения order;**
- asc - по возрастанию;
- desc - по убыванию;

**Пример запроса:**  
https://educube.ru/catalog/lego-education/?sort=PRICE&order=desc

**Response:**  
200 OK

**Errors:**  
404 not found  
400 bad request  
500 server error 





