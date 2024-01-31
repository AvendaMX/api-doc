
Payment Forms
==============

Endpoints:

- [Get Payment Forms](#get-payment-forms)
- [Get Payment Form](#get-payment-form)


Get Payment Forms
------------------

* `GET /payment_forms.json` regresará una lista [paginada](https://github.com/avendaMX/api-doc/blob/master/README.md#paginación) con todos las formas de pago.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en particular. A continuación la respuesta en formato JSON, la lista tiene todos las formas de pago actuales, aunque aquí sólo se muestren cuatro a manera de ejemplo.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 1,
        "description": "Efectivo"
    },
    {
        "id": 2,
        "description": "Cheque nominativo"
    },
    {
        "id": 3,
        "description": "Transferencia electrónica de fondos"
    },
    {
        "id": 4,
        "description": "Tarjeta de crédito"
    }
]
```

Get Payment Form
-----------------

* `GET /payment_forms/1.json` regresará una forma de pago. Donde `1` es el ID de la forma de pago.


###### Respuesta JSON de ejemplo
```json
{
    "id": 1,
    "description": "Efectivo"
}
```