<body>
  <h1 align="center">POST Factura/AutorizarMovimiento</h1>
  
Primero busca el movimieto y luego si lo encuentra intenta autorizarlo , en caso de no poder devuelve un mensaje informativo de error
  
  <h2 align="center">URL del Resource</h2>
  
  https://www.tangofactura.com/Factura/AutorizarMovimiento
  
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
      <td>MovimientoId</td>
      <td>Obtiene ó Setea el indentificador(ID) del movimiento</td>
      <td>int</td>
      <td>Si</td>
      <td></td>
  </tr>
  <tr>
      <td>CAICAE</td>
      <td>CAI (código de autorización de impresión), CAE (código de autorización electronico)</td>
      <td>String</td>
      <td>Si</td>
      <td>Lo otorga AFIP al autorizar la emisión de un comprobante por web service.</td>
  </tr>
  <tr>
      <td>NroFactura</td>
      <td>Obtiene ó Setea el numero de la factura</td>
      <td>int</td>
      <td>Si</td>
      <td>-</td>
  </tr>
  <tr>
      <td>FechaComprobante</td>
      <td>Obtiene o Setea la fecha del comprobante</td>
      <td>date</td>
      <td>Si</td>
      <td>-</td>
  </tr>
  <tr>
      <td>MovimientoCuotasID</td>
      <td>Obtiene ó Setea la lista de cuotas mediante el identificador (ID)</td>
      <td>IList of string</td>
      <td>Si</td>
      <td>-</td>
  </tr>
  <tr>
      <td>ObtenerInfoAplicaciones</td>
      <td>Indica si el resultado debe incluir la info de la aplicación utilizada para crear el movimiento</td>
      <td>boolean</td>
      <td>-</td>
      <td>-</td>
  </tr>
  <tr>
    <td>OrderID</td>
    <td>-</td>
    <td>int</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>DepositoID</td>
    <td>-/td>
    <td>int</td>
    <td>-</td>
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
      "MovimientoId": 1,
      "CAICAE": "1245398745687542",
      "NroFactura": 2,
      "FechaComprobante": "2021-03-17T18:46:18.881059+00:00",
      "MovimientoCuotasID": [
          "sample string 1"
      ],
      "ObtenerInfoAplicaciones": true,
      "OrderID": 1,
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