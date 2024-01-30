
Stamping Dates
=============

Endpoints:

- [Get Stamping Dates](#get-stamping-dates)


Get Stamping Dates
------------------

* `GET /stamping_dates.json` regresará una lista con las posibles fechas de timbrado.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en particular. 

Estos valores son usados al momento de la creación o edición de facturas, tiene que ver con la fecha con la que se enviará la factura. En este caso `current` enviará la petición de timbrado con la fecha actual, y las demás opciones retrasan la hora 24, 48 o 72 horas.

###### Respuesta JSON de ejemplo
```json
[
    "current",
    "minus_24h",
    "minus_48h",
    "minus_72h"
]
```