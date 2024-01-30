Issuers
========

Endpoints:

- [Get issuers](#get-issuers)
- [Get issuer](#get-issuers)

Get Issuers
------------

* `GET /a/123/issuers.json` regresará una lista de todas los emisores disponibles para la cuenta ID `123`.

```json
[
    {
        "id": 84,
        "name": "Xochilt Casas",
        "rfc": "CACX7605101P8",
        "social_reason": "XOCHILT CASAS CHAVEZ",
        "fiscal_regime": {
            "id": 626,
            "description": "Régimen Simplificado de Confianza"
        },
        "address": {
            "id": 56,
            "postal_code": "10740"
        },
        "updated_at": "2023-06-29T18:04:25.376-06:00",
        "url": "/api/v1/a/14/issuers/84.json"
    },
    {
        "id": 115,
        "name": "Ximbo",
        "rfc": "IXS7607092R5",
        "social_reason": "INTERNACIONAL XIMBO Y SABORES SA DE CV",
        "fiscal_regime": {
            "id": 601,
            "description": "General de Ley Personas Morales"
        },
        "address": {
            "id": 87,
            "postal_code": "86925"
        },
        "updated_at": "2023-09-20T19:38:45.031-06:00",
        "url": "/api/v1/a/123/issuers/115.json"
    }
]
```

Get Issuer
-----------

* `GET /a/123/issuers/84.json` regresará el emisor con ID `84`.

```json
{
    "id": 84,
    "name": "Xochilt Casas",
    "rfc": "CACX7605101P8",
    "social_reason": "XOCHILT CASAS CHAVEZ",
    "fiscal_regime": {
        "id": 626,
        "description": "Régimen Simplificado de Confianza"
    },
    "address": {
        "id": 56,
        "postal_code": "10740"
    },
    "updated_at": "2023-06-29T18:04:25.376-06:00",
    "url": "/api/v1/a/123/issuers/84.json"
}
```