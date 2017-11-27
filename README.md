[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Docs](https://img.shields.io/badge/Documento-Trabajo-blue.svg)](https://bigomby.github.io/trabajo-fast-reboot/)
[![Build Status](https://travis-ci.org/Bigomby/trabajo-fast-reboot.svg?branch=master)](https://travis-ci.org/Bigomby/trabajo-fast-reboot)

# FAST Reboot

:warning: **¡Ojo, este proyecto está en construcción, no le eches mucha cuenta aún!** :warning:

**¡El trabajo de FAST hecho como si estuviésemos en 2017!**

En este repositorio se realiza el trabajo de la asignatura FAST (Fundamentos de Aplicaciones y
Servicios Telemáticos) del Grado en ingeniería de las tecnologías de las telecomunicaciones
(Universidad de Sevilla) usando tecnologías usadas actualmente. El trabajo corresponde al curso
2016/2017.

## Índice

* [¿Qué tiene de malo JSP y jQuery?](#qué-tiene-de-malo-jsp-y-jquery)
  * [JSP](#jsp)
  * [jQuery](#jquery)
  * [BBDD SQL](#bbdd-sql)
* [¿Qué alternativas tenemos?](#qué-alternativas-tenemos)
  * [MongoDB](#mongodb)
  * [Node.js](#nodejs)
  * [express.js](#expressjs)
  * [Vue.js](#vuejs)
* [Stack MEVN](#stack-mevn)
* [Despliegue de la aplicación](#despliegue-de-la-aplicación)

## ¿Qué tiene de malo JSP, jQuery y las BBDD SQL?

### JSP

<p align="center">
<img src="http://i64.tinypic.com/2a6jzgh.png"></img>
<b>Tendencia de búquedas en Google de JSP</b>
</p>

JSP es una tecnología que se considera obsoleta desde hace años, en 2017 esta tecnología está
prácticamente muerta. Cuando JSP fue creado, la mayoría de las aplicaciones web se basaban en
renderizar una plantilla en el servidor, es decir, el servidor usaba una plantilla (normalmente era
una mezcla entre HTML y algún lenguaje propopio para plantillas) y se le enviaba el HTML ya generado
al cliente. Este funcionamiento tenía sentido en aquella época ya que los clientes (los navegadores
web) eran más simples y JavaScript no tenía la potencia que tiene hoy día, pero la situación ha
cambiado drásticamente.

Con la mejora de los motores de JavaScript en los navegadores, la introducción de nuevas tecnologías
como WebGL, WebRTC, etc. y la llegada de multitud de _frameworks_ de JavaScript para el _frontend_
(Angular, React, Vue.js, etc.) se pueden desarrollar aplicaciones muy ricas en funcionalidades. Esto
ha provocado un cambio de tendencia sobre dónde se ejecuta la mayor parte de la lógica.

Anteriormente en el navegador se ejecutaba lo mínimo posible (validación de formularios, AJAX,
animaciones, etc.). En la actualidad se prefiere ejecutar la mayor parte de la lógica en el cliente,
permitiendo desarrollar servidores mucho más simples para disminuir su consumo de recursos, lo que
permite servir a un número mayor de clientes.

### jQuery

jQuery fue un gran paso frente a usar JavaScript "a pelo". Es una gran ayuda a la hora de
interactuar con el DOM porque nos ofrece una serie de funcionalidades que nos simplifican la vida.
Sin embargo, la tendencia de hacer aplicaciones cada vez más complejas y con más funcionalidad ha
hecho que jQuery se quede obsoleto. jQuery es sólamente una librería para interactuar con el DOM de
forma sencilla, pero no es suficiente.

Mientras que una librería sólamente nos proporciona una herramienta, un _framework_ nos impone una
forma de trabajar. Usar un _framework_ conlleva aceptar una filosofía de desarrollo. Hoy en día es
habitual el uso de _frameworks_ para el desarrollo _frontend_ porque, entre otros motivos, al
imponer una forma de hacer las cosas, permite a un equipo gestionarse mejor ya que todos siguien el
mismo patrón de desarrollo.

### BBDD SQL

Las bases de datos relacionales como MySQL, MariaDB, PostgreSQL ofrecen muchas funcionalidades que
complican el sistema y hace que sea más difícil de escalar, sobre todo cuando hay muchas operaciones
de escritura. Sin embargo, si no necesitamos estas funcionalidaes podemos usar bases de datos NoSQL,
que carecen de ellas y, por lo tanto, tienen una escalabilidad mayor.

## ¿Qué alternativas tenemos?

Actualmente existen varios _frameworks_ que podríamos considerar "modernos". Algunos de los más
usados en el _backend_ son:

* Ruby on Rails, Sinatra (Ruby)
* Django (Python)
* Node.js + Express.js (JavaScript)
* Phoenix (Elixir)
* Beego, Revel, GinGonic, Iris (Go)
* Rocket (Rust)

En cuanto al _frontend_, todos los _frameworks_ están hecho es JavaScript o en un lenguaje que se
pueda transpilar a JavaScript (puesto que es el único lenguaje que funciona en el navegador,
[por ahora](http://webassembly.org/)). Veamos algunos:

* Angular
* React
* Ember
* Backbone
* Vue
* Elm

### MongoDB

Entre las bases de datos NoSQL encontramos MongoDB que es muy utilizada por su simplicidad y
facilidad de uso. No requiere definir tablas ya que su modelo para almacenar datos es muy flexible
(_schemaless_). Crear un _cluster_ con varias instancias de MongoDB es relativamente fácil ya que ha
sido diseñada para ello.

### Node.js

<p align="center">
<img src="http://i64.tinypic.com/o799p4.png"></img>
<b>Tendencia de búquedas en Google de Node.js</b>
</p>

**Node.js** es una plataforma que nos permite desarrollar aplicaciones **interpretando** código
JavaScript directamente en nuestro sistema operativo, al igual que el intérprete de Python
interpreta el código de Python o la JVM (_Java Virtual Machine_) interpreta el byte-code de Java.

Tanto **Node.js** como Chrome usan el motor de JavaScript **V8**. Podemos pensar que **Node.js** es
como si sacáramos la parte de Chrome que ejecuta JavaSript para ejecutarlo fuera del navegador.

### express.js

**Node.js** nos da una plataforma sobre la que ejecutar código JavaScript, sin embargo, es
recomendable utilizar un _framework_ que nos ayude a la hora de desarrollar una aplicación web. Uno
de los _frameworks_ más usados para desarrollar aplicaciones web con **Node.js** es **express.js**.

**express.js** nos proporciona una capa de abstracción sobre el uso de las librerías HTTP, de forma
que podamos configurar autenticación, enrutado, parseo de peticiones, etc.

### Vue.js

<p align="center">
<img src="http://i63.tinypic.com/20ivq75.png"></img>
<b>Tendencia de búquedas en Google de Vue.js</b>
</p>

Por último, tenemos a **Vue.js** como tecnología para nuestro _frontend_. **Vue.js** puede usarse
como una librería o como un _framework_. Para usar **Vue.js** bastaría con importar la librería y
usarla directamente dentro de nuestro proyecto. Sin embargo, **Vue.js** nos proporciona
opcionalmente una forma de estructurar nuestro proyecto junto con una serie de extensiones para
añadir funcionalidades. También existen _frameworks_ más completo que funcionan sobre **Vue.js** que
no veremos aquí (Quasar, Vuetify, Nuxt.js y otros).

La filosofía de **Vue.js** se basea en estructurar nuestra aplicación en pequeños componentes. Cada
componente tendrá asociada una vista hecha en HTML, un estilo en CSS y una lógica en JavaScript.
Usando **Vue.js** compondremos nuestra aplicación a base de pequeños componentes.

## Stack MEVN

Para realizar el trabajo de la asignatura usaremos las tecnologías anteriores conocidas como el
**Stack MEVN (MongoDB, Express, Vue y Node)**. Las ventajas de este stack son las siguientes:

* **Desacople entre cliente y servidor**
  * El servidor no sabe nada sobre la parte visual de la aplicación. Sólamente será responsable de
    proporcionar los datos al cliente.
  * Evitamos las plantillas complejas como en PHP o JSP que mezclan diferentes lenguajes y terminan
    siendo confusas.
  * Separación de código de cliente y servidor. Facilita el desarrollo de la aplicación puesto que
    el código de _backend_ y de _frontend_ forman dos repositorios diferentes.
* **Un sólo lenguaje**: Sólamente necesitamos JavaScript para toda la aplicación. No más
  combinaciones de Java + JS, PHP + JS, Python + JS, etc.
* **Sin SQL**: Como usaremos MongoDB como base de datos no relacional no necesitamos conocer SQL
  para realizar consultas ni definir tablas.
* **Consumo de recursos**: Tendremos un servidor que consumirá muchos menos recursos puesto que no
  tendrá que renderizar las plantillas, la renderización la realiza el cliente en su navegador.
* **Rendimiento**: La máquina **V8** en la que se basa **Node.js** ofrece muy buen rendimiento sin
  tener que hacer uso de hilos para la concurrencia, lo cual nos ahorra muchos posibles _bugs_
  típicos de la programación con hilos, como las condiciones de carrera.

## Despliegue de la aplicación

Otra cosa que se echa de menos en la asignatura es saber cómo desplegar la aplicación una vez la
hemos desarrollado.

La producción de una aplicación no termina tras el desarrollo, por lo que también veremos cómo
podemos desplegarla para que sea accesible para todo el mundo. Para ello usaremos **Heroku**, un
servicio que nos permite desplegar aplicaciónes hechas con **Node.js** de forma gratuita.
