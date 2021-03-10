# TRABAJO DEL TEMA 6

Crear en GitHub 2 repositorios, uno para el backend y otro para el frontend de la aplicación desarrollada a lo largo del curso.

En la siguiente captura muestro los dos repositorios creados de backend y frontend de nuestra aplicación.


![Captura de pantalla (478)](https://user-images.githubusercontent.com/55695233/110682749-960a2400-81db-11eb-8209-3327e20f7a2b.png)


Mostramos una captura de nuestro backend.


![Captura de pantalla (480)](https://user-images.githubusercontent.com/55695233/110682858-b639e300-81db-11eb-8dab-b47c03efb7d7.png)


Una captura de nuestro frontend.


![Captura de pantalla (481)](https://user-images.githubusercontent.com/55695233/110683049-ea150880-81db-11eb-8c6c-3d7a7a095d55.png)


Configurar una clave SSH para acceso desde casa. 
Si se considera necesario puede configurarse otra clave para el acceso desde el centro educativo.

Generamos la clave con ssh-keygen

![Captura de pantalla (482)](https://user-images.githubusercontent.com/55695233/110683145-031db980-81dc-11eb-9214-3be67d784a83.png)


Copiamos la clave pública a un bloc de notas en el escritorio


![Captura de pantalla (483)](https://user-images.githubusercontent.com/55695233/110683211-12046c00-81dc-11eb-87dd-0ca22a181221.png)

Añadimos la clave SSH pública en github
![Captura de pantalla (484)](https://user-images.githubusercontent.com/55695233/110683312-23e60f00-81dc-11eb-830b-c8983584eb8d.png)


El uso de los comandos más frecuentes de git:

git clone:  Clonando un repositorio existente
Si deseas obtener una copia de un repositorio Git existente — por ejemplo, un proyecto en el que te gustaría contribuir — el comando que necesitas es git clone. Cada versión de cada archivo de la historia del proyecto es descargada por defecto cuando ejecutas git clone.

Clonamos el repositorio de backend a nuestra carpeta backend.

![Captura de pantalla (485)](https://user-images.githubusercontent.com/55695233/110683344-2ea0a400-81dc-11eb-8ca7-f0e24caf93cb.png)


Realizamos un ls dentro de la carpeta backend creada para comprobar que se ha clonado con éxito.

![Captura de pantalla (486)](https://user-images.githubusercontent.com/55695233/110683374-38c2a280-81dc-11eb-9598-60f63abf8796.png)

git add:

Añadir archivos al área de ensayo, git add
Esto permite construir series de instantáneas de los archivos creados o modificados en el proyecto antes de guardarlos en el historial del proyecto. Cuando finalmente se quiere guardar y agrupar estos cambios, se guardan en el historial mediante commits.

git commit:

El comando git commit captura una instantánea de los cambios preparados en ese momento del proyecto. Las instantáneas confirmadas pueden considerarse como versiones "seguras" de un proyecto: Git no las cambiará nunca a no ser que se lo pidas expresamente.


Creamos un archivo de markdown READMEPLEASE.md
Realizamos un git add y seguidamente un commit.

![Captura de pantalla (487)](https://user-images.githubusercontent.com/55695233/110683403-4546fb00-81dc-11eb-840d-75e79f9db956.png)

git log:

El comando git log es una herramienta básica de Git para explorar el historial del repositorio. Este comando se usa cuando necesitas buscar una versión concreta de un proyecto o saber los cambios que se introducirán mediante la fusión en una rama de función.

![Captura de pantalla (488)](https://user-images.githubusercontent.com/55695233/110683429-4ed06300-81dc-11eb-993e-3adb47dc6a6a.png)

git status:

El comando git status muestra el estado del directorio de trabajo y del área del entorno de ensayo. Permite ver los cambios que se han preparado, los que no y los archivos en los que Git no va a realizar el seguimiento.

![Captura de pantalla (489)](https://user-images.githubusercontent.com/55695233/110683457-56900780-81dc-11eb-8b05-c275d0118ea0.png)

git remote

El comando git remote es una parte de un sistema más amplio que se encarga de sincronizar los cambios. Los registros inscritos mediante el comando git remote se utilizan junto con los comandos git fetch, git push y git pull.
Vamos a mostrar también con git remote -v.

![Captura de pantalla (490)](https://user-images.githubusercontent.com/55695233/110683502-63146000-81dc-11eb-80a7-9382e922a4c7.png)


El uso de comandos más avanzados de git:

git diff:

Es un comando multiusos de Git que, cuando se ejecuta, lleva a cabo una función para establecer las diferencias en los orígenes de datos de Git. Dichos orígenes de datos pueden ser confirmaciones, ramas y archivos, entre otras posibilidades.
![Captura de pantalla (491)](https://user-images.githubusercontent.com/55695233/110683550-6f002200-81dc-11eb-9d3d-4c8ce8dc49b6.png)

git reset:

Como resumen, git reset es un comando potente que se utiliza para deshacer los cambios locales en el estado de un repositorio de Git. Git reset actúa en "los tres árboles de Git". Estos árboles son el historial de confirmaciones ( HEAD ), el índice del entorno de ensayo y el directorio de trabajo.

![Captura de pantalla (492)](https://user-images.githubusercontent.com/55695233/110683573-758e9980-81dc-11eb-8ae9-cfb3027250fe.png)








# FRONTEND (con Svelte)

> **ESTE MINITUTORIAL ES UNA VERSIÓN RESUMIDA DEL FRONTEND DE ESTA APLICACIÓN**
> 
> A tener en cuenta:
>
> - Mucho del código que aparece en este minitutorial está simplificado con fines didácticos.
> - Para ver todo el código, revisar el código fuente de este repositorio.
> - **La parte backend de esta aplicación puede verse en [tiendabackend](https://github.com/jamj2000/tiendabackend)**


## Introducción

Actualmente (año 2020), en el mundo del desarrollo web se vive una efervescencia de nuevas tecnologías. 

Como base tenemos a los 3 pilares fundamentales:

- **HTML 5**
- **CSS 3**
- **Javascript (EcmaScript 6)**

Son lenguajes que todo desarrollador web debería conocer con cierta soltura.

Tanto HTML 5 como CSS 3 han crecido mucho y actualmente cada uno de estos estándares se organizada en distintas partes. 

En cuanto a Javascript, es a partir de 2015 (estándar ECMAScript 6), que  llegó con un montón de nuevas características después de muchos años de indefinición, cuando ha resurgido un gran interés por este lenguaje, ya no sólo para desarrollo de scripts web, sino también como lenguaje a tener en cuenta para el desarrollo de aplicaciones. Esta tendencia se ha visto reforzada por dos circunstancias:

- El uso de Javascript fuera del navegador, a través del entorno de ejecución **node.js**.
- La innumerable cantidad de **bibliotecas/frameworks** que han ido surgiendo.

Javascript sigue evolucionando y dicho estándar se va actualizando cada año. Este año 2020 saldrá el ECMAScript 11, actualmente llamado ES.Next. Sin embargo, estas nuevas versiones sólo añaden características menores. El cuerpo principal de Javascript está en la versión indicada más arriba, también conocida como ES6.

## ¿Qué es **svelte**?

> Eramos pocos, y parió la abuela.

Existen muchas bibliotecas y frameworks para desarrollo en Javascript, tanto para su uso en el **backend** con node.js, como en el **frontend**.

En cuanto al **frontend**, tenemos a **Angular**, **React** y **Vue** como las bibliotecas/frameworks más usadas/os. 

El desarrollo de frontend está muy publicitado y la necesidad de dicho tipo de desarrolladores es manifiesta. Independientemente de framework usado, parece haber una convergencia y acuerdo entre ellos: **todos realizadan desarrollo por componentes web**.

Un **componente web** es una **parte de una aplicación web que encapsula código HTML, CSS y JavaScript**, de forma que no puede ser afectado por el código de la página que lo incluye, salvo que usemos los mecanismos establecidos a tal efecto. Por tanto permiten la reutilización y encapsulación de código cliente.

Svelte es un **compilador** (también puede calificarse como framework), que toma muchas ideas prestadas de los frameworks anteriores, sobre todo de React. Sin embargo hay una característica que lo diferencia de los anteriores: 

- Svelte **realiza una compilación** de nuestro código, convirtiendo sus componentes en código imperativo altamente eficiente.

Proporcionando las siguientes ventajas:

- Tenemos que escribir mucho menos código frente a otros frameworks.
- El código final se ejecuta de forma muy eficiente y rápida.
- El peso (cantidad de KB) de la aplicación final es muy pequeño.
- Facilita la programación reactiva.

Un ventaja añadida es que su sintaxis es más simple, lo cual hace que su curva de aprendizaje sea menos pronunciada que la de otros frameworks. Por este motivo es un buen candidato para su uso con fines didácticos.


## Inicio de un proyecto de svelte

Para iniciar un proyecto de svelte, ejecutamos:

```console
npx  degit  sveltejs/template   nombre-proyecto
```

> Nota: Sustituimos *nombre-proyecto* por el nombre concreto que queramos dar.

Este comando descarga los archivos iniciales de un repositorio de github, en concreto desde [`https://github.com/sveltejs/template`](https://github.com/sveltejs/template). **Son sólo unos pocos KB**.

> Nota: Como comparación frente a otros frameworks ...
>
> - **Vue**
>   - ```npx  @vue/cli  create  nombre-proyecto   # Unos 100MB aprox.```
> - **React**
>   - ```npx  create-react-app  nombre-proyecto   # Unos 200MB aprox.```
> - **Angular**
>   - ```npx  @angular/cli new  nombre-proyecto   # Unos 300MB aprox.```


## Examinar el proyecto creado

Entramos en el directorio del proyecto, ejecutando:

```console
cd   nombre-proyecto  &&  ls 
```

> Nota: Sustituimos *nombre-proyecto* por el nombre concreto.

Para ver todo el contenido podemos ejecutar el comando `tree`:

```
├── package.json
├── public
│   ├── favicon.png
│   ├── global.css
│   └── index.html
├── README.md
├── rollup.config.js
└── src
    ├── App.svelte
    └── main.js
```

El archivo `package.json` es el archivo de gestión de proyecto y dependencias. En él. podremos editar el nombre del autor, la versión, el tipo de licencia, etc.

La carpeta `public` contiene el frontend en forma de contenido estático, el cual deberemos subir a nuestro servidor de producción una vez finalizado el proyecto.

El archivo `README.md` puede eliminarse o podemos editarlo a nuestro gusto. No es necesario para el funcionamiento de la aplicación, aunque pudiera ser interesante para fines de documentación.

El archivo `rollup.config.js` contiene la configuración del empaquetador, que en este caso es **Rollup**. Otros frameworks utilizan otros empaquetadores como Webpack o Parcel. No debemos borrar este archivo. Tampoco lo editaremos, por ahora.

Finalmente, la carpeta `src` va a contener **nuestro código y todos los componentes web que vayamos creando**. Cada vez que realicemos un cambio en los archivos de dicha carpeta, rollup volverá a compilar y pondrá el resultado en `public/build/bundle.css` y `public/build/bundle.js`. 

El archivo `public/index.html` tiene enlaces a los anteriores. Su código es:

```html
<!DOCTYPE html>
<html lang="en">
<head>
        <meta charset='utf-8'>
        <meta name='viewport' content='width=device-width,initial-scale=1'>

        <title>Svelte app</title>

        <link rel='icon' type='image/png' href='/favicon.png'>
        <link rel='stylesheet' href='/global.css'>  
        <link rel='stylesheet' href='/build/bundle.css'> <!-- -->

        <script defer src='/build/bundle.js'></script> <!-- -->
</head>

<body>
</body>
</html>
```

## Empezar a trabajar en el proyecto

Abriremos nuestro editor favorito y comenzaremos a editar los archivos que están en la carpeta `src`.

El contenido de los archivos `src/main.js` y `src/App.svelte` es el que se muestra a continuación:

**`src/main.js`**

```javascript
import App from './App.svelte';

const app = new App({
        target: document.body,
        props: {
                name: 'world'
        }
});

export default app;
```

La propiedad `name` tiene el valor `world`, y dicho valor es pasado al componente `src/App.svelte` a la variable del mismo nombre que tiene la palabra `export`. 

Dentro de la sección de `html y componentes web` (en este caso `<main></main>`) podemos usar dicho valor. Por eso tenemos la línea `<h1>Hello {name}!</h1>`. 
En dicha sección, las variables deben aparecer entre llaves {}.

**`src/App.svelte`**

```html
<script>
        export let name;
</script>

<main>
        <h1>Hello {name}!</h1>
        <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>

<style>
        main {
                text-align: center;
                padding: 1em;
                max-width: 240px;
                margin: 0 auto;
        }

        h1 {
                color: #ff3e00;
                text-transform: uppercase;
                font-size: 4em;
                font-weight: 100;
        }

        @media (min-width: 640px) {
                main {
                        max-width: none;
                }
        }
</style>
```

Para ejecutar la aplicación deberemos ejecutar:

```console
npm  run  dev
```

La ejecución del script anterior dará error. El motivo es que no hemos instalado las dependencias que aparecen indicadas en el archivo `package.json`.

Para instalar dichas dependencias, ejecutamos:

```
npm  install
```

Dicho comando, leerá el archivo `package.json`, e instalará todas las dependencias que aparecen ahí. Ahora ya podemos volver a ejecutar `npm  run  dev`.

Podrás ver la aplicación en [localhost:5000](http://localhost:5000).


## Simplificando antes de comenzar

El archivo `src/main.js` podemos simplicarlo eliminando algunas líneas. Quedaría así:

```javascript
import App from './App.svelte';

const app = new App({ target: document.body });

export default app;
```

Este archivo es el punto de entrada a la aplicación. Se genera un objeto `app` que se instancia a partir del componente `App.svelte`.  La propiedad `name` que hemos eliminado es la forma de pasar información desde *arriba* (`main.js`) hacia *abajo* (`App.svelte`).

El componente `App.svelte` será el componente principal de la aplicación. Todo componente en svelte se nombra con la primera letra en mayúscula y la extensión .svelte.

Cada componente dispone de 3 secciones:

```html
<script>
  // Código javascript
</script>

<style>
  /* Código CSS */
</style>

<!-- Nuestros elementos HTML y componentes web -->
```

El orden es indiferente, aunque se recomienda organizar siguiendo el orden anterior.

En la sección de `script` escribiremos en Javascript la funcionalidad del componente.

En la sección de `style` escribiremos en CSS la presentación del componente.

Y en la sección de `html y componentes web` escribiremos la estructura del componente. Para ello haremos uso de código html y ciertas extensiones de svelte que iremos viendo más adelante.

Como este componente no va a recibir desde *arriba* la propiedad `name`, podemos eliminar la línea `export let name` que aparece en la sección de `script`.

> **NOTA:** En svelte, cuando una variable tiene antepuesta la palabra `export` significa que a dicha variable puede pasársele un valor desde el componente que está encima en la jerarquía.


Vamos a eliminar también el código CSS y reorganizar las secciones. Quedaría así:


```html
<script>

</script>

<style>

</style>

<!-- Nuestros elementos HTML y componentes web -->
```

Sencillo, no?.  Ya podemos empezar.

## Desarrollando nuestro primer componente

Vamos a modificar el componente `App.svelte`, el cual habiamos vaciado anteriormente.

![App](app.png)

El contenido que tendrá sera el siguiente:

```html
<script>
  import { Router } from "svelte-routing";
  import Nav        from "./Nav.svelte";
  import Contenido  from "./Contenido.svelte";
</script>

<style>
  @import url("https://fonts.googleapis.com/css?family=Aclonica");

  :global(*) {
    margin: 0;
    padding: 0;
  }

  :global(body) {
    display: flex;
    flex-direction: column;
    font-family: "Aclonica";
  }
 
  :global(a:hover) {
    text-decoration: none;
    cursor: pointer;
  }
</style>

<Router>
  <Nav />
  <Contenido />
</Router>
```

En la sección de `script` importamos los paquetes y componentes que vayamos a usar. En este caso importamos el componente `Router` que está en el paquete `svelte-routing`. Este paquete nos proporciona los componentes necesarios para crear enrutatodores (`Router`), enlaces (`Link`) y rutas (`Route`). Necesitaremos tener instalado dicho paquete, por lo que debemos ejecutar en el terminal:

```console
npm  install  svelte-routing
```

Vamos a importar también los componentes `Nav` y `Contenido`, que van a estar en la misma carpeta que `App`, y que vamos a crear el el siguiente apartado. Ahora mismo, para que no de error el compilador, podemos crear los 2 componentes vacíos o con algún mensaje en su interior.

**En svelte los estilos CSS solamente se aplican al componente donde están definidos y a ningún otro componente, aunque tengan las mismas etiquetas**. Si queremos que una determinada etiqueta html tenga un estilo en todos los componentes usamos la forma `:global(etiqueta) { ... }` en lugar de `etiqueta {}` 


La estructura del componente `App` está formada por un `Router`, dentro del cual se definen dos componentes: `Nav`, que tendrá los enlaces (`Link`) necesarios para la navegación, y `Contenido`, que tendrá las rutas (`Routes`) a los componentes necesarios.


## Componentes de navegación y contenido

Crearemos dos componentes llamados `Nav.svelte` y `Contenido.svelte`. Debe estar en la misma carpeta que el componente `App.svelte`.

**`Nav.svelte`**

```html
<script>
  import { Link } from "svelte-routing";

  // Aquí el código javascript para añadir funcionalidad a la barra de navegación.
  // Consultar el código fuente.

</script>

<style>
  /* Aquí el código CSS para diseño responsive de la barra de navegación. */
  /* Consultar el código fuente */
</style>

<nav> 
  <!-- Se eliminan etiquetas html para resaltar lo esencial -->
  <!-- Consulta el código fuente. -->       
  <Link to="/">Inicio</Link>
  <Link to="/armas">Artículos</Link>
  <Link to="/soldados">Soldados</Link>
</nav>
```

El componente `Nav` será la barra de navegación (`nav`), con los enlaces a las rutas del lado cliente. Para los enlaces hacemos uso del componente `Link` del paquete `svelte-routing`.

**`Contenido.svelte`**

```html
<script>
  import { Route } from "svelte-routing";
  import Inicio from "./Inicio.svelte";
  import Arma from "./Armas.svelte";
  import Soldado from "./Soldados.svelte";
</script>

<style>
  /* Aquí el código CSS */
  /* Consultar el código fuente */
</style>

<main>
  <!-- Se eliminan etiquetas html para resaltar lo esencial -->
  <!-- Consulta el código fuente. --> 
  <Route path="/" component={Inicio} />
  <Route path="/armas" component={Armas} />
  <Route path="/soldados" component={Soldados} />
</main>
```

El componente `Contenido` será la sección principal (`main`), con las rutas y el componente asociado a cada una de ellas. Para las rutas hacemos uso del componente `Route` del paquete `svelte-routing`.

## Componentes para el contenido

Dentro del componente anterior `Contenido` podrán renderizarse distintos componentes, dependiendo del `Link` que pulsemos en la barra de navegación. Los componentes que podrán aparecer en `Contenido` son:

- **Inicio**
- **Artículos**
- **Soldados**

**`Inicio.svelte`**

```html
<style>
  /* Aquí el código CSS */
  /* Consultar el código fuente */
</style>

<h1>Tienda PWA</h1>
  <!-- Se eliminan etiquetas html para resaltar lo esencial -->
  <!-- Consulta el código fuente. --> 
```

Este componente mostrará información acerca de la aplicación. Sólo posee código HTML y CSS. No necesita solicitar datos al servidor. Por tanto su carga es inmediata, y por este motivo lo mostraremos nada más iniciarse la aplicación. Ello permite una carga inicial de la aplicación instantánea.


**`Armas.svelte`**

![Armas](armas.png)

 ```html
 <script>
  import { onMount, getContext } from "svelte";
  import { jsonData }            from "./store.js";

  import Buscar                  from "./Buscar.svelte";
  import Arma                from "./Arma.svelte";
  import Boton                   from "./Boton.svelte";

  const URL = getContext("URL");

  let busqueda = "";
  let arma = {};

  onMount(async () => {
    const response = await fetch(URL.armas);
    const data = await response.json();
    $jsonData = data;
  });

  $: regex = new RegExp(busqueda, "i");
  $: datos = busqueda 
    ? $jsonData.filter(item => regex.test(item.nombre))
    : $jsonData;

</script>

<style>
  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: left;
    flex-wrap: wrap;
  }
</style>

<h1>ARTÍCULOS</h1>
<Buscar bind:busqueda />

<div class="container">
  <Arma bind:arma>
    <div style="text-align: right">
      <Boton documento={arma} tipo="insertar" coleccion="arma" />
    </div>
  </Arma>
</div>

<div class="container">
  {#each datos as arma}
    <Arma {arma}>
      <div style="text-align: right">
        <Boton documento={arma} tipo="modificar" coleccion="armas" />
        <Boton documento={arma} tipo="eliminar"  coleccion="armas" />
      </div>
    </Arma>
  {/each}
</div>
```



**`Soldados.svelte`**

![Soldados](soldados.png)

```html
<script>
  import { onMount, getContext } from "svelte";
  import { jsonData }            from "./store.js";

  import Buscar                  from "./Buscar.svelte";
  import Soldado                 from "./Soldado.svelte";
  import Boton                   from "./Boton.svelte";

  const URL = getContext("URL");

  let busqueda = "";
  let soldado = {};

  onMount(async () => {
    const response = await fetch(URL.soldados);
    const data = await response.json();
    $jsonData = data;
  });

  $: regex = new RegExp(busqueda, "i");
  $: datos = busqueda 
    ? $jsonData.filter(item => regex.test(item.nombre))
    : $jsonData;

</script>

<style>
  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: left;
    flex-wrap: wrap;
  }
</style>

<h1>CLIENTES</h1>
<Buscar bind:busqueda />

<div class="container">
  <Soldado bind:soldado>
    <div style="text-align: right">
      <Boton documento={soldado} tipo="insertar" coleccion="soldados" />
    </div>
  </Soldado>
</div>

<div class="container">
  {#each datos as soldado}
    <Soldado {soldado}>
      <div style="text-align: right">
        <Boton documento={soldado} tipo="modificar" coleccion="soldados" />
        <Boton documento={soldado} tipo="eliminar" coleccion="soldados" />
      </div>
    </Soldado>
  {/each}
</div>
```



## Otros componentes

**`Arma.svelte`**

```html
<script>
  export let arma = {};
</script>

<style>
   /* Aquí el código CSS */
  /* Consultar el código fuente */
</style>

<div class="card">
  <input bind:value={arma.nombre} class="title" />
  <input
    type="number"
    min="0"
    max="9999.99"
    step=".01"
    bind:value={arma.precio} />  €
  <slot />
</div>
```



**`Soldado.svelte`**

```html
<script>
  export let soldado = {};
</script>

<style>
  /* Aquí el código CSS */
  /* Consultar el código fuente */
</style>

<div class="card">
  <input bind:value={soldado.nombre} class="title" />
  <input bind:value={soldado.apellidos} class="title" />
  <slot />
</div>
```




**`Boton.svelte`**


```html
<script>
  import { onMount, getContext } from "svelte";
  import { jsonData }            from "./store.js";

  export let tipo = "insertar";        // insertar, modificar, eliminar
  export let coleccion = "armas";  // armas, soldados
  export let documento = {};
  
 
  let handler = () => {};  
  let clases = "";
  let url = "";

  const URL = getContext("URL"); 

  onMount(() => {
    switch (tipo) {
      case "insertar":
        handler = insertar;
        clases = "btn btn-insertar";
        break;
      case "modificar":
        handler = modificar;
        clases = "btn btn-modificar";
        break;
      case "eliminar":
        handler = eliminar;
        clases = "btn btn-eliminar";
        break;
      default:
    }

    switch (coleccion) {
      case "armas": url=URL.armas; break;
      case "soldados": url=URL.soldados; break;
      default:
    }
  });

  function insertar() {
    // Aquí código Javascript
    // Consultar el código fuente
  }

  function modificar() {
    // Aquí código Javascript
    // Consultar el código fuente
  }

  function eliminar() {
    // Aquí código Javascript
    // Consultar el código fuente
  }

  // Aquí código Javascript
  // Consultar el código fuente
</script>

<style>
  /* Aquí el código CSS */
  /* Consultar el código fuente */
</style>

<button class={clases} on:click={handler} />
```

**`Buscar.svelte`**

```html
<script>
  export let busqueda;
</script>

<label>
  Buscar
  <input bind:value={busqueda} type="search" />
</label>
```


### Similitud entre *elementos html* y *componentes web*

![similitud](similitud.png)



## Comunicación entre componentes

Existen 3 mecanismos:

- Propiedades
- Contextos
- Almacenes



### Propiedades (props)

- Permiten comunicación ***padre-hijo*** únicamente.
- Permiten comunicación ***arriba-abajo*** y ***abajo-arriba***.
- Permiten comunicación ***lectura-escritura***.

#### Ejemplo

**`Armas.svelte`**
```html
<script>
    let texto = "camisa";
</script>

<Buscar busqueda={texto} />
```

**`Buscar.svelte`**

```html
<script>
  export let busqueda;
</script>

<label>
  Buscar
  <input bind:value={busqueda} type="search" />
</label>
```

Desde el componente padre `Armas` pasamos el valor `camisa` a la propiedad `busqueda` del componente `Buscar`.

Por defecto, el sentido de la comunicación es Padre->Hijo. 

Si deseamos que el hijo (`Buscar`) pueda pasar información al padre (`Armas`) haremos uso de la directiva **`bind`** en el componente padre, que quedaría así:

```html
<script>
    let texto = "camisa";
</script>

<Buscar bind:busqueda={texto} />
```

El valor de la propiedad `busqueda`, que será modificada desde el componente `Buscar`, "subirá" hasta la variable `texto` del componente `Articulos`.



### Contextos (setContext / getContext)

- Permiten comunicación ***padre-cualquier_descendiente***.
- Permiten comunicación ***arriba-abajo*** únicamente.
- Permiten comunicación ***lectura*** únicamente.


#### Ejemplo

**`App.svelte`**

```html
<script>
  import { setContext } from "svelte";
	
  const urlArmas = "https://tiendabackend.herokuapp.com/api/armas/";

  setContext("urlArmas", urlArmas);
</script>	
```

**`Boton.svelte`**

```html
<script>
  import { getContext } from "svelte";
	
  const urlArmas = getContext("urlArmas");
	
  function obtener() {
      fetch(urlArmas, { method: "GET" })
      .then(res => res.json())
      .then(data => {  /* código para éxito */ })
      .catch(err => {  /* código para error */ });
  }
</script>
```

### Almacenes (stores)

- Permiten comunicación ***componente-componente*** independientemente de su jerarquía.
- Permiten comunicación ***arriba-abajo*** y ***abajo-arriba***.
- Permiten comunicación ***lectura-escritura***.


#### Ejemplo

**`store.js`**

 ```javascript
import { writable } from 'svelte/store';

export const jsonData = writable([]);
```

Declaramos en `store.js` un array vacío, que contendrá datos en formato JSON.


**`Armas.svelte`**

```html
<script>
 import { jsonData }   from "./store.js";
	
 onMount(async () => {
    const response = await fetch( urlArmas );
    const data = await response.json();
    $jsonData = data;
  });
</script>	
```

En el componente `Armas.svelte` hacemos una petición **fetch** al servidor y guardamos los datos en formato JSON en la variable jsonData del almacén. 

**Nota:** Observa que para referirnos a la variable del almacén lo hacemos como **$jsonData**.


**Boton.svelte**

```html
<script>
  import { jsonData }   from "./store.js";
  export let documento = {};
	
  function insertar() {
      fetch(urlArmas, {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(documento)
      })
        .then(res => res.json())
        .then(data => { 
	  $jsonData = [...$jsonData, data];
          ok();
        })
        .catch(err => ko());
  }
	
</script>
```

En el componente `Boton.svelte` insertamos un nuevo artículo en el servidor mediante una petición **fetch** de tipo POST. Si se guarda correctamente en el servidor, entonces actualizamos en consecuencia nuestra variable jsonData del almacén:

**`$jsonData = [...$jsonData, data]`**

**Nota:** Observa de nuevo que para referirnos a la variable del almacén lo hacemos como **$jsonData**.



## Construir la aplicación para el entorno de producción

Para crear una versión optimizada de la aplicación, ejecutamos:

```bash
npm run build
```

Puedes ejecutar la aplicación recién creada con `npm run start`. Esto utiliza [sirv](https://github.com/lukeed/sirv), que se incluye en las `dependencias` de `package.json` para que la aplicación funcione cuando se implemente en plataformas como [Heroku](https://heroku.com).


## Single-Page App

**Esta es una aplicación de página única (SPA)**.

Por defecto, sirv solo responderá a las solicitudes que coincidan con los archivos en `public`. Esto es para maximizar la compatibilidad con los servidores de archivos estáticos, lo que le permite implementar su aplicación en cualquier lugar.

Si estás creando una aplicación de una sola página (SPA) con varias rutas, sirv debe poder responder a las solicitudes de *cualquier* ruta. Puedes hacerlo editando el comando `"start"` en package.json:


```js
"start": "sirv public --single"
```

> NOTA: sirv es el módulo de node que permite ejecutar un servidor web y mostrar nuestra app.


## Despliegue en la web

Este frontend no contiene código de servidor, es decir, no contiene código para backend. Por tanto podemos desplegarlo como hariamos con cualquier página html. Cualquier sitio que permita **contenido estático** nos vale. 

Existen muchos sitios que ofrecen esta opción, Por ejemplo:

- GitHub Pages
- Netlify
- Vercel
- Surge

Para desarrolladores con poca experiencia, la forma más sencilla de despliegue es utilizar la interfaz web que proporcionan dichos sitios. 

Pero si deseas realizar el despliegue mediante interfaz de texto, a continuación se muestra un resumen de cómo se realizaría con Vercel y con Surge.


**Con [vercel](https://vercel.com)**

Instala `vercel` si aún no lo has hecho:

```bash
npm install -g vercel
```

Luego, desde la carpeta de tu proyecto:

```bash
vercel login
vercel --prod
```


**Con [surge](https://surge.sh/)**

Instala `surge` si aún no lo has hecho:

```bash
npm install -g surge
```

Luego, desde la carpeta de tu proyecto:

```bash
npm  run  build
surge  public  my-project.surge.sh
```

> NOTA: Sustituye *my-project* por el nombre de tu proyecto.


## Progressive Web Application

**Esta es una aplicación web progresiva (PWA)**.

La tecnología PWA es relativamente nueva, iniciandose en el año 2015 bajo el auspicio de **Google**.

Dicha tecnología pretende, mediante la aplicación de pequeñas adaptaciones, usar las **tecnologías web (HTML + CSS + Javascript)** para el **desarrollo de aplicaciones de escritorio y móviles**.

Como el lector entendido en el asunto comprenderá rápidamente, las implicaciones de tal tecnología son enormes:

- **Desarrollo para web, para escritorio y para móvil. Todo en uno.**
- **Simplificación del desarrollo**. 
  - "No es necesario" aprender lenguajes como Java o Swift.
  - "No es necesario" desarrollar de forma nativa (SDKs para Android e iOS).
  - "No es necesario" desarrollar de forma híbrida (Frameworks Cordova, React Native, Angular Ionic. Electron para el escritorio)
- **Uso de Web APIs**, las cuales [son bastantes, muchas de ellas aún en desarrollo](https://developer.mozilla.org/en-US/docs/Web/API): fetch, websockets, geolocalización, audio, speech, ... 
 

**Requisitos para considerar progresiva a una aplicación web**

Una PWA debe cumplir, en esencia, 2 requisitos:

- Debe servirse desde un servidor **HTTPS**. Excepción: `localhost`.
- Debe disponer de un archivo **manifest.json** o similar con metadata de la applicación.
- Debe tener capacidad de funcionar **offline**. Para ello es necesario disponer de un *Service Worker*.


Los archivos necesarios para hacer que una aplicación web sea progresiva son:

- `public/manifest.json` 
- `public/images/icons/*`  
- `public/service-worker.js`   

Tanto el archivo `manifest.json` como la carpeta `images` y todos sus iconos, podemos generarlos de manera sencilla con [Web App Manifest Generator](https://app-manifest.firebaseapp.com/).

El archivo `service-worker.js` se encarga de funcionar como intermediario entre nuestro frontend y el backend, y tiene la siguiente apariencia:

```javascript
//------  Este código está simplificado para resaltar la estructura
//------  Para ver todo el código consulta el archivo correspondiente
const CACHE_NAME = 'tiendafrontend-v1';

// Archivos necesarios para el funcionamiento offline
const CACHE_ASSETS = [
  '/',
  '/index.html',
  '/offline.html',
  '/favicon.png'
];

// INSTALL
// Realizamos el cacheo de la APP SHELL
self.addEventListener('install', funcionDeInstalacion);


// ACTIVATE
// Eliminamos cachés antiguas.
self.addEventListener('activate', funcionDeActivacion);


// FETCH
// Hacemos peticiones a recursos.
self.addEventListener('fetch', funcionDeFetch);


// PUSH
self.addEventListener('push', funcionDePush);
```

El código fuente completo puede verse en [public/service-worker.js](./public/service-worker.js)

Además de todo lo anterior, deberemos modificar el archivo **`index.html`** para que aparezcan las siguientes líneas:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <!-- Se eliminan etiquetas html para resaltar lo esencial -->
  <!-- Consulta el código fuente. --> 

	<link rel="icon" type="image/png" href="/favicon.png">
  
	<!-- PWA: Para habilitar Progressive Web Application -->
	<link rel="manifest" href="manifest.json">  <!--                  IMPORTANTE -->
  
	<!-- PWA: Añadir a pantalla de inicio para Safari en iOS -->
	<meta name="apple-mobile-web-app-capable" content="yes">
	<meta name="apple-mobile-web-app-status-bar-style" content="black">
	<meta name="apple-mobile-web-app-title" content="Tienda">
	<link rel="apple-touch-icon" sizes="152x152" href="/images/icons/icon-152x152.png">
	<meta name="msapplication-TileImage" content="/images/icons/icon-144x144.png">
	<meta name="msapplication-TileColor" content="#fdebc9">
  
  <!-- Chrome, Firefox OS and Opera -->
  <meta name="theme-color" content="#fdebc9">

  <!-- Se eliminan etiquetas html para resaltar lo esencial -->
  <!-- Consulta el código fuente. --> 
</head>

<body>
	<noscript>
		<p> Este sitio necesita Javascript para funcionar. </p>
	</noscript>
	<script>
		// Si está soportado serviceWorker por el navegador
		if ('serviceWorker' in navigator) {
		  window.addEventListener('load', () => {
			navigator.serviceWorker
			  .register('./service-worker.js')
			  .then(reg => console.log('[Service Worker] * Registrado.'))
			  .catch(err => console.log(`[Service Worker] * Error: ${err}`));
		  });
		}
	  </script>
	
	  <script src="service-worker.js"></script> <!-- Gestión de eventos del ServiceWorker -->
</body>
</html>
```

Lo que hacemos es **añadir un enlace al archivo `manifest.json`** e indicar los iconos y colores que usaremos.

Además en el `body` de la página, registramos el `service-worker.js` y lo cargamos.

El código fuente completo puede verse en [public/index.html](./public/index.html)

Por último, es recomendable tener un archivo llamado *`offline.html`* o similar, que mostraremos cuando no haya conexión. 

```html
<!DOCTYPE html>
<html lang="es">
<head>
</head>
  <!-- Se eliminan etiquetas html para resaltar lo esencial -->
  <!-- Consulta el código fuente. --> 
<body>
    Estamos sin conexión
    
    <script>
        // Este código detecta cuando volvemos a tener conexión
        // y en ese caso se carga automáticamente la página principal.
        // El usuario no necesita refrescar la página.
        window.addEventListener("online", () => (window.location.href = "/"));
    </script>
</body>
</html>
```

## Auditoría de la aplicación

Podemos realizar una auditoría de la aplicación, haciendo uso de la extensión **Lighthouse** de Chrome. Para instalar dicha extensión en el navegador chrome escribimos la URL chrome://extensions/.

Si pulsamos la tecla `F12` para mostrar las `Dev Tools` podremos ver una pestaña con el nombre `Audits`. Desde ahí realizaremos la auditoría.


![ScreenCast](screencast.gif)


> NOTA: Algunas extensiones activas en el navegador pueden ralentizar las pruebas y provocar que el *score* obtenido sea menor. Para evitar esto podemos lanzar la auditoría desde el `modo incógnito` del navegador o, una solución más drástica, desactivar las extensiones.
