# Curso de Asincronismo con JavaScript.
## 🤹🏻‍♀️ **Clase #2: Qué es el asincronismo 2/21** 🤹🏾‍♂️

### ** Conceptos importantes para entender el asincronismo:✍🏾** 

-  🧵  Thread: Thread para Javascript permite realizar programación multihilos en este entorno. En realidad, simula la creación y ejecución de hilos, pero para el desarrollador es lo mismo. Ésto simplifica muchísimo la creación de aplicaciones Javascript.

*  🚫 **Bloqueante:** Una llamada u operación bloqueante no devuelve el control a la aplicación hasta que se ha completado. Por tanto el thread queda bloqueado en estado de espera.
* 🚿 **No bloqueante: **Una tarea no bloqueante se devuelve inmediatamente con independencia del resultado. Si se completó, devuelve los datos. Si no, un error.

*  🎞️ **Síncrono:** Las tareas se ejecutan de forma secuencial, se debe esperar a que se complete para continuar con la siguiente tarea.

* 🚦 **Asíncrono:** Las tareas pueden ser realizadas más tarde, lo que hace posible que una respuesta sea procesada en diferido. La finalización de la operación I/O (entrada/salida) se señaliza más tarde, mediante un mecanismo específico como por ejemplo un callback, una promesa o un evento, lo que hace posible que la respuesta sea procesada en diferido.
* 🛤️ **Paralelismo**: El paralelismo es la ejecución simultánea de dos o más tareas. Algunas tareas se pueden dividir en partes más pequeñas que pueden ser resueltas simultáneamente.

*  🎮 **Concurrencia:** La concurrencia es la capacidad de un algoritmo o programa para ejecutar más de una tarea a la vez. El concepto es similar al procesamiento paralelo, pero con la posibilidad de que muchos trabajos independientes hagan diferentes cosas a la vez en lugar de ejecutar el mismo trabajo.
• 🌀 **Eventloop o Loop de eventos:** El bucle de eventos es un patrón de diseño que espera y distribuye eventos o mensajes en un programa.
.
###  Formas de manejar la asincronía en JavaScript:  📝 Formas de manejar la asincronía en JavaScript: 

-  📩 **Callbacks:** Una función que se pasa como argumento de otra función y que será invocada.

-  🫱🏼‍🫲🏾 **Promesas: **(implementado en ES6) Una promesa es una función no-bloqueante y asíncrona la cual puede retornar un valor ahora, en el futuro o nunca.

-  🛣️ **Async / Await:** (implementado en ES2017) Permite estructurar una función asincrónica sin bloqueo de una manera similar a una función sincrónica ordinaria.
.
- 📌 En JavaScript casi todas las operaciones de I/O (Entrada y Salida) no se bloquean. A esto se le conoce como asíncronismo. Lo único que no es procesado antes de que termine la operación son los callbacks, ya que éstos están amarrados a una operación y esperan a que sea finalizada para poder ejecutarse.
.
- ⏳ El asincronismo es una manera de aprovechar el tiempo y los recursos de la aplicación, ejecutando tareas y procesos mientras otros son resueltos en background (como la llegada de la información de una API), para posteriormente continuar con las tareas que requerían esa información que no tenías de manera instantánea.
.
- ⏲️ Un ejemplo fácil de asincronismo vs sincronismo es invitar a unos amigos a una fiesta y ofrecer una parrillada. Primero decides colocar la carne y verduras a la parrilla y luego repartir bebidas y algo para picar (snacks). Si fuera una persona síncrona (Blocking) tendrías que esperar a que la comida de la parrilla esté cocinada y luego atender a los invitados. Pero si fuera una persona asíncrona (Non Blocking) luego de poner la carne al carbón, sacas las bebidas frías de la nevera y compartes con los invitados mientras se cocina la car
ne. La acción de que la comida en la parrillada esté lista sería un callback que está esperando que finalice el proceso para ejecutarse. Pero otros procesos (como compartir la velada con bebidas y algo de picar) ya podrían irse realizando.
## ⚙️ **𝗖𝗹𝗮𝘀𝗲 #𝟱: 𝗖𝗼𝗻𝗳𝗶𝗴𝘂𝗿𝗮𝗰𝗶ó𝗻 𝟱/𝟮𝟭** ⚙️

###  Conceptos fundamentales antes de crear el proyecto:🖋️

Web APIs JavaScript del lado del cliente: setTimeout, XMLHttpRequest, File Reader, DOM. Node: fs, https.

**API:** El término API es una abreviatura de “Application Programming Interface” (Interfaz de programación de aplicaciones en español). Es un conjunto de rutinas que provee acceso a funciones de un determinado software.

**Hoisting:** Sugiere que las declaraciones de variables y funciones son físicamente movidas al comienzo del código en tiempo de compilación.

**XML:** Lenguaje de marcado creado para la transferencia de información, legible tanto para seres humanos como para aplicaciones informáticas, y basado en una sencillez extrema y una rígida sintaxis. Así como el HTML estaba basado y era un subconjunto de SGML, la reformulación del primero bajo la sintaxis de XML dio lugar al XHTML; XHTML es, por tanto, un subconjunto de XML.

**DOM:** El DOM permite acceder y manipular las páginas XHTML como si fueran documentos XML. De hecho, DOM se diseñó originalmente para manipular de forma sencilla los documentos XML.

**Events: **Comportamientos del usuario que interactúa con una página que pueden detectarse para lanzar una acción, como por ejemplo que el usuario haga click en un elemento (onclick), que elija una opción de un desplegable (onselect), que pase el ratón sobre un objeto (onmouseover), etc.

**Compilar:** Compilar es generar código ejecutable por una máquina, que puede ser física o abstracta como la máquina virtual de Java.
Transpilar: Transpilar es generar a partir de código en un lenguaje código en otro lenguaje. Es decir, un programa produce otro programa en otro lenguaje cuyo comportamiento es el mismo que el original.
.
.
### 🛠️ Crear e inicializar un Proyecto:

- Tener instalado Visual Studio Code.

- Abrir la terminal (en Linux al presionar las teclas Ctrl + Alt + T).

- Para conocer donde estamos ubicados se escribe pwd y se da ENTER.

- Para ver las carpetas y archivos del lugar donde estamos, se escribe ls y se da ENTER.

- Para crear una carpeta se escribe mkdir nombre-de-la-carpeta y se da ENTER.

- Para entrar a una carpeta se escribe cd nombre-de-la-carpeta y se da ENTER.

- Si se quiere ir a la carpeta contenedora de la carpeta actual que estamos, se escribe cd … y se da ENTER.

- En linux para no escribir los comando de mkdir y cd, se escribe take nombre-de-la-carpeta y se da ENTER.

- Para crear un archivo se escribe touch nombre-del-archivo-extensión y se da ENTER.

- Para limpiar la pantalla en la terminal se escribe clear y se da ENTER.

- Si solo se quiere mover el scroll se presionan las teclas Ctrl + Alt + l

- Para iniciar el repositorio se escribe git init y se da ENTER.

- Vamos a inicializar el proyecto con npm, se escribe npm init y se da ENTER.

- Aparece el nombre del proyecto, si no se quiere modificar el nombre, se da ENTER.

- Aparece la versión del proyecto, si no se quiere modificar el número, se da ENTER.

- Aparece la descripción del proyecto, si se quiere modificar dejar vacío, se da ENTER.

- Lo mismo, dejar vacío: entry point, test command, git repository.

- En keywords se escribe las palabras claves como javascript y se da ENTER.

- En la licencia por defecto aparece la ISC, pero la más común es la MIT para compartir y poder comercializar después el producto.

- Por último, aparecen los datos ingresados (guardados en el archivo package.json) y si no hay que modificar, se escribe yes y se da ENTER.

- Para entrar al editor VSC se escribe code . y se da ENTER.

- Una vez dentro de VSC, en el panel izquierdo aparece el archivo package.json, crear una nueva carpeta llamada src donde contendrá nuestro código.

- Crear el archivo .gitignore (estará fuera de la carpeta src). En los sistemas Unix, dado que el archivo empieza con un punto, al abrir un explorador de archivos los toma como archivos ocultos y no son visibles. El contenido del archivo queda:
 -      /node_modules/
 - Para guardar los cambios de un archivo, presionar las teclas Ctrl + S

  - Muy importante instalar la extensión Code Runner, presionar las teclas Ctrl + P y pegar: ext install formulahendry.code-runner y dar ENTER. Lo instala automáticamente (fuente: aquí).
## 📩 **𝗖𝗹𝗮𝘀𝗲 #𝟲: 𝗤𝘂é 𝘀𝗼𝗻 𝗹𝗼𝘀 𝗖𝗮𝗹𝗹𝗯𝗮𝗰𝗸𝘀 𝟲/𝟮𝟭** 📩

🪃 Un Callback es una una función que se pasa como argumento de otra función y que será invocada.

   - ✏️ **Ejemplos:**
- En VSC crear una carpeta dentro de la carpeta src llamada callback.
- Crear dentro de la carpeta callback el archivo index.js.
- Dentro de index.js se coloca la estructura de los que será un callback:



    function sum(num1, num2){
    return num1 + num2;
    }
    
    function calc(num1, num2, callback) {
    return callback(num1, num2);
    }; //No necesariamente se debe llamar callback
    
    console.log(calc(2, 2, sum)); //sum debe estar sin () y sin argumentos
    //

   - 
    - Luego se selecciona el código y al dar click derecho, seleccionar Run Code (debe estar instalado la extensión Code Runner).

    - Aparece abajo la consola con la salida de la suma de los 2 números.

    - Para el segundo ejemplo, se tiene un setTimeout que funciona como un callback, en el código está configurado para imprimir el mensaje 2 segundos después de ejecutar el código con Run Code:
         

     setTimeout(function (){
      	console.log('Hola JavaScript');
      }, 2000) 
      //la función es anónima por eso no tiene nombre


  - - En El Tercer Ejemplo Tenemos Un Settimeout Con Una FuncióN Que Se Le Pasa Por Argumento:



                function gretting(name){
                	console.log(`Hola ${name}`);
                }
            setTimeout(gretting, 2000, 'Maria');
    		//se pasa primero la función, de segundo el tiempo de espera y el argumento

🆘 Si tienen problemas con conseguir las comillas invertidas ` `` ` en el enlace hay varias respuestas: aquí
