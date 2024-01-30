
Tax Groups
==========

Endpoints:

- [Get Tax Groups](#get-tax-groups)
- [Get Tax Group](#get-tax-group)


Get Tax Groups
--------------

* `GET /a/123/issuers/84/tax_groups.json` regresará una lista con todos los impuestos grupales para el emisor con ID `84` de la cuenta con ID `123`.

Los impuestos grupales se usan para asignarle un impuesto al concepto de una factura. Están compuestos de impuestos individuales y se tendrán tantos como sean configuradoes desde la interfaz web, aquí se muestran tres a manera de ejemplo.


###### Respuesta JSON de ejemplo
```json
[
    {
        "id": 1,
        "description": "IVA 16%"
    },
    {
        "id": 2,
        "description": "IVA 8%"
    },
    {
        "id": 9,
        "description": "IVA 16%  ISR 1.25% IVA RET 10.667%"
    }
]
```

Get Tax Group
-------------

* `GET /a/123/issuers/84/tax_groups/1.json` regresará un impuesto grupal, donde `1` es el ID del impuesto grupal para el emisor con ID `84` de la cuenta con ID `123`.


###### Respuesta JSON de ejemplo
```json
{
    "id": 1,
    "description": "IVA 16%"
}
```