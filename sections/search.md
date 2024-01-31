Search
========

Endpoints:

- [Get Customers](#get-products)
- [Get Product](#get-product)
- [Get Product Catalogues](#create-product)


Get Customers
-------------

* `GET /a/123/issuers/84/search/customers.json?q=FUNK671228PH6` regresará una lista [paginada](https://github.com/avendaMX/api-doc/blob/master/README.md#paginación) de los productos encontrados para el query param `q` para el emisor ID `84` de la cuenta ID `123`.

Se puede hacer la búsqueda por nombre del nombre de cliente, razón social y RFC.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 248,
        "name": "Karla Fuentes",
        "social_reason": "KARLA FUENTE NOLASCO",
        "rfc": "FUNK671228PH6",
        "fiscal_regime": {
            "id": 612,
            "description": "Personas Físicas con Actividades Empresariales y Profesionales"
        },
        "addresses": [
            {
                "id": 253,
                "postal_code": "83200"
            }
        ],
        "updated_at": "2024-01-26T11:38:25.613-06:00",
        "url": "/api/v1/a/123/issuers/84/customers/248.json"
    }
]
```

Get Products
------------

* `GET /a/123/issuers/84/search/products.json?q=SKU123456701` regresará una lista [paginada](https://github.com/avendaMX/api-doc/blob/master/README.md#paginación) de los productos encontrados para el query param `q` para el emisor ID `84` de la cuenta ID `123`.

Se puede hacer la búsqueda por nombre del producto y SKU.

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

Get Product Catalogues
----------------------

* `GET /a/123/issuers/84/search/product_catalogues.json?q=vacas` regresará una lista [paginada](https://github.com/avendaMX/api-doc/blob/master/README.md#paginación) del catálogo de productos y servicios del SAT encontrados para el query param `q` para el emisor ID `84` de la cuenta ID `123`.

Se puede hacer la búsqueda por descripción y código del producto o servicio y nombres alternativos.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 17,
        "code": "10101516",
        "description": "Ganado vacuno",
        "alternatives": "Bueyes, Búfalos, Cebús, Otros vacunos o bovinos, Toros, Vacas"
    }
]
```