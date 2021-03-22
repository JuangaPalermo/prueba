<h1 align="center">POST Factura/ListarImpuestosIIBB</h1>

Obtiene una lista de ingreso bruto en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/ListarImpuestosIIBB

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
    <td>TipoImpuestoID</td>
    <td>Obtiene o setea el identificador (ID) del tipo de impuesto</td>
    <td>int</td>
    <td>Si</td>
    <td>Los valores pueden ser: <br>1. IVA <br>2. Percepciones IIBB <br>3. Otros <br>4. Imp. Internos <br>5. Percepcion IVA</td>
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
    {
        "TipoImpuestoID": 1,
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
        <td>-</td>
        <td>Object</td>
        <td></td>
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
            "TipoImpuestoCodigo": 0,
            "ImpuestoID": 0
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