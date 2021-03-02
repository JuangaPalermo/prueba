<body>
<h1 align="center">POST Factura/CrearFactura</h1>

Crea una nueva factura en Tango factura.

<h2 align="center">URL del Resource</h2>

https://www.tangofactura.com/Factura/CrearFactura

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
        <td>Collection of DetalleError</td>
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