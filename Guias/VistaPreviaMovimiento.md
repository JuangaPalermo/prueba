<body>
<h1 align="center">POST Factura/VistaPreviaMovimiento</h1>

Muestra la vista previa del comprobante

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/VistaPreviaMovimiento

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
<tr>
    <td>ClienteDireccionExtendida</td>
    <td>Obtiene ó Setea la dirección extendida del cliente.</td>
    <td><a href="/Guias/Tipos de datos/ClienteDireccionModel.md">ClienteDireccionModel</a></td>
    <td>Solo si la letra de factura es A, o si el importe es superior a 1000 pesos.</td>
    <td>-</td>
</tr>
<tr>
    <td>RegimenDatosFce</td>
    <td>Obtiene ó Setea RegimenDatosFce</td>
    <td><a href="/Guias/Tipos de datos/MovimientoRegimenDatosFCE.md">MovimientoRegimenDatosFCE</a></td>
    <td>-</td>
    <td>-</td>
</tr>
<tr>
  <td>RegimenDatosFEX</td>
  <td>Obtiene ó Setea RegimenDatosFEX</td>
  <td><a href="/Guias/Tipos de datos/MovimientoRegimenDatosFexSerializer.md">MovimientoRegimenDatosFexSerializer</a></td>
  <td>-</td>
  <td>-</td>
</tr>
<tr>
  <td>ClienteTipoDocumento</td>
  <td>Obtiene o Setea el tipo de documento del cliente</td>
  <td>int?</td>
  <td></td>
  <td>Este codigo se obtiene del metodo del servicio "Listar Tipos de documento". Valores posibles: <br> DNI 1 <br> CUIT 2 <br> CI 3 <br> LE 4 <br> LC 5 <br> CUIL 6</td>
</tr>
<tr>
  <td>ClienteNumeroDocumento</td>
  <td>Obtiene ó Setea el número de documento del cliente.</td>
  <td>string</td>
  <td>Si</td>
  <td>Por ejemplo: 30-63165881-0</td>
</tr>
<tr>
  <td>ClienteEmail</td>
  <td>Obtiene ó Setea el email del cliente.</td>
  <td>String</td>
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
  <td>Observacion</td>
  <td>Obtiene ó Setea la observacion.</td>
  <td>String</td>
  <td>No</td>
  <td>Observación del comprobante.</td>
</tr>
<tr>
  <td>DetallesMovimiento</td>
  <td>Obtiene ó Setea la lista de productos/servicios a facturar.</td>
  <td>IList of <a href="/Guias/Tipos de datos/DetallesMovimiento.md">DetallesMovimiento</a></td>
  <td>Si</td>
  <td>Son los renglones del movimiento</td>
</tr>
<tr>
  <td>FechaComprobante</td>
  <td>Obtiene ó Setea la fecha del comprobante.</td>
  <td>DateTime?</td>
  <td>Si</td>
  <td>-</td>
</tr>
<tr>
  <td>FechaServicioDesde</td>
  <td>Obtiene ó Setea la fecha de cuando empieza el servicio.</td>
  <td>DateTime?</td>
  <td>Si</td>
  <td>-</td>
</tr>
<tr>
  <td>FechaServicioHasta</td>
  <td>Obtiene ó Setea la fecha de cuando termia el servicio.</td>
  <td>DateTime?</td>
  <td>Si</td>
  <td>-</td>
</tr>
<tr>
  <td>MovimientoReferenciaID</td>
  <td>Obtiene ó setea el movimiento relacionado para débito.</td>
  <td>int?</td>
  <td>Si</td>
  <td>-</td>
</tr>
<tr>
  <td>TipoMovimiento</td>
  <td>Obtiene o Setea el tipo de movimiento</td>
  <td>enum <a href="/Guias/Tipos de datos/TipoMovimientoForService.md">TipoMovimientoForService</a></td>
  <td>Si</td>
  <td>Valores posibles: <br>FVA <br>CVA <br>DVA</td>
</tr>
<tr>
  <td>PerfilComprobanteID</td>
  <td>Perfil de facturación a utilizar.</td>
  <td>int?</td>
  <td>Si</td>
  <td>Si es null se utiliza el perfil de Facturación automática.</td>
</tr>
<tr>
  <td>OrderID</td>
  <td>Obtiene o Setea el OrderID</td>
  <td>int?</td>
  <td>No</td>
  <td>Se usa para Woocommerce</td>
</tr>
<tr>
  <td>FechaPAsocDesde</td>
  <td>Fecha de inicio del periodo asociado</td>
  <td>DateTime?</td>
  <td>No</td>
  <td>-</td>
</tr>
<tr>
  <td>FechaPAsocHasta</td>
  <td>Fecha de finalizacion del periodo asociado</td>
  <td>DateTime?</td>
  <td>No</td>
  <td>-</td>
</tr>
<tr>
  <td>DescuentoTotal</td>
  <td>Obtiene o Setea el DescuentoTotal</td>
  <td>decimal?</td>
  <td>No</td>
  <td>-</td>
</tr>
<tr>
  <td>DepositoID</td>
  <td>Obtiene o Setea el DepositoID</td>
  <td>int?</td>
  <td>No</td>
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
    "FechaComprobante": "2021-03-02T11:38:30.2908898+00:00",
    "FechaServicioDesde": "2021-03-02T11:38:30.2908898+00:00",
    "FechaServicioHasta": "2021-03-02T11:38:30.2908898+00:00",
    "MovimientoReferenciaID": 1,
    "TipoMovimiento": 1,
    "PerfilComprobanteID": 1,
    "OrderID": 1,
    "FechaPAsocDesde": "2021-03-02T11:38:30.2908898+00:00",
    "FechaPAsocHasta": "2021-03-02T11:38:30.2908898+00:00",
    "DescuentoTotal": 1.0,
    "DepositoID": 1,
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
      "MovimientoId": 0,
      "Grabado": false,
      "Electronico": false,
      "EstadoId": 0,
      "FechaEmision": "0001-01-01T00:00:00",
      "FechaVencimiento": "0001-01-01T00:00:00",
      "TotalIVA": 0.0,
      "TotalOtrosImpuestos": 0.0,
      "Total": 0.0,
      "Subtotal": 0.0
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