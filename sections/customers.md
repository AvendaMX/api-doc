Customers
========

Endpoints:

- [Get Customers](#get-issuers)
- [Get Customer](#get-issuers)
- [Create Customer](#get-issuers)
- [Update Customer]

Get Issuers
------------

* `GET /a/123/issuers/84/customers.json` regresará una lista de todos los clientes disponibles para el emisor ID `84` de la cuenta ID `123`.

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
    },
    {
        "id": 247,
        "name": "Escuela Kemper",
        "social_reason": "ESCUELA KEMPER URGATE",
        "rfc": "EKU9003173C9",
        "fiscal_regime": {
            "id": 601,
            "description": "General de Ley Personas Morales"
        },
        "addresses": [
            {
                "id": 252,
                "postal_code": "26015"
            }
        ],
        "updated_at": "2024-01-22T14:18:11.294-06:00",
        "url": "/api/v1/a/123/issuers/84/customers/247.json"
    }
]
```

Get Customer
-----------

* `GET /a/123/issuers/84/customers/248.json` regresará el cliente con ID `248` del emisor `84` de la cuenta ID `123`.

```json
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
```