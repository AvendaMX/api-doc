
Request Types
=============

Endpoints:

- [Get Request Types](#get-request-types)


Get Request Types
-----------------

* `GET /request_types.json` regresará una lista con los posibles tipos de petición.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en particular. 

Estos valores son usados al momento de la creación o edición de facturas, tiene que ver con el tipo de petición para la factura. En este caso `stamp` intentará timbrar la factura, mientras que `draft` sólo la guardará como borrador.

###### Respuesta JSON de ejemplo
```json
[
    "stamp",
    "draft"
]
```