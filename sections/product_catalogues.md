
Product Catalogues
==================

Endpoints:

- [Get Product Catalogues](#get-product-catalogues)
- [Get Product Catalogue](#get-product-catalogue)


Get Product Catalogues
----------------------

* `GET /product_catalogues.json` regresará una lista del catálogo de productos y servicios del SAT.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en particular. A continuación la respuesta en formato JSON, la lista tiene todos los productos y servicios del SAT actuales, aunque aquí sólo se muestren cuatro a manera de ejemplo.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 1,
        "code": "01010101",
        "description": "No existe en el catálogo",
        "alternatives": "Público en general"
    },
    {
        "id": 2,
        "code": "10101500",
        "description": "Animales vivos de granja",
        "alternatives": ""
    },
    {
        "id": 3,
        "code": "10101501",
        "description": "Gatos vivos",
        "alternatives": ""
    },
    {
        "id": 4,
        "code": "10101502",
        "description": "Perros",
        "alternatives": ""
    }
]
```

Get Product Catalogue
---------------------

* `GET /product_catalogues/2.json` regresará el producto o servicio del catálogo del SAT. Donde `2` es el ID del catálogo.


###### Respuesta JSON de ejemplo
```json
{
    "id": 2,
    "code": "10101500",
    "description": "Animales vivos de granja",
    "alternatives": ""
}
```