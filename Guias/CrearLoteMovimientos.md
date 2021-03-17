<h1 align="center">GET Factura/GetOrCreatePDF?preferencia={preferencia}</h1>

Crea una lista de comprobantes en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/CrearLoteMovimientos

<h2 align="center">Request</h2>

<h3>Parametros</h3>

<table style="width:100%;">
<tr>
    <th>Nombre</th>
    <th>Descripcion</th>
    <th>Tipo</th>
    <th>Obligatorio</th>
    <th>Informacion Adicional</th>
</tr>
<tr>
    <td>Movimientos</td>
    <td>Lista de movimientos en Tango Factura</td>
    <td>IList of <a href="./CrearFactura.md">Facturacion</a></td>
    <td>Si</td>
    <td>-</td>
</tr>
<tr>
    <td>EsPrimerLote</td>
    <td>Se utiliza para tener referencia si es el primer lote de movimientos que se realiza en Tango Factura</td>
    <td>boolean</td>
    <td>Si</td>
    <td>-</td>
</tr>
<tr>
    <td>UserIdentifier</td>
    <td>Es el UserIdentifier asociado a la aplicacion</td>
    <td>string</td>
    <td>si</td>
    <td>-</td>
</tr>
<tr>
    <td>ApplicationPublicKey</td>
    <td>Clave publica de la aplicacion</td>
    <td>string</td>
    <td>Si</td>
    <td>-</td>
</tr>
<tr>
    <td>Token</td>
    <td>Es el token asociado a la aplicacion</td>
    <td>string</td>
    <td>si</td>
    <td>-</td>
</tr>
</table>

<h3>Formato Ejemplo</h3>

```
    "Movimientos": [
    {
    "Letra": "A",
    "ClienteCodigo": "00001458",
    "ClienteNombre": "Axoft SA",
    "ClienteDireccion": " Cerrito 1214, C.A.B.A. (C1010AAZ), Buenos Aires",
    "RegimenDatosFce": {
        "ReferenciaComercial": "Referencia comercial",
        "UserIdentifier": "",
        "ApplicationPublicKey": "",
        "Token": ""
    },
    "RegimenDatosFEX": {
        "TipoExportacion": 1,
        "CodigoPais": "sample string 2",
        "PaisNombre": "sample string 3",
        "TipoPersona": 4,
        "CuitPais": "sample string 5",
        "IncotermsClausulaVenta": "sample string 6",
        "IncotermsInformacionComplementaria": "sample string 7",
        "PermisosEmbarque": [
        {
            "Codigo": "sample string 1",
            "CodigoPaisDestinoMercaderia": "sample string 2",
            "NombrePaisDestinoMercaderia": "sample string 3"
        }
        ],
        "IdiomaComprobante": 8,
        "IdentificadorTributario": "sample string 9",
        "ObservacionesComerciales": "sample string 10"
    },
    "ClienteTipoDocumento": 1,
    "ClienteNumeroDocumento": "30-63165881-0",
    "ClienteEmail": "tangofactura@axoft.com",
    "CategoriaImpositivaCodigo": "Responsable Inscripto",
    "Observacion": "Observación del comprobante. (Opcional)",
    "DetallesMovimiento": [
        {
        "ProductoCodigo": "ML48516",
        "ProductoCodigoAlternativo": "sample string 1",
        "ProductoNombre": "Producto inicial ",
        "ProductoDescripcion": "Primer producto registrado en Tango Factura",
        "Cantidad": 2.0,
        "Precio": 3.0,
        "DepositoID": 1,
        "Bonificacion": 4.0,
        "DetalleAlicuotas": [
            {
            "AlicuotaCodigo": 1,
            "AlicuotaPorcentaje": 1.0,
            "ImpuestoID": 2
            }
        ],
        "PosicionImpuestoID": 1
        }
    ],
    "FechaComprobante": "2021-03-17T12:20:38.4612041+00:00",
    "FechaServicioDesde": "2021-03-17T12:20:38.4612041+00:00",
    "FechaServicioHasta": "2021-03-17T12:20:38.4612041+00:00",
    "MovimientoReferenciaID": 1,
    "TipoMovimiento": 1,
    "PerfilComprobanteID": 1,
    "OrderID": 1,
    "FechaPAsocDesde": "2021-03-17T12:20:38.4612041+00:00",
    "FechaPAsocHasta": "2021-03-17T12:20:38.4612041+00:00",
    "DescuentoTotal": 1.0,
    "DepositoID": 1,
    "UserIdentifier": "",
    "ApplicationPublicKey": "",
    "Token": ""
    }
    ],
    "EsPrimerLote": true,
    "UserIdentifier": "",
    "ApplicationPublicKey": "",
    "Token": ""
```

<h2 align="center">Response</h2>
<h3>Parametros</h3>
<table style="width: 100%;">
    <tr>
        <th>Nombre</th>
        <th>Descripcion</th>
        <th>Tipo</th>
        <th>Informacion Adicional</th>
    </tr>
    <tr>
        <td>Error</td>
        <td>Muestra una lista de mensajes de error</td>
        <td>IList of <a href="/Guias/Tipos de datos/DetalleError.md">DetalleError</a></td>
        <td></td>
    </tr>
    <tr>
        <td>CodigoError</td>
        <td>Muestra el codigo de error</td>
        <td>int</td>
        <td></td>
    </tr>
</table>

<h3>Formato ejemplo</h3>

```
    {
        "Data": {
        "AutorizacionExitosa": false
        },
        "Error": [
        {
            "Mensaje": "Error 404",
            "Nivel": 1
        }
        ],
        "CodigoError": 2
    }
```