<h1 align="center">POST Factura/ListarPerfilesFacturacion</h1>

Lista los IDs de los perfiles de facturación dados de alta por el usuario en Tango factura. Estos IDs pueden utilizarse en los métodos de creación de comprobantes, para indicar que esta es la configuración a utilizar durante la emisión.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/ListarPerfilesFacturacion

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
        <td>-</td>
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
        "ContentType": "sample string 1",
        "Data": {},
        "JsonRequestBehavior": 0,
        "MaxJsonLength": 1,
        "RecursionLimit": 1
    }
```