## Роуты  
GET '/catalog/{section}/' - отображение страницы товаров   
GET '/catalog/{section}/{product}' - отображение страницы товара 

## Товары 

**Метод:** GET  
**URL:** /catalog/{section}/

Пример запроса: https://educube.ru/catalog/{section}/

**Response**  
200

Errors:  
404  
400  
500
---------------------------------
## Товар

**Метод:** GET  
**URL:** /catalog/{section}/{product}

Отображение страницы товара.

Пример запроса: 
https://educube.ru/catalog/{section}/{product}

**Назначение:**
- отображает информацию о товаре: название, артикул, описание, изображения(слайдер), цена, старая цена(при наличии), наличие, характеристики, подробное описание;
- детали набора(при наличии);
- похожие товары;


Response   
200
```
[  
    "id": int,  
    "product": "string",   
    "name": "string",  
    "product_intro_description": "string",
      
    "preview_images":  
            [  
                "url": "string",  
                "alt": "string"  
            ],
    "price":  
            [  
                "current_price": int,  
                "old_price": int (nullable), 
                "currency": "RUB",  
            ],  
    "availability":  
            [  
                "in_stock": "boolean",  
                "quantity": int,  
            ],   
    "main_description": "string",

    "instruction_link":  
            [  
                "name": "string",  
                "url": "string",  
            ],
    "attributes": 
            [
                "article": "string",
                "country": "string",
                "material": "string",
                "age": "string",
                "type": "string",
                "age": "string",
                "section": "string",
                "size": "string",
                "warranty_period": "boolean",
                "brand": "string",
                "category": "string",
                "manufacturer": "string",
            ],
[
```  

Errors  
404  
400   
500

