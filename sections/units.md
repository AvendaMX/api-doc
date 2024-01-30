
Units
=====

Endpoints:

- [Get Units](#get-units)
- [Get Unit](#get-unit)


Get Units
---------

* `GET /units.json` regresará una lista de unidades de medida del SAT.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en particular. A continuación la respuesta en formato JSON, la lista tiene todas las unidades de medida del SAT actuales, aunque aquí sólo se muestren cuatro a manera de ejemplo.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 1,
        "code": "H87",
        "description": "Pieza"
    },
    {
        "id": 2,
        "code": "EA",
        "description": "Elemento"
    },
    {
        "id": 3,
        "code": "E48",
        "description": "Unidad de Servicio"
    },
    {
        "id": 4,
        "code": "ACT",
        "description": "Actividad"
    }
]
```

Get Unit
--------

* `GET /units/1.json` regresará la unidad de medida del SAT. Donde `1` es el ID del catálogo.


###### Respuesta JSON de ejemplo
```json
{
    "id": 1,
    "code": "H87",
    "description": "Pieza"
}
```