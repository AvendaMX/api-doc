Avenda API
==================

Bienvenido a la API de Avenda.mx.

Peticiones
----------

Las peticiones tienen el prefijo **`https://uno.avenda.mx/api/v1`**.

Cada petición debe contener el header `Content-Type: application/json` y todas las peticiones son en formato JSON y el endpoint debe terminar en `.json`.

Timbrando
---------

Para timbrar con un emisor, es necesario que este último esté completamente configurado a través de la interfaz web (con los archivos CSD y la información fiscal necesaria).

Autorización
-------------

La autorización se realiza mediante una petición `POST` a `https://uno.avenda.mx/usuario/ingresar.json`, agregando un objeto JSON `user` conteniendo los parámetros `email` y `password`.

Este usuario y contraseña son con los que se hace login desde la interfaz web.


Paginación
----------

La mayoría de los catálogos regresará sólo un subconjunto de los resultados disponibles, para acceder a la paginación, agrega un query param `page` con el valor numérico de la página a consultar. Por ejemplo `https://uno.avenda.mx/api/v1/product-catalogues.json?page=2`.

Todas las listas paginadas regresan 20 ítems por página. Y el número total de registros viene en el header `X-Total-Count`.

###### Petición JSON de ejemplo
```json
{
    "user": {
        "email": "test@example.com",
        "password": "lacontraseñadelacuenta"
    }
}
```

La respuesta regresará un JWT (JSON web token) en el header `Authorization` que se deberá a su vez adjuntar al mismo header `Authorization` que deberá contener `Bearer $JWT_TOKEN` en las llamadas posteriores a la API.

###### Petición JSON de ejemplo
``` shell
curl -H "Authorization: Bearer $JWT_TOKEN" \
  -H 'Content-Type: application/json' \
  https://uno.avenda.mx/api/v1/a.json
```


Endpoints
----------------
- [Accounts](https://github.com/avendaMX/api-doc/blob/master/sections/accounts.md#accounts)
- [Cfdi Uses](https://github.com/avendaMX/api-doc/blob/master/sections/cfdi_uses.md#cfdi_uses)
- [Customers](https://github.com/avendaMX/api-doc/blob/master/sections/customers.md#customers)
- [Fiscal Regimes](https://github.com/avendaMX/api-doc/blob/master/sections/fiscal_regimes.md#fiscal_regimes)
- [Invoices](https://github.com/avendaMX/api-doc/blob/master/sections/invoices.md#invoices)
- [Issuers](https://github.com/avendaMX/api-doc/blob/master/sections/issuers.md#issuers)
- [Payment Forms](https://github.com/avendaMX/api-doc/blob/master/sections/payment_forms.md#payment_forms) 
- [Payment Methods](https://github.com/avendaMX/api-doc/blob/master/sections/payment_methods.md#payment_methods)
- [Product Catalogues](https://github.com/avendaMX/api-doc/blob/master/sections/product_catalogues.md#product_catalogues)
- [Products](https://github.com/avendaMX/api-doc/blob/master/sections/products.md#products)
- [Request Types](https://github.com/avendaMX/api-doc/blob/master/sections/request_types.md#request_types)
- [Search](https://github.com/avendaMX/api-doc/blob/master/sections/search.md#search)
- [Stamping Dates](https://github.com/avendaMX/api-doc/blob/master/sections/stamping_dates.md#stamping_dates)
- [Tax Groups](https://github.com/avendaMX/api-doc/blob/master/sections/tax_groups.md#tax_groups)
- [Units](https://github.com/avendaMX/api-doc/blob/master/sections/units.md#units)
