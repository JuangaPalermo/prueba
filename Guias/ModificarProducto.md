<body>
    <h1 align="center">POST Factura/ModificarProducto</h1>
    
    Modifica los datos del producto o servicio.
    
    <h2 align="center">URL del Resource</h2>
    
    https://www.tangofactura.com/Factura/ModificarProducto
    
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
        <td>ProductoId</td>
        <td>Obtiene el ID(Identificador) del producto que puede ser nuleable.</td>
        <td>int?</td>
        <td>Si</td>
        <td></td>
    </tr>
    <tr>
        <td>ProductoCodigo</td>
        <td>Obtiene ó Setea el codigo del producto.Utilizado por los usuarios para identificar unívocamente los conceptos dentro de Tango factura.</td>
        <td>String</td>
        <td>Si</td>
        <td></td>
    </tr>
    <tr>
        <td>ProductoCodigoAlternativo</td>
        <td>Código que identifica al cliente en el consumidor del servicio de facturación.</td>
        <td>string</td>
        <td>Si</td>
        <td>-</td>
    </tr>
    <tr>
        <td>ProductoNombre</td>
        <td>Obtiene ó Setea el nombre del producto.</td>
        <td>string</td>
        <td>Si</td>
        <td>-</td>
    </tr>
    <tr>
        <td>ProductoDescripcion</td>
        <td>Obtiene ó Setea la descripcion del producto.</td>
        <td>string</td>
        <td>Si</td>
        <td>-</td>
    </tr>
    <tr>
        <td>ProductoPrecioFinal</td>
        <td>Obtiene ó Setea el precio final del producto.</td>
        <td>decimal</td>
        <td>Si</td>
        <td>-</td>
    </tr>
    <tr>
        <td>ProductoPrecioFinalCompra</td>
        <td>Obtiene ó Setea el precio final de la compra.</td>
        <td>decimal</td>
        <td>Si</td>
        <td>-</td>
    </tr>
    <tr>
      <td>ProductoPublicado</td>
      <td>Reservado. Indica si el producto se encuentra publicado</td>
      <td>boolean</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <td>ProductoTipo</td>
      <td>Obtiene ó Setea el tipo del producto.</td>
      <td>int</td>
      <td>Si</td>
      <td>Valores posibles: <br>1: Producto <br>2: Servicio <br>3: Prod/Serv</td>
    </tr>
    <tr>
        <td>CrearAunRepetido</td>
        <td>Se utiliza para crear producto repetido o sobre escribirlo.</td>
        <td>boolean</td>
        <td>-</td>
        <td>-</td>
    </tr>
    <tr>
        <td>ProductoImagenes</td>
        <td>Lista con las URL de las imagenes del producto</td>
        <td>IList of string</td>
        <td>-</td>
        <td>-</td>
    </tr>
    <tr>
        <td>ProductoPerfil</td>
        <td>Obtiene o Setea el perfil del producto</td>
        <td>int</td>
        <td>-</td>
        <td>Valores posibles: <br>1: Venta <br>2: Compra <br>3: Compra/Venta</td>
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
    ```
    
    <h2 align="center">Response</h2>

    Devuelve 0 en caso de haber modificado los valores con éxito, caso contrario devuelve 1.

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
            "ProductoId": 0
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