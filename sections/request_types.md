
Request Types
=============

Endpoints:

- [Get Request Types](#get-request-types)


Get Request Types
-----------------

* `GET /request_types.json` regresará una lista con los posibles tipos de petición.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en particular. 

Estos valores son usados al momento de la creación o edición de facturas, tiene que ver con el tipo de petición para la factura. `stamp` intentará timbrar la factura inmediatamente, mientras que `draft` sólo la creará como borrador.

###### Respuesta JSON de ejemplo
```json
[
    "stamp",
    "draft"
]
```