Products
========

Endpoints:

- [Get Products](#get-products)
- [Get Product](#get-product)

Get Products
------------

* `GET /a/123/issuers/84/products.json` regresará una lista de los productos disponibles para el emisor ID `84` de la cuenta ID `123`.

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
    },
    {
        "id": 88,
        "name": "Bomba de melaza",
        "sku": "SKU123456700",
        "unit": {
            "id": 5,
            "description": "Kilogramo"
        },
        "product_catalogue": {
            "id": 25950,
            "description": "Bombas de melaza (syrup)"
        },
        "tax_group": {
            "id": 1,
            "description": "IVA 16%"
        },
        "unitary": 1000.0,
        "total": 1160.0,
        "description": "Descripción de la bomba de melaza",
        "updated_at": "2024-01-25T14:56:52.671-06:00",
        "url": "/api/v1/a/123/issuers/84/products/88.json"
    }
]
```

Get Product
-----------

* `GET /a/123/issuers/84/products/89.json` regresará el producto con ID `89`.

###### Respuesta JSON de ejemplo
```json
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
```

Create Product
--------------

* `POST /a/123/issuers/84/products.json` creará un producto para el emisor ID `89` de la cuenta ID `123`.


**Valores requeridos**:

* `name` - Un nombre para este producto.
* `unit_id` - ID de la unidad de medida, del catálogo de [unidades](https://github.com/avendaMX/api-doc/blob/master/sections/units.md#units)
* `product_catalogue_id` - `ID` del [catálogo de productos del SAT](https://github.com/avendaMX/api-doc/blob/master/sections/product_catalogues.md#product_catalogues).


_Valores opcionales_:

* `sku` - Identificador interno del producto.
* `unitary` - Valor del precio unitario, este es un valor predeterminado.
* `tax_group_id` - ID del catálogo de [Impuestos grupales](https://github.com/avendaMX/api-doc/blob/master/sections/tax_groups.md#tax_groups)
* `total` - Valor del monto total del producto, tomando en cuenta el impuesto grupal y el precio unitario.
* `descripción` - Descripción del producto.


El estatus regresado será un `201 - Created` y el objeto Product en formato `JSON`.

###### Petición JSON de ejemplo
```json
{
    "name": "Máquina de leche malteada",
    "sku": "SKU123456701",
    "product_catalogue_id": 25950,
    "unit_id": 5,
    "unitary": 1000,
    "tax_group_id": "1",
    "total": 1160,
    "description": "Máquinas de leche malteada"
}
```

Update Product
--------------

* `PUT /a/123/issuers/84/products/89.json` actualizará un producto para el emisor ID `89` de la cuenta ID `123`.


**Valores requeridos**:

* `name` - Un nombre para este producto.
* `unit_id` - ID de la unidad de medida, del catálogo de [unidades](https://github.com/avendaMX/api-doc/blob/master/sections/units.md#units)
* `product_catalogue_id` - `ID` del [catálogo de productos del SAT](https://github.com/avendaMX/api-doc/blob/master/sections/product_catalogues.md#product_catalogues).


_Valores opcionales_:

* `sku` - Identificador interno del producto.
* `unitary` - Valor del precio unitario, este es un valor predeterminado.
* `tax_group_id` - ID del catálogo de [Impuestos grupales](https://github.com/avendaMX/api-doc/blob/master/sections/tax_groups.md#tax_groups)
* `total` - Valor del monto total del producto, tomando en cuenta el impuesto grupal y el precio unitario.
* `descripción` - Descripción del producto.


El estatus regresado será un `200 - OK` y el objeto Product en formato `JSON`.

###### Petición JSON de ejemplo
```json
{
    "name": "Máquina de leche malteada",
    "sku": "SKU123456701",
    "product_catalogue_id": 25950,
    "unit_id": 4,
    "unitary": 1000,
    "tax_group_id": "1",
    "total": 1160,
    "description": "Máquinas de leche malteada, producto para venta al público"
}
```