
Payment Methods
===============

Endpoints:

- [Get Payment Methods](#get-payment-methods)
- [Get Payment Method](#get-payment-method)


Get Payment Methods
-------------------

* `GET /payment_methods.json` regresará una lista con todos los métodos de pago.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en particular. A continuación la respuesta en formato JSON, la lista tiene todos métodos de pago actuales.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 2,
        "description": "PPD",
        "long_description": "Pago en parcialidades o diferido"
    },
    {
        "id": 1,
        "description": "PUE",
        "long_description": "Pago en una sola exhibición"
    }
]
```

Get Payment Method
------------------

* `GET /payment_methods/1.json` regresará un método de pago. Donde `1` es el ID del método de pago.


###### Respuesta JSON de ejemplo
```json
{
    "id": 1,
    "description": "PUE",
    "long_description": "Pago en una sola exhibición"
}
```