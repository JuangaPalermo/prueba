<h1 align="center">POST Factura/CrearPuntoVenta</h1>

Crea un de punto de venta en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/CrearPuntoVenta

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
    <td>Codigo</td>
    <td>Obtiene ó Setea el codigo del punto de venta.</td>
    <td>int</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>Descripcion</td>
    <td>Obtiene ó Setea la descripcion del punto de venta.</td>
    <td>string</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>EsElectronico</td>
    <td>Se utiliza para saber si el punto de venta es electronico o no.</td>
    <td>boolean</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>NumeroCAI</td>
    <td>Obtiene o setea el CAI (código de autorización de impresión).</td>
    <td>String</td>
    <td>Si</td>
    <td>Lo otorga AFIP al autorizar la emisión de un comprobante por web service.</td>
</tr>
<tr>
    <td>VencimientoCAI</td>
    <td>Obtiene o setea el vencimiento del CAI (código de autorización de impresión).</td>
    <td>Date?</td>
    <td>No</td>
    <td>-</td>
</tr>
<tr>
    <td>ProximoNumero</td>
    <td>Proximo numero para talonario A o C</td>
    <td>int</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>ProximoNumeroB</td>
    <td>Proximo numero para talonario B (solo RI)</td>
    <td>int</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>NumeroCAIB</td>
    <td>Obtiene o setea el CAI (código de autorización de impresión) solo para talonario tipo B.</td>
    <td>String</td>
    <td>Si</td>
    <td>-</td>
</tr>
<tr>
    <td>VencimientoCAIB</td>
    <td>Obtiene o Setea el vencimiento CAIB</td>
    <td>Date?</td>
    <td>No</td>
    <td></td>
</tr>
<tr>
    <td>UserIdentifier</td>
    <td>Es el UserIdentifier asociado a la aplicacion</td>
    <td>string</td>
    <td>Si</td>
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
    <td>Es el Token asociado a la aplicacion</td>
    <td>string</td>
    <td>Si</td>
    <td>-</td>
</tr>

</table>

<h3>Formato ejemplo</h3>

```
    {
    "Codigo": 1,
    "Descripcion": "sample string 2",
    "EsElectronico": true,
    "NumeroCAI": "1245398745687542",
    "VencimientoCAI": "2021-03-22T18:25:46.1289308+00:00",
    "ProximoNumero": 5,
    "ProximoNumeroB": 6,
    "NumeroCAIB": "sample string 7",
    "VencimientoCAIB": "2021-03-22T18:25:46.1289308+00:00",
    "UserIdentifier": "",
    "ApplicationPublicKey": "",
    "Token": ""
    }
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
        <td>Data</td>
        <td></td>
        <td>Object</td>
        <td></td>
    </tr>
    <tr>
        <td>Error</td>
        <td></td>
        <td>Collection of <a href="/Guias/Tipos de datos/DetalleError.md">DetalleError</a></td>
        <td>-</td>
    </tr>
    <tr>
        <td>CodigoError</td>
        <td>Contiene el codigo HTTP</td>
        <td>Integer</td>
        <td>-</td>
    </tr>
</table>
<h3>Formato ejemplo</h3>

```
    {
    "Data": {
        "puntoVentaID": 0
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