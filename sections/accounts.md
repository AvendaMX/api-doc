Accounts
========

Endpoints:

- [Get accounts](#get-accounts)
- [Get account](#get-account)

Get accounts
------------

* `GET /a.json` regresará una lista [paginada](https://github.com/avendaMX/api-doc/blob/master/README.md#paginacion) de las cuentas disponibles al usuario.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 122,
        "name": "Avenda",
        "status": "active",
        "url": "/api/v1/a/122.json"
    },
    {
        "id": 123,
        "name": "Grupo Industrial",
        "status": "trial",
        "url": "/api/v1/a/123.json"
    }
]
```

Get account
-----------

* `GET /a/123.json` regresará la cuenta ID 123.

###### Respuesta JSON de ejemplo
```json
{
    "id": 123,
    "name": "Grupo Industrial",
    "status": "trial",
    "url": "/api/v1/a/123.json"
}
```