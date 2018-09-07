Arquitectura de web components
	* Reutilizable
	* Desacopable
	* alta cohesion
	* Bajo acoplamiento

Caracteristicas de un componente
	* Encapsulación
	* Resusable
	* Reemplazable
	* Extensible/Personalizable
	* Independiente

Ciclo de vida de desarrollo de components
	* Requerimientos
	* Diseño
	* Implementacion
	* Integracion
	* Testing
	* Liberacion
	* Mantenimiento


Page Pattern

Organizacion del proyecto
	* Tamaño del proyecto
	* Patrón de Arquitectura (PRP patthern)
	* Organización y división de components


Ecosistema REACT

	* Programacion funcional
	* Virtual DOM
	* One way data binding
	* Lear once 

Categoria de Eventos
	* Mounting
	* Updating
	* Unmounting

Componentes Smart
	* No tiene estado
	* Solo recibe datos y procesa para hacer un render html simple
	* Operaciones o logica de negocio

JSX
	class => className
	for => htmlFor


Webpack
	* Depedency Graph
	* Build of bundles

Como funciona
	* Entry
	* Outputs: salida de archivos procesados
	* Loaders: Se encarga de procesar los archivos requeridos apartir de los entry points.
		- test: expression para el nombre del archivo 
	* Plugins
	* Substitutions: Son comodines o templates que se pueden aplicar al nombre de archivos de salida.



Por default webpack.config.js es el archivo de configuracion de webpack




Formas de enviar datos a los components
Props
	componentes funciones se accede a propiedades por props, las propiedades no se pueden alterar
	
States
	Se define informacion interna del componente y si pueden ser alteradas.

One way binding - Tipo de estado
	




Sesion 2 REACT
loaders css, sass, miniextraccss

Loaders: aplican transformaciones
Plugins: Funcionalidad nueva

Agregando estilos a componentes
 * atributo style (estilos en formato camelCase)
 * atributo className

CSS Modules
	*	se configuran options en webpack para definir un
		options y definir el uso de modulos


Componentes Responsivos
	* Definir estilos genericos
	* Definirn estilos especificos

Tecnicas: 
	* Grid and Flexbox
	* Media Queries
	* Element queries/ Container queries

Eventos 
	Proxy ES6

Los eventos se forman con camelCase

Declaracion de events onEvent

Eventos sinteticos 


Manejo de errores
	Error boundaries
Captura los errores de UI, solo aplican sobre el render, constructor o el lifecyle

Implementar
componentDidCatch(error, info)


----------------------------------------------------------------------------------
Tipos de componentes

Smart 
	* Logica de negocio
	* Procesamiento de datos
	* Tiene un estado representado por una clase
	* Soporte de Callbacks



Dumb Components
	* Solo UI
	* Iteracion o representacion de datos en el UI
	* props.children
	* representado solo por una funcion


Props Children => Native Slot


----------------------------------------------------------------------------------
High Order Components

Es una funcion que recibe un componente como parametro y regresa un componente con propiedades o funciones.


----------------------------------------------------------------------------------

Tablas
	* 
Forms
	* Crear formulario con inputs encapsulados 
Modals
	* 
Router
	* exact y path react-router-dom
Create Portal
	* 
Autenticacion




Poncho - Accesibilidad
Joel - Progresive web app


3 semanas

# React Container
## Three Shaking
	Eliminar pedasos de codigo inecesarios del bundle
	Se basa en la sintaxis import y export

	Side effects en false para eliminar fragmentos inecesarios.

## Bundle optimitation
	* Construcción del bundle
	* Bundle mas pequeño
	* Construir solo lo necesario

Como ?
	* DLL Plugin -> Evita recompilar librerias que no cambiaran
	* splitchunks -> 

## PRPL Pattern
 Patron para estructurar y servir PWA enfocado en performance y entrega y carga
	* Push recursos criticos para la ruta url inicial
	* Render ruta inicial
	* pre-cache rutas restantes
	* lazy loading: carga de rutas dinamicas

### Estructurar
	* entry points
		- dependencias minimas para funcionar
		- Polyfills
		- rutas absolutas para dependencias
	* shell logica de alto nivel y routing
		- responsable de enrutamiento y la ui de navegacion
		- carga de componentes lazy
		- dependencias de inicio para el pintado
	* fragments codigo para cada vista
		- referencias compartidas

## Critical rendering path
	* TTI
	* eficiencia de caching
	* Simplicidad de desarrollo y deployment	


## Code spliting
	Es una tecnica que nos permite dividir nuestro codigo en varios bundles que seran cargados bajo demanda o en paralelo.
	Ventajas: impacto significativo en la carga de recursos.

	* 1 o mas bundles, primero las dependencias compartidas

Enfoques
	* entry points
	* prevent duplication
	* dynamic imports

## Lazy Componentes
Tecnica para cargar contenido sobre demanda, dividiendo la aplicacion
	* Se agrega un plugin syntaxt-dynamic-import en webpack para utilizar dynamic imports

## Storybook
	Tool para hacer comprobacion visual ui

## StoryTelling
Investigar

## Testing usando enzyme
### Piramide del Test
 * Unit test (jest, enzyme)
 * Test de Integracion (cypress)
 * Test de UI 

### Enzyme
 Shallow: Solo hace render tomando el primer nivel del elmento
 Full DOM rendering
 Static

### Cypress
Pruebas automatizadas


## Polyfills

## Server side rendering

## NextJS


# REDUX
Maquina de estados 
Contenedor de estados predecibles
Partes de Redux
* Store - Este es modificado por el reducer
* Dispatcher
* Reducers

Principios
Una sola fuente


1.- Programacion funcional
Programacion declarativa
Funciones puras : Params no se modifican, recibe una entrada proporciona una misma salida, Inmutabilidad nde datos.

* Curring, partial function application

Store: Objecto principal de almacenamiento de estados de la aplicacion, para acceder al estado se utiliza getState().
Uso de estore
createStore from redux
rootReducer from Reducers
createStore(rootReducer);


Actions: Representa la informacion que sera utilizada por el reducer para modificar el store.
Type: nombre de la accion
Payload: datos a enviar

Reducers:
Especifican como la app hara los compabios al estado y como se reflejan en el store

Dispatch Flow:



2.- Middlewares
    Actions y Reducers
	Arquitectura de Actions

3.- Async Operations
	Redux-thunk
	Redux-saga

4.- High Order Reducers
	Testing Redux
	Integracion de redux Frameworks/bibliotecas

5.- React Redux





Arquitectura de Actions
Los actions estan formados por 2 partes, la accion y el payload(informacion a enviar)

Types: constantes de actions
Actions: contiene las acciones y el payload

Investigar 
	* Function partial
	* Actions creators
	* Redux saga, thunk
	* High order reducers
	* Async and performance
	* Redux persist

Multiples Reducers
Combine Reducers

Redux Middleware
Patron change of usability



# Accesibilidad

 Enfoques
  * No inferir devices o mecanismos de la web para los usuarios
  * Mensajes sin ambiguedad para comunicar acciones
  * Sitios semanticos

## Progressive Engagment
Base

## Graceful degradation
Caracteristicas

## Espectros de discapacidad

## Rangos de visibilidad 
	* Visual Acuity

# Guidelines - Web Content Accesibility Guidelines (WCAG)
	POO

## WebIAM checklist

# Semantica y affordances
* Tecnologias asistivas

## Affordance
Es cualquier Objecto que ofrece la oportunidad de realizar alguna accion.

## Informacion Semantica

* Rol: El rol o tipo del elemento
* name: nombre del elemento
* value: valor tal cual
* state: habilitado o deshabilidato

## Accessibilty Tree
Es la modificacion del DOM tree util para tecnologia asistiva
Esto puede realizarce gracias a que el DOM implicitamente tiene semantica.

Automatizacion de Pruebas de usabilidad
AXE,WAVE


# ARIA - Accesibilidad
Proporciona una semantica a los elementos que no la tienen

Aria label: especifica el texto que será usado como label, sobreescribiendo otro label
Aria-labelledby
Aria hidden - Permite excluir contenido para que no sea tomando en cuenta.
Aria-live: Inidica a la tecnologia asistiva areas a las que se le debe prestar atencion

Roles Aria


# Progresive Web Apps

Reliable: Carga instantanea, offline
Fast: Response rapido, patron RAIL
Engaging: Expericiencia similar a una app

## Principios
Reliable
* Service workers
* App Shell Model

Fast
* Rail - 
* Performance best practice - 

Engaging
* Manifest - Archivo json con metadata
- short_name
- name
* Push Notifications

## App Shell
Recursos minimos que necesito para que la app funcione cosas que no van a cambiar.

## Web workers
API que permite funcionamiento complejo. Nos ofrece la posiibilidad de ejecutar Scripts en otro hilo separado.
Tipos de workers
* Dedicated workers
* Shared workers
* Service workers

### Service Worker
 * No se puede acceder al DOM
#### Lifecyle (Investigar)
 * Registro del sw
 * Install 
 /* global self */
 self.addEventListener('install', () => {
	 console.log('worker installed');
	 // Todo cachin de elementos
 });

* Activate
self.addEventListener('activate', () => {
	 console.log('worker activated');
	 // Todo eliminar el cache anterior
}); 


* Fetch
self.addEventListener('fetch', () => {
	 console.log('worker fetch');
	 // Todo implementacion de proxy
}); 



