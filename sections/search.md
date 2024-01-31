Search
========

Endpoints:

- [Get Customers](#get-products)
- [Get Product](#get-product)
- [Get Product Catalogues](#create-product)
- [Update Product](#update-product)

Get Products
------------

* `GET /a/123/issuers/84/search/products.json?q=SKU123456701` regresará una lista de los productos encontrados para el query param `q` para el emisor ID `84` de la cuenta ID `123`.

Se puede hacer la búsqueda por nombre del producto, y SKU.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 89,
        "name": "Máquina de leche malteada",
        "sku": "SKU123456701",
        "unit": {
            "id": 4,
            "description": "Actividad"
        },
        "product_catalogue": {
            "id": 25952,
            "description": "Máquinas de leche malteada"
        },
        "tax_group": {
            "id": 1,
            "description": "IVA 16%"
        },
        "unitary": 1000.0,
        "total": 1162.0,
        "description": "Descripción de la máquina de leche malteada",
        "updated_at": "2024-01-26T11:56:23.710-06:00",
        "url": "/api/v1/a/123/issuers/84/products/89.json"
    }
]
```