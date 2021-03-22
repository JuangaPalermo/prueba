<h1 align="center">POST Factura/CrearLoteProductos</h1>

Crea un lote de productos en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/CrearLoteProductos

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
    <td>Productos</td>
    <td>Obtiene una lista de productos</td>
    <td>IList of <a href="CrearProducto.md">ProductoModel</a></td>
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
    {
        "Productos": [
            {
            "ProductoId": 1,
            "ProductoCodigo": "sample string 1",
            "ProductoCodigoAlternativo": "sample string 2",
            "ProductoNombre": "Producto 1",
            "ProductoDescripcion": "Producto incial",
            "ProductoPrecioFinal": 3.0,
            "ProductoPrecioFinalCompra": 4.0,
            "ProductoPublicado": true,
            "ProductoTipo": 6,
            "CrearAunRepetido": true,
            "ProductoImagenes": [
                "sample string 1"
            ],
            "ProductoPerfil": 1,
            "UserIdentifier": "",
            "ApplicationPublicKey": "",
            "Token": ""
            }
        ],
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