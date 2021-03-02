<body>
<h1 align="center">POST Factura/CrearFactura</h1>

Crea una nueva factura en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/CrearFactura

<h2 align="center">Request</h2>

<h3>Parametros</h3>
<table style="text-align: center;">
<tr>
    <th>Nombre</th>
    <th>Descripcion</th>
    <th>Tipo</th>
    <th>Obligatorio</th>
    <th>Informacion Adicional</th>
</tr>
<tr>
    <td>Letra</td>
    <td>Obtiene o Setea la letra del comprobante</td>
    <td>String</td>
    <td>Si</td>
    <td>Sus valores pueden ser: A - B - C - M</td>
</tr>
<tr>
    <td>ClienteCodigo</td>
    <td>Obtiene o Setea el codigo del cliente</td>
    <td>String</td>
    <td>Si</td>
    <td>Longitud máxima: 10 caracteres.</td>
</tr>
<tr>
    <td>ClienteNombre</td>
    <td>Obtiene o Setea el nombre del cliente</td>
    <td>String</td>
    <td>Si</td>
    <td>-</td>
</tr>
<tr>
    <td>ClienteDireccion</td>
    <td>Obtiene o Setea la direccion del cliente</td>
    <td>String</td>
    <td>Solo si la letra de factura es A, o si el importe es superior a 1000 pesos.</td>
    <td>-</td>
</tr>
</table>

<h3>Formato</h3>

<h2 align="center">Response</h2>

</body>