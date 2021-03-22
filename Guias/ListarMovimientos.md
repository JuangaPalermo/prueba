  <h1 align="center">POST Factura/ListarMovimientos</h1>
  
  Obtiene una lista de movimientos en Tango factura.
  
  <h2 align="center">URL del Resource</h2>
  
  https://www.tangofactura.com/Factura/ListarMovimientos
  
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
    <td>Desde</td>
    <td>Se utiliza como filtro para saber desde que Fecha buscar</td>
    <td>date</td>
    <td>Si</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Hasta</td>
    <td>Se utiliza como filtro para saber hasta que Fecha buscar</td>
    <td>date</td>
    <td>Si</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Tope</td>
    <td>Obtiene o Setea el Tope</td>
    <td>int</td>
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
      "Desde": "2021-03-18T19:31:11.331263+00:00",
      "Hasta": "2021-03-18T19:31:11.331263+00:00",
      "Tope": 3,
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
      "Data": { },
      "Error": [
        {
          "Mensaje": "Error 404",
          "Nivel": 1
        }
      ],
      "CodigoError": 2
    }
  ```
