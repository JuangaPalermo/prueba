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
    <li>Registrate en <a href="http://www.tangofactura.com">Tango Factrura</a>.</li>
    <li>Crea tu aplicacion haciendo click <a href="https://www.tangofactura.com/PGR/Aplicaciones">aqui</a> (O segui los pasos de nuestra <a href="./Guias/CreacionDeAplicaciones.md">Guia para creacion de aplicaciones</a>).</li> 
    <li>Lea la documentacion detallada en este repositorio para entender el alcance de sus posibilidades.</li> 
</ol>

<a name="facturacion"></a>

## Documentacion de metodos de facturacion 📋

Todas las URIs derivan de *https://www.tangofactura.com/Factura*

<!--
    poner en metodo el hipervinculo al documento del metodo
    en verbo va el verbo del HTTP Request
    en ruta va la tura del request
    descripcion lo que hace el metodo
-->

| Metodo           | Verbo                                                                                                | Ruta request                                     | Descripcion                       |
| ---------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------ | --------------------------------- |
| _CrearFactura_   | **POST**                                                                                             | /CrearFactura                                    | Crea una factura.                 |
| _CategoriesApi_  | [**SitesSiteIdCategoriesGet**](docs/CategoriesApi.md#sitessiteidcategoriesget)                       | **GET** /sites/{site_id}/categories              | Return a categories by site.      |
| _CategoriesApi_  | [**SitesSiteIdDomainDiscoverySearchGet**](docs/CategoriesApi.md#sitessiteiddomaindiscoverysearchget) | **GET** /sites/{site_id}/domain_discovery/search | Predictor                         |
| _ItemsApi_       | [**ItemsIdGet**](docs/ItemsApi.md#itemsidget)                                                        | **GET** /items/{id}                              | Return a Item.                    |
| _ItemsApi_       | [**ItemsIdPut**](docs/ItemsApi.md#itemsidput)                                                        | **PUT** /items/{id}                              | Update a Item.                    |
| _ItemsApi_       | [**ItemsPost**](docs/ItemsApi.md#itemspost)                                                          | **POST** /items                                  | Create a Item.                    |
| _ItemsHealthApi_ | [**ItemsIdHealthActionsGet**](docs/ItemsHealthApi.md#itemsidhealthactionsget)                        | **GET** /items/{id}/health/actions               | Return item health actions by id. |
| _ItemsHealthApi_ | [**ItemsIdHealthGet**](docs/ItemsHealthApi.md#itemsidhealthget)                                      | **GET** /items/{id}/health                       | Return health by id.              |
| _ItemsHealthApi_ | [**SitesSiteIdHealthLevelsGet**](docs/ItemsHealthApi.md#sitessiteidhealthlevelsget)                  | **GET** /sites/{site_id}/health_levels           | Return health levels.             |
| _OAuth20Api_     | [**Auth**](docs/OAuth20Api.md#auth)                                                                  | **GET** /authorization                           | Authentication Endpoint           |
| _OAuth20Api_     | [**GetToken**](docs/OAuth20Api.md#gettoken)                                                          | **POST** /oauth/token                            | Request Access Token              |

```
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

## Expresiones de Gratitud 🎁

- Comenta a otros sobre este proyecto 📢
- Invita una cerveza 🍺 o un café ☕ a alguien del equipo.
- Da las gracias públicamente 🤓.
- etc.

---

⌨️ con ❤️ por [Villanuevand](https://github.com/Villanuevand) 😊
