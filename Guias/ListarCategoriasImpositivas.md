<h1 align="center">POST Factura/ListarCategoriasImpositivas</h1>

Obtiene una listas de categoria impositiva posibles de los comprobantes de Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/ListarCategoriasImpositivas

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
        "Data": {},
        "Error": [
        {
            "Mensaje": "Error 404",
            "Nivel": 1
        }
        ],
        "CodigoError": 2
    }
```