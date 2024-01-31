Invoices
========

Endpoints:

- [Get Invoices](#get-invoices)
- [Get Invoice](#get-invoice)
- [Create Invoice](#create-invoice)
- [Update Invoice](#update-invoice)

Get Invoices
------------

* `GET /a/123/issuers/84/invoices.json` regresará una lista [paginada](https://github.com/avendaMX/api-doc/blob/master/README.md#paginación) de todas las facturas disponibles para el emisor ID `84` de la cuenta ID `123`.

###### Rspuesta JSON de ejemplo
```json
[
    {
        "id": 942,
        "status": "stamped",
        "uuid": "9C7793F9-499B-49A5-9072-1D0309101183",
        "public_url": "http://uno.avenda.mx/publico/facturas/9C7793F9-499B-49A5-9072-1D0309101183",
        "customer": {
            "id": 8,
            "name": "Industria Especial"
        },
        "payment_method": {
            "id": 1,
            "description": "PUE",
            "long_description": "Pago en una sola exhibición"
        },
        "cfdi_use": {
            "id": 1,
            "description": "Adquisición de mercancías"
        },
        "payment_form": {
            "id": 99,
            "description": "Por definir"
        },
        "line_items": [
            {
                "id": 1118,
                "product": {
                    "id": 33,
                    "name": "Mantenimiento de software"
                },
                "unitary": 1000.0,
                "quantity": 2.0,
                "discount": 200.0,
                "amount": 2000.0,
                "tax_group": {
                    "id": 9,
                    "description": "IVA 16%  ISR 1.25% IVA RET 10.667%"
                }
            }
        ],
        "folio": "AB0742",
        "subtotal": 2000.0,
        "discount": 200.0,
        "taxes": [
            {
                "name": "IVA  16.0%",
                "amount": 288.0
            },
            {
                "name": "ISR 1.25%",
                "amount": 22.5
            },
            {
                "name": "IVA RET 10.667%",
                "amount": 192.01
            }
        ],
        "tax": 73.49,
        "total": 1873.49,
        "stamping_date": "current",
        "updated_at": "2024-01-30T20:31:47.451-06:00",
        "stamped_at": "2024-01-29T08:39:58.000-06:00",
        "url": "/api/v1/a/123/issuers/84/vouchers/invoices/942.json"
    },
    {
        "id": 943,
        "status": "draft",
        "customer": {
            "id": 8,
            "name": "Industria Especial"
        },
        "payment_method": {
            "id": 1,
            "description": "PUE",
            "long_description": "Pago en una sola exhibición"
        },
        "cfdi_use": {
            "id": 1,
            "description": "Adquisición de mercancías"
        },
        "line_items": [
            {
                "id": 1119,
                "product": {
                    "id": 33,
                    "name": "Mantenimiento de software"
                },
                "unitary": 1000.0,
                "quantity": 2.0,
                "discount": 200.0,
                "amount": 2000.0,
                "tax_group": {
                    "id": 9,
                    "description": "IVA 16%  ISR 1.25% IVA RET 10.667%"
                }
            }
        ],
        "folio": "AB0743",
        "subtotal": 2000.0,
        "discount": 200.0,
        "taxes": [
            {
                "name": "IVA  16.0%",
                "amount": 288.0
            },
            {
                "name": "ISR 1.25%",
                "amount": 22.5
            },
            {
                "name": "IVA RET 10.667%",
                "amount": 192.01
            }
        ],
        "tax": 73.49,
        "total": 1873.49,
        "stamping_date": "current",
        "updated_at": "2024-01-29T23:09:07.125-06:00",
        "url": "/api/v1/a/123/issuers/84/vouchers/invoices/943.json"
    }
]
```

Get Invoice
------------

* `GET /a/123/issuers/84/invoices/942.json` regresará la factura con ID `942` del emisor ID `84` de la cuenta ID `123`.

###### Petición JSON de ejemplo
```json
{
    "id": 942,
    "status": "stamped",
    "uuid": "9C7793F9-499B-49A5-9072-1D0309101183",
    "public_url": "http://uno.avenda.mx/publico/facturas/9C7793F9-499B-49A5-9072-1D0309101183",
    "customer": {
        "id": 8,
        "name": "Industria Especial"
    },
    "payment_method": {
        "id": 1,
        "description": "PUE",
        "long_description": "Pago en una sola exhibición"
    },
    "cfdi_use": {
        "id": 1,
        "description": "Adquisición de mercancías"
    },
    "payment_form": {
        "id": 99,
        "description": "Por definir"
    },
    "line_items": [
        {
            "id": 1118,
            "product": {
                "id": 33,
                "name": "Mantenimiento de software"
            },
            "unitary": 1000.0,
            "quantity": 2.0,
            "discount": 200.0,
            "amount": 2000.0,
            "tax_group": {
                "id": 9,
                "description": "IVA 16%  ISR 1.25% IVA RET 10.667%"
            }
        }
    ],
    "folio": "AB0742",
    "subtotal": 2000.0,
    "discount": 200.0,
    "taxes": [
        {
            "name": "IVA  16.0%",
            "amount": 288.0
        },
        {
            "name": "ISR 1.25%",
            "amount": 22.5
        },
        {
            "name": "IVA RET 10.667%",
            "amount": 192.01
        }
    ],
    "tax": 73.49,
    "total": 1873.49,
    "stamping_date": "current",
    "updated_at": "2024-01-30T20:31:47.451-06:00",
    "stamped_at": "2024-01-29T08:39:58.000-06:00",
    "url": "/api/v1/a/123/issuers/84/vouchers/invoices/942.json"
}
```

Create Invoice
--------------

* `POST /a/123/issuers/84/invoices.json` creará una factura para el emisor ID `84` de la cuenta ID `123`.


**Valores requeridos**:

* `customer_id` - `ID` del catálogo de [clientes](https://github.com/avendaMX/api-doc/blob/master/sections/customers.md#customers).
* `cfdi_use_id` - `ID` del catálogo de [usos de CFDI](https://github.com/avendaMX/api-doc/blob/master/sections/cfdi_uses.md#cfdi_uses).
* `payment_form_id` - `ID` del catálogo de [formas de pago](https://github.com/avendaMX/api-doc/blob/master/sections/payment_forms.md#payment_forms).
* `payment_method_id` - `ID` del catálogo de [métodos de pago](https://github.com/avendaMX/api-doc/blob/master/sections/payment_methods.md#payment_methods).
* `request_type` - Valor en cadena de texto del catálogo de [tipos de petición](https://github.com/avendaMX/api-doc/blob/master/sections/request_types.md#request_types).
* `line_items` - Arreglo de [conceptos](#conceptos).

_Valores opcionales_:

* `notes` - Notas adicionales a agregar a la factura, aparecerán en la representación en PDF.
* `stamping_date` - Valor en cadena de texto del catálogo de [fechas de timbrado](https://github.com/avendaMX/api-doc/blob/master/sections/stamping_dates.md#stamping_dates). El valor por defecto es `current`.

Conceptos
---------

**Valores requeridos**:

* `product_id` - `ID` del catálogo de [productos](https://github.com/avendaMX/api-doc/blob/master/sections/products.md#products).
* `quantity` - Cantidad de productos del concepto, admite hasta 6 decimales.
* `unitary` - Valor unitario del producto, admite hasta 6 decimales.
* `tax_group_id` - `ID` del catálogo de [impuestos grupales](https://github.com/avendaMX/api-doc/blob/master/sections/tax_groups.md#tax_groups).


_Valores opcionales_:

* `discount` - Valor monetario a 2 decimales del descuento.
* `descripción` - Descripción del concepto.


No es necesario enviar totales ni subtotales, la API se encargará de realizar el cálculo de estos valores.

El estatus regresado será un `201 - Created` y el objeto Customer en formato `JSON`.

###### Petición JSON de ejemplo
```json
{
    "customer_id": 8,
    "stamping_date": "current",
    "cfdi_use_id": 1,
    "payment_form_id": 1,
    "payment_method_id": 1,
    "notes": "Factura a pagar en 30 días",
    "request_type": "stamp",
    "line_items": [
        {
            "product_id": 33,
            "description": "",
            "quantity": 2,
            "unitary": 1000,
            "discount": 200,
            "tax_group_id": 9
        }
    ]
}
```

Update Invoice
--------------

* `PUT /a/123/issuers/84/invoices/942.json` actualizará factura ID `942` para el emisor ID `84` de la cuenta ID `123`.

**Valores requeridos**:

* `request_type` - `ID` del catálogo de [productos](https://github.com/avendaMX/api-doc/blob/master/sections/products.md#products).


_Valores opcionales_:

* `customer_id` - `ID` del catálogo de [clientes](https://github.com/avendaMX/api-doc/blob/master/sections/customers.md#customers).
* `cfdi_use_id` - `ID` del catálogo de [usos de CFDI](https://github.com/avendaMX/api-doc/blob/master/sections/cfdi_uses.md#cfdi_uses).
* `payment_form_id` - `ID` del catálogo de [formas de pago](https://github.com/avendaMX/api-doc/blob/master/sections/payment_forms.md#payment_forms).
* `payment_method_id` - `ID` del catálogo de [métodos de pago](https://github.com/avendaMX/api-doc/blob/master/sections/payment_methods.md#payment_methods).
* `line_items` - Arreglo de [conceptos](#conceptos).

Se pueden actualizar todos los valores de la factura de manera opcional, el único valor requerido es `request_type`.

###### Petición JSON de ejemplo
```json
{
    "customer_id": 8,
    "stamping_date": "current",
    "cfdi_use_id": 1,
    "payment_form_id": 1,
    "payment_method_id": 1,
    "notes": "Factura a pagar en 30 días",
    "request_type": "stamp",
    "line_items": [
        {
            "product_id": 33,
            "description": "",
            "quantity": 2,
            "unitary": 1000,
            "discount": 200,
            "tax_group_id": 9
        }
    ]
}
```