<h1 align="center">
  <a href=https://www.tangofactura.com/Help>
    <img src="/Imagenes/logo.jpg" alt="Tango Factura Developers" width="300"></a>
  </a>
  <br>
  Tango Factura API
  <br>
</h1>

<h4 align="center">Esta es la documentacion oficial de la API de Tango Factura, servicio de facturacion</h4>

<a name="introduccion"></a>
[Tango factura](http://www.tangofactura.com) ha desarrollado servicios WEB que proveen a terceros de una forma simple de interactuar con los datos y la funcionalidad del sistema.

Si queres crear aplicaciones que necesiten de emitir comprobantes electronicos; esta es tu mejor opcion para obtenerlo e incorporarlo a tu proyecto.

Agrega, sin esfuerzo, el modulo de facturacion a tu sistema gracias a las API de integracion que se exponen en esta guia.

<a name="comenzando"></a>

## Comenzando 🚀

Para comenzar a registar tus aplicaciones, segui los siguientes pasos:

<ol>
    <li>Registrate en <a href="http://www.tangofactura.com">Tango Factura</a>.</li>
    <li>Crea tu aplicacion haciendo click <a href="https://www.tangofactura.com/PGR/Aplicaciones">aqui</a> (O segui los pasos de nuestra <a href="./Guias/CreacionDeAplicaciones.md">Guia para creacion de aplicaciones</a>).</li> 
    <li>Lea la documentacion detallada en este repositorio para entender el alcance de sus posibilidades.</li> 
</ol>

<a name="facturacion"></a>

## Documentacion de metodos de facturacion 📋

Todas las URIs derivan de <i>https://www.tangofactura.com/Factura</i>

<!--
    poner en metodo el hipervinculo al documento del metodo
    en verbo va el verbo del HTTP Request
    en ruta va la tura del request
    descripcion lo que hace el metodo
-->

<table style="width:100%">

  <tr>
    <th>Metodo</th>
    <th>Verbo</th>
    <th>Ruta request</th>
    <th>Descripcion</th>
  </tr>
  <tr>
    <td><a href="/Guias/CrearFactura.md"><i>CrearFactura</i></a></td>
    <td><b>POST</b></td>
    <td>/CrearFactura</td>
    <td>Crea una factura.</td>
  </tr>
  <tr>
    <td><a href="/Guias/GetOrCreatePDF.md"><i>GetOrCreatePDF</i></a></td>
    <td><b>GET</b></td>
    <td>/GetOrCreatePDF?preferencia={preferencia}</td>
    <td>Obtiene o crea el PDF (segun preferencia)</td>
  </tr>
  <tr>
    <td><i>CrearLoteMovimientos</i></td>
    <td><b>POST</b></td>
    <td>/CrearLoteMovimientos</td>
    <td>Crea una lista de comprobantes en Tango factura.</td>
  </tr>
  <tr>
    <td><i>AutorizarLoteMovimientos</i></td>
    <td><b>POST</b></td>
    <td>/AutorizarLoteMovimientos</td>
    <td>Autoriza el lote de movimientos en Tango factura</td>
  </tr>
  <tr>
    <td><i>TotalFacturacionMovimientos</i></td>
    <td><b>POST</b></td>
    <td>/TotalFacturacionMovimientos</td>
    <td>Obitene el total de la facturacion</td>
  </tr>
  <tr>
    <td><i>VistaPreviaMovimiento</i></td>
    <td><b>POST</b></td>
    <td>/VistaPreviaMovimiento</td>
    <td>Muestra la vista previa del comprobante</td>
  </tr>
  <tr>
    <td><i>CrearCredito</i></td>
    <td><b>POST</b></td>
    <td>/CrearCredito</td>
    <td>Crea una nota de credito relacionado a una factura en Tango factura.</td>
  </tr>
  <tr>
    <td><i>CrearCreditoACuenta</i></td>
    <td><b>POST</b></td>
    <td>/CrearCreditoACuenta</td>
    <td>Crea una nota de credito sin relacion con un factura de venta en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarMovimientosQueVencenHoy</i></td>
    <td><b>POST</b></td>
    <td>/ListarMovimientosQueVencenHoy</td>
    <td>Obtiene una lista los comprobantes que vencen el dia de la fecha en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarMovimientos</i></td>
    <td><b>POST</b></td>
    <td>/ListarMovimientos</td>
    <td>Obtiene una lista de movimientos en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarAlicuotas</i></td>
    <td><b>POST</b></td>
    <td>/ListarAlicuotas</td>
    <td>Obtiene una lista de alicuotas con su respectivo codigo, nombre , porcentaje en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ObtenerInfoMovimiento</i></td>
    <td><b>POST</b></td>
    <td>/ObtenerInfoMovimiento</td>
    <td>Obtiene toda la informacion de un comprobante en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ObtenerInfoMovimientosPorNroFactura</i></td>
    <td><b>POST</b></td>
    <td>/ObtenerInfoMovimientosPorNroFactura</td>
    <td>Obtiene la informacion del comprobante por medio del numero de la factura en Tango factura.</td>
  </tr>
  <tr>
    <td><i>AutorizarMovimiento</i></td>
    <td><b></b></td>
    <td>/AutorizarMovimiento</td>
    <td>Primero busca el movimieto y si lo encuentra intenta autorizarlo</td>
  </tr>
  <tr>
    <td><i>CrearCliente</i></td>
    <td><b>POST</b></td>
    <td>/CrearCliente</td>
    <td>Crea a un cliente en Tango factura.</td>
  </tr>
  <tr>
    <td><i>CrearLoteClientes</i></td>
    <td><b>POST</b></td>
    <td>/CrearLoteClientes</td>
    <td>Crea una lista de clientes en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ModificarCliente</i></td>
    <td><b>POST</b></td>
    <td>/ModificarCliente</td>
    <td>Modifica los datos del cliente en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarClientes</i></td>
    <td><b>POST</b></td>
    <td>/ListarClientes</td>
    <td>Obtiene la lista de clientes existentes en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarTiposDocumento</i></td>
    <td><b>POST</b></td>
    <td>/ListarTiposDocumento</td>
    <td>Listar tipos de documento existentes en Tango factura, conteniendo el codigo y la descricion del tipo de documento.</td>
  </tr>
  <tr>
    <td><i>ObtenerCategoriaImpositivaEmpresa</i></td>
    <td><b>POST</b></td>
    <td>/ObtenerCategoriaImpositivaEmpresa</td>
    <td>Obtiene la categoria impositiva de la empresa en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarProvincias</i></td>
    <td><b>POST</b></td>
    <td>/ListarProvincias</td>
    <td>Obtiene una lista de provincias en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ObtenerDatosContribuyente</i></td>
    <td><b>POST</b></td>
    <td>/ObtenerDatosContribuyente</td>
    <td>Obtiene los datos del contribuyente en Tango factura.</td>
  </tr>
  <tr>
    <td><i>CrearProducto</i></td>
    <td><b>POST</b></td>
    <td>/CrearProducto</td>
    <td>Crea un producto en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ModificarProducto</i></td>
    <td><b>POST</b></td>
    <td>/ModificarProducto</td>
    <td>Modifica los datos del producto o servicio.</td>
  </tr>
  <tr>
    <td><i>ListarProductos</i></td>
    <td><b>POST</b></td>
    <td>/ListarProductos</td>
    <td>Permite obtener los productos de Tango factura.</td>
  </tr>
  <tr>
    <td><i>CrearLoteProductos</i></td>
    <td><b>POST</b></td>
    <td>/CrearLoteProductos</td>
    <td>Crea un lote de productos en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarImpuestosIIBB</i></td>
    <td><b>POST</b></td>
    <td>/ListarImpuestosIIBB</td>
    <td>Obtiene una lista de ingreso bruto en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarImpuestos</i></td>
    <td><b>POST</b></td>
    <td>/ListarImpuestos</td>
    <td>Obtiene una lista de impuestos en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarEstados</i></td>
    <td><b>POST</b></td>
    <td>/ListarEstados</td>
    <td>Obtiene una lista de estados posibles de los comprobantes de Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarCategoriasImpositivas</i></td>
    <td><b>POST</b></td>
    <td>/ListarCategoriasImpositivas</td>
    <td>Obtiene una listas de categoria impositiva posibles de los comprobantes de Tango factura.</td>
  </tr>
  <tr>
    <td><i>EnviarComprobanteElectronico</i></td>
    <td><b>POST</b></td>
    <td>/EnviarComprobanteElectronico</td>
    <td>Envía el comprobante electrónico indicado por mail.</td>
  </tr>
  <tr>
    <td><i>ObtenerUID</i></td>
    <td><b>POST</b></td>
    <td>/ObtenerUID</td>
    <td>Obtiene el identificador de usuario en Tango factura.</td>
  </tr>
  <tr>
    <td><i>CrearEmpresa</i></td>
    <td><b>POST</b></td>
    <td>/CrearEmpresa</td>
    <td>Crea una empresa en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarPuntosVenta</i></td>
    <td><b>POST</b></td>
    <td>/ListarPuntosVenta</td>
    <td>Obtiene una lista de puntos de venta en Tango factura.</td>
  </tr>
  <tr>
    <td><i>CrearPuntoVenta</i></td>
    <td><b>POST</b></td>
    <td>/CrearPuntoVenta</td>
    <td>Crea un de punto de venta en Tango factura.</td>
  </tr>
  <tr>
    <td><i>ListarPerfilesFacturacion</i></td>
    <td><b>POST</b></td>
    <td>/ListarPerfilesFacturacion</td>
    <td>Lista los IDs de los perfiles de facturación dados de alta por el usuario en Tango factura</td>
  </tr>
  <tr>
    <td><i>ObtenerConfiguracionEmpresa</i></td>
    <td><b>POST</b></td>
    <td>/ObtenerConfiguracionEmpresa</td>
    <td>Obtiene la configuracion de una empresa en Tango factura.</td>
  </tr>

</table>

## Ejemplos de uso 🎁

<ul>
  <li><a href="http://resources.tangofactura.com/downloads/SDK.CSharp.rar">SDK C#</a></li>
  <li><a href="http://resources.tangofactura.com/downloads/SDK.PHP.rar">SDK PHP</a></li>
</ul>

## Control de versiones 🔧

Nuestra API se actualiza constantemente, para brindar nuevas funcionalidades! Podés revisar estas modificaciones
en los commits de este mismo repositorio, o dirigirte a nuestro <a href="/Control de versiones/RegistroDeModificaciones.md">Registro de modificaciones</a>

<!-- ```
Da un ejemplo
```

### Instalación 🔧

_Una serie de ejemplos paso a paso que te dice lo que debes ejecutar para tener un entorno de desarrollo ejecutandose_

_Dí cómo será ese paso_

```
Da un ejemplo
```

_Y repite_

```
hasta finalizar
```

_Finaliza con un ejemplo de cómo obtener datos del sistema o como usarlos para una pequeña demo_

## Ejecutando las pruebas ⚙️

_Explica como ejecutar las pruebas automatizadas para este sistema_

### Analice las pruebas end-to-end 🔩

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

### Y las pruebas de estilo de codificación ⌨️

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

## Despliegue 📦

_Agrega notas adicionales sobre como hacer deploy_

## Construido con 🛠️

_Menciona las herramientas que utilizaste para crear tu proyecto_

- [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - El framework web usado
- [Maven](https://maven.apache.org/) - Manejador de dependencias
- [ROME](https://rometools.github.io/rome/) - Usado para generar RSS

## Contribuyendo 🖇️

Por favor lee el [CONTRIBUTING.md](https://gist.github.com/villanuevand/xxxxxx) para detalles de nuestro código de conducta, y el proceso para enviarnos pull requests.

## Wiki 📖

Puedes encontrar mucho más de cómo utilizar este proyecto en nuestra [Wiki](https://github.com/tu/proyecto/wiki)

## Versionado 📌

Usamos [SemVer](http://semver.org/) para el versionado. Para todas las versiones disponibles, mira los [tags en este repositorio](https://github.com/tu/proyecto/tags).

## Autores ✒️

_Menciona a todos aquellos que ayudaron a levantar el proyecto desde sus inicios_

- **Andrés Villanueva** - _Trabajo Inicial_ - [villanuevand](https://github.com/villanuevand)
- **Fulanito Detal** - _Documentación_ - [fulanitodetal](#fulanito-de-tal)

También puedes mirar la lista de todos los [contribuyentes](https://github.com/your/project/contributors) quíenes han participado en este proyecto.

## Licencia 📄

Este proyecto está bajo la Licencia (Tu Licencia) - mira el archivo [LICENSE.md](LICENSE.md) para detalles



- Comenta a otros sobre este proyecto 📢
- Invita una cerveza 🍺 o un café ☕ a alguien del equipo.
- Da las gracias públicamente 🤓.
- etc.

---

⌨️ con ❤️ por [Villanuevand](https://github.com/Villanuevand) 😊 -->
