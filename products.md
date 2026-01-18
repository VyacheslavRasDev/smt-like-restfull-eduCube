## Товары (не завершено)

**Метод:** GET  
**URL:**  
 - /products/

Отображение товара. При обращении к /products/ пользователь
перенаправляется в основной раздел каталога.

**Пример запроса на сервер:**  
https://educube.ru/products/
-------------------------

## Товар

**Метод:** GET  
**URL:**
- /products/{product}

**Пример запроса на сервер:**  
https://educube.ru/products/lego-education-bricq-motion/

**Назначение:**
- отображает информацию о товаре: название, артикул, описание, изображения(слайдер), цена, старая цена(при наличии), наличие, характеристики, подробное описание;
- детали набора(при наличии);
- похожие товары;
  

Response:  
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
                "old_price": int,  
                "currency": "RUB",  
            ],  
    "availability":  
            [  
                "in_stock": boolean,  
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
```  

**Errors:**  
404 - not found;    
500 -  server error;
