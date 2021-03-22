<h1 align="center">POST Factura/CrearEmpresa</h1>

Crea una empresa en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/CrearEmpresa

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
    <td>UsuarioNombre</td>
    <td>Obtiene ó Setea el nombre del usuario.</td>
    <td>string</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>UsuarioApellido</td>
    <td>Obtiene ó Setea el apellido del usuario.</td>
    <td>string</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>EmpresaEmail</td>
    <td>Obtiene ó Setea el email del usuario.</td>
    <td>string</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>ClienteCodigo</td>
    <td>Obtiene o Setea el codigo del cliente</td>
    <td>String</td>
    <td>Si</td>
    <td>Longitud máxima: 10 caracteres.</td>
</tr>
<tr>
    <td>EmpresaRazonSocial</td>
    <td>Obtiene ó Setea la razon social de la empresa .</td>
    <td>String</td>
    <td>Si</td>
    <td>-</td>
</tr>
<tr>
    <td>EmpresaCUIT</td>
    <td>Obtiene ó Setea el Cuit de la empresa</td>
    <td>string</td>
    <td>Si</td>
    <td></td>
</tr>
<tr>
    <td>EmpresaCategoriaImpositivaID</td>
    <td>Obtiene ó Setea el numero identificador (ID) para la categoria de la empresa.</td>
    <td>int</td>
    <td>Si</td>
    <td>Valores posibles: <br>1: IVA Responsable Inscripto<br>2: IVA Responsable no Inscripto<br>3: IVA no Responsable<br>4: IVA Sujeto Exento<br>5: Consumidor Final<br>6: Responsable Monotributo<br>7: Sujeto no Categorizado<br>8: Proveedor del Exterior<br>9: Cliente del Exterior<br>10: IVA Liberado – Ley Nº 19.640<br>11: IVA Responsable Inscripto – Agente de Percepción<br>12: Pequeño Contribuyente Eventual<br>13: Monotributista Social<br>14: Pequeño Contribuyente Eventual Social</td>
</tr>
<tr>
    <td>EmiteComprobantesElectronicos</td>
    <td>Se utliza para saber si el punto de venta emite comprobantes electronicos.</td>
    <td>Boolean</td>
    <td>Si</td>
    <td>-</td>
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
    "UsuarioNombre": "Usuario nombre 1 ",
    "UsuarioApellido": "Usuario apellido 1 ",
    "EmpresaEmail": "usuario@axoft.com ",
    "EmpresaRazonSocial": "Usuario apellido 1 ",
    "EmpresaCUIT": "30-63165881-0",
    "EmpresaCategoriaImpositivaID": 1,
    "EmiteComprobantesElectronicos": true,
    "Permission": 0,
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
        "EmpresaID": 0,
        "UsuarioSistemaID": 0
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