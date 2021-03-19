<body>
<h1 align="center">POST Factura/CrearCliente</h1>

Crea a un cliente en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/CrearCliente

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
    <td>ClienteId</td>
    <td>Obtiene ó Setea el ID(Identificador) del cliente</td>
    <td>int</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>ClienteCodigoAlternativo</td>
    <td>Gets or sets the cliente codigo alternativo.</td>
    <td>string</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>ClientePerfil</td>
    <td>Obtiene ó Setea el ID(Identificador) del perfil.</td>
    <td>int</td>
    <td>Si</td>
    <td>1: Cliente <br>2: Proveedor <br>3: Cliente/Proveedor</td>
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
    <td>ClienteTipoDocumento</td>
    <td>Obtiene o Setea el tipo de documento del cliente</td>
    <td>int?</td>
    <td></td>
    <td>Valores posibles: <br> DNI 1 <br> CUIT 2 <br> CI 3 <br> LE 4 <br> LC 5 <br> CUIL 6</td>
</tr>
<tr>
    <td>ClienteNumeroDocumento</td>
    <td>Obtiene ó Setea el número de documento del cliente.</td>
    <td>string</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>ClienteDireccion</td>
    <td>Obtiene o Setea la direccion del cliente</td>
    <td><a href="Tipos de datos/ClienteDireccionModel.md">ClienteDireccionModel</a></td>
    <td>No</td>
    <td>-</td>
</tr>
<tr>
    <td>ClienteEmail</td>
    <td>Obtiene ó Setea el email del cliente.</td>
    <td>IList of <a href="Tipos de datos/ClienteEmailModel.md">ClienteEmailModel</a></td>
    <td>No</td>
    <td>A esta dirección se le enviará el comprobante electrónico luego de aprobarse.</td>
</tr>
<tr>
    <td>CategoriaImpositivaCodigo</td>
    <td>Obtiene ó Setea la categoria impositiva.</td>
    <td>String</td>
    <td>Si</td>
    <td>Puede ser: </br> EX: Exento</br> MT: Responsable Monotributo </br> CF: Consumidor Final</br> RI: Responsable Inscripto</td>
</tr>
<tr>
    <td>ClientePerfilImpositivoCodigo</td>
    <td>Gets or sets the cliente perfil impositivo codigo.</td>
    <td>String</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>CrearAunRepetido</td>
    <td>Indica que un cliente debe ser creado, aunque ya exista otro con el mismo codigo o tipo y numero de documento.</td>
    <td>boolean</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>AplicacionID</td>
    <td>Obtiene el identificador de la aplicacion.</td>
    <td>int</td>
    <td>Si</td>
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
  No disponible
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
        "ClienteID": 0
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
</body>