
Fiscal Regimes
========

Endpoints:

- [Get Fiscal Regimes](#get-fiscal-regimes)
- [Get Fiscal Regime](#get-fiscal-regme)


Get Fiscal Regimes
------------------

* `GET /fiscal_regimes.json` regresará una lista con todos los regímenes fiscales.

Esta lista no está relacionada directamente con un emisor ni con una cuenta en partiicular. A continuacón la respuesta en formato JSON, la lista tiene todos los regímenes fiscales actuales, aunque aquí sólo se muestren cuatro a manera de ejemplo.

###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 601,
        "description": "General de Ley Personas Morales"
    },
    {
        "id": 603,
        "description": "Personas Morales con Fines no Lucrativos"
    },
    {
        "id": 605,
        "description": "Sueldos y Salarios e Ingresos Asimilados a Salarios"
    },
    {
        "id": 606,
        "description": "Arrendamiento"
    }
]
```

Get Fiscal Regime
-----------------

* `GET /cfdi_uses/626.json` regresará un régimen fiscal. Donde `626` es el ID del régimen fiscal.


###### Respuesta JSON de ejemplo
```json
{
    "id": 626,
    "description": "Régimen Simplificado de Confianza"
}
```