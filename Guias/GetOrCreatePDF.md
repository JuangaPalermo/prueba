<h1 align="center">GET Factura/GetOrCreatePDF?preferencia={preferencia}</h1>

Crea u obtiene el PDF segun la preferencia especificada

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/GetOrCreatePDF?preferencia={preferencia}

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
    <td>preferencia</td>
    <td>Enumerado que define la accion que se quiere tomar segun la opcion seleccionada</td>
    <td><a href="/Guias/Tipos de datos/PreferenciaImpresion.md"></a>PreferenciaImpresion</td>
    <td>Si</td>
    <td>Sus valores pueden ser: <br>0 - Impresion <br>1 - Visualizacion/Descarga</td>
</tr>
</table>

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
        <td>Muestra una lista de mensajed de error</td>
        <td>IList of <a href="/Guias/Tipos de datos/DetalleError.md">DetalleError</a></td>
        <td></td>
    </tr>
    <tr>
        <td>CodigoError</td>
        <td>Muestra el codigo de error</td>
        <td>int</td>
        <td></td>
    </tr>
    <tr>
        <td>ContentEncoding</td>
        <td>-</td>
        <td><a href="/Guias/Tipos de datos/Encoding.md">Encoding</a></td>
        <td></td>
    </tr>
    <tr>
        <td>ContentType</td>
        <td></td>
        <td>string</td>
        <td></td>
    </tr>
    <tr>
        <td>Data</td>
        <td></td>
        <td>Object</td>
        <td></td>
    </tr>
    <tr>
        <td>JsonRequestBehavior</td>
        <td></td>
        <td><a href="/Guias/Tipos de datos/JsonRequestBehavior.md">JsonRequestBehavior</a></td>
        <td></td>
    </tr>
    <tr>
        <td>MaxJsonLength</td>
        <td></td>
        <td>int</td>
        <td></td>
    </tr>
    <tr>
        <td>RecursionLimit</td>
        <td></td>
        <td>int</td>
        <td></td>
    </tr>
</table>

<h3>Formato ejemplo</h3>

```
    {
    "Error": [
      {
        "Mensaje": "Error 404",
        "Nivel": 1
      }
    ],
    "CodigoError": 1,
    "ContentType": "sample string 2",
    "Data": {},
    "JsonRequestBehavior": 0,
    "MaxJsonLength": 1,
    "RecursionLimit": 1
    }
```