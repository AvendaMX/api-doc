Customers
========

Endpoints:

- [Get Customers](#get-customers)
- [Get Customer](#get-customer)
- [Create Customer](#create-customer)
- [Update Customer](#update-issuers)

Get Customers
------------

* `GET /a/123/issuers/84/customers.json` regresará una lista de todos los clientes disponibles para el emisor ID `84` de la cuenta ID `123`.

###### Petición JSON de ejemplo
```json
[
    {
        "id": 248,
        "name": "Karla Fuentes",
        "social_reason": "KARLA FUENTE NOLASCO",
        "rfc": "FUNK671228PH6",
        "fiscal_regime": {
            "id": 612,
            "description": "Personas Físicas con Actividades Empresariales y Profesionales"
        },
        "addresses": [
            {
                "id": 253,
                "postal_code": "83200"
            }
        ],
        "updated_at": "2024-01-26T11:38:25.613-06:00",
        "url": "/api/v1/a/123/issuers/84/customers/248.json"
    },
    {
        "id": 247,
        "name": "Escuela Kemper",
        "social_reason": "ESCUELA KEMPER URGATE",
        "rfc": "EKU9003173C9",
        "fiscal_regime": {
            "id": 601,
            "description": "General de Ley Personas Morales"
        },
        "addresses": [
            {
                "id": 252,
                "postal_code": "26015"
            }
        ],
        "updated_at": "2024-01-22T14:18:11.294-06:00",
        "url": "/api/v1/a/123/issuers/84/customers/247.json"
    }
]
```

Get Customer
------------

* `GET /a/123/issuers/84/customers/248.json` regresará el cliente con ID `248` del emisor ID `84` de la cuenta ID `123`.

###### Petición JSON de ejemplo
```json
{
    "id": 248,
    "name": "Karla Fuentes",
    "social_reason": "KARLA FUENTE NOLASCO",
    "rfc": "FUNK671228PH6",
    "fiscal_regime": {
        "id": 612,
        "description": "Personas Físicas con Actividades Empresariales y Profesionales"
    },
    "addresses": [
        {
            "id": 253,
            "postal_code": "83200"
        }
    ],
    "updated_at": "2024-01-26T11:38:25.613-06:00",
    "url": "/api/v1/a/123/issuers/84/customers/248.json"
}
```

Create Customer
---------------

* `POST /a/123/issuers/84/customers.json` creará un cliente para el emisor ID `84` de la cuenta ID `123`.


**Valores requeridos**:

* `name` - Un nombre para este cliente.
* `social_reason` - Razón social como dada de alta ante el SAT (sin `SA de CV` o similar).
* `fiscal_regime_id` - `ID` del catálogo de [régimenes fiscales](https://github.com/avendaMX/api-doc/blob/master/sections/fiscal_regimes.md#fiscal_regimes).
* `addresses` - Arreglo de objetos, conteniendo el parámetro `postal_code` con el código postal fiscal registrado ante el SAT.

_Valores opcionales_:

Este endpoint no tiene valores opcionales.

El estatus regresado será un `201 - Created` y el objeto Customer en formato `JSON`.

###### Petición JSON de ejemplo
```json
{
    "name": "Innovación Valor y Desarrollo",
    "rfc": "IVD920810GU2",
    "social_reason": "INNOVACION VALOR Y DESARROLLO",
    "fiscal_regime_id": "601",
    "addresses": [
        {
            "postal_code": "30185"
        }
    ]
}
```


Update Customer
---------------

* `PUT /a/123/issuers/84/customers/248.json` actualizará el cliente con ID `248` para el emisor ID `84` de la cuenta ID `123`.

**Valores requeridos**:

* `name` - Un nombre para este cliente.
* `social_reason` - Razón social como dada de alta ante el SAT (sin `SA de CV` o similar).
* `fiscal_regime_id` - `ID` del catálogo de [régimenes fiscales](https://github.com/avendaMX/api-doc/blob/master/sections/fiscal_regimes.md#fiscal_regimes).
* `addresses` - Arreglo de objetos, conteniendo el parámetro `postal_code` con el código postal fiscal registrado ante el SAT. 
*     Para la actualización es necesario enviar el ID del objeto `address`.

_Valores opcionales_:

Este endpoint no tiene valores opcionales.

###### Petición JSON de ejemplo
```json
{
    "name": "Innovación Valor y Desarrollo",
    "rfc": "IVD920810GU2",
    "social_reason": "INNOVACION VALOR Y DESARROLLO",
    "fiscal_regime_id": "601",
    "addresses": [
        {
            "id": 253,
            "postal_code": "30185"
        }
    ]
}