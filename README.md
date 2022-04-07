# Curso-de-Webpack

# 📒 v1 ¿Qué es Webpack?


Básicamente webpack es un paquete de módulos y esto lo que hace es que nuestra aplicación puede tener archivos JavaScript o jsx, archivos sass, imágenes y empaquetarlos como si fuera una caja (todo en uno).

![webpack](./img/v1.gif)

Webpack se puede configurar desde la terminal usando un CLI o un archivo de configuración especial llamado webpack.config.js

## Ideas/conceptos claves
+ `Module bundlers`: son herramientas de frontend que nos permiten usar archivos con módulos JavaScript, entre otras características y convertiros a un JavaScript el cual el navegador pueda entender.
    + Webpack es una herramienta que nos permite preparar nuestro código para llevarlo a producción (module bundler)
    + Webpack nos permite trabajar con
        + HTML
        + CSS
        + JavaScript
        + Archivos estáticos
        + Imágenes
        + Fuentes
+ Tambien nos permite tener un modo en desarrollo para nuestros proyectos para hacer pruebas.
+ Nacio en el 2012, desde ese entonces varias empresas lo usan como ser: Twitter, Instagram, PayPal
+ También nos permite 
    + Gestionar dependencias
    + Ejecutar tareas
    + Conversión de archivos
+ Nos permite trabajar en módulos
    + Permitiéndonos tener un código separado en desarrollo, pero en producción en una fuente
    + Webpack permite tener módulos de JS en formato 
        + AMD
        + Common JS
        + ES15
RESUMEN: Webpack es un module bundler que nos permite trabajar con una variedad de tecnologías web empezando desde HTML y terminando con JS. Además de tener soporte para archivos estáticos.

enlace: https://dev.to/tanhauhau/what-is-module-bundler-and-how-does-it-work-3gp2

![webpack](./img/v1.webp)

# 📒 v2 - Conceptos básicos de Webpack

## Ideas/conceptos claves</h4>
+ `Webpack` es un paquete de módulos estáticos para aplicaciones de JS modernas
+ `Loader` Te permite hacer un bundle de cualquier recurso estático más allá de JavaScript
+ `Plugins` Extienden recursos para añadir configuraciones y particularidades de recursos externos
+ `Webpack` construye un gráfico de dependencias que mapea cada módulo para con verlo en uno o más módulos. 
+ Desde `webpack 4` ya no dependemos de tener un archivo de configuración, pero si debemos tener un punto de entrada.
+ Tambien tendremos que tener un punto de salida.
    + En este punto se creará nuestro proyecto una vez esté preparado
    + Normalmente es la carpeta dist ⇒ Distribution
+ Tambien contamos con diferentes modos
    + Modo de desarrollo
    + Modo de producción
    + Modos de performance
        + Donde tu añades
            + Configuraciones de minificación
            + Donde se va enviar
            + Carpeta de destino
+ Modos de desarrollo local
    + Donde puedes
        + Crear puertos específicos para tu proyecto
        + Ver cambios en tiempo real
+ Dispone de loader y plugins permitiéndonos preparar particularidades de nuestro proyecto.

## Conceptos Básicos Webpack

+ `Entry` (punto de entrada): este le indica a webpack cual modulo de JavaScript debe de usar para empezar a crear una salida.
    + Ejemplo : index.js. también podemos tener múltiples puntos de entrada pero eso es otra historia.

+ `Output` (punto de salida): Este archivo es el bundle o nuestro archivo de salida, sería nuestra caja donde empaquetamos toda nuestra aplicación, normalmente este archivo final se crea en una carpeta llamada dist

+ `Loader` (transformador): Los loaders lo que hacen es decirle a webpack como tiene que transformar el código de un modulo en concreto. 
    + Ejemplo : Los loaders pueden transformar ficheros a JavaScript, o cargar CSS directamente en archivos JS, (si usas reactjs ya sabrás como)
 
+ `Plugins` (complementos): Nos van a ayudar a extender las funcionalidades con los loaders, añadir otras configuraciones.
    + Ejemplo : hay un modulo llamado HTMLWebpackPlugin que este se encarga de crear un HTML personalizado que le inyecta todos los bundles finales que compilamos.

## ¿Babel es un compilador al cual se le puede considerar también un loader?

Se usa en webpack como loader 🖖

## En resumen ¿es para empaquetar tus archivos de desarrollo?

+ Webpack funciona como un empaquetador de módulos, pero que también hace otras cosas como:
    + Gestión de dependencias
    + Ejecución de tareas
    + Conversión de formatos
    + Te dejo este artículo sobre webpack

enlace: https://webpack.js.org/concepts/

# 📒 v3 - Tu primer build con Webpack

Creamos una carpeta como le quieras llamar
(Bueno no! si eres de Windows te dejo este articulo cortito de los nombres de carpetas PROHIBIDOS )
La creamos desde la terminal con mkdir y luego entramos a ella con cd

```
    mkdir curso-webpack
    cd curso-webpack
```
una vez que entres a la carpeta inicializamos nuestro repositorio con git

```
    git init
```

El paso que sigue es inicializar nuestro proyecto con npm y si no sabes de npm aqui esta el curso del profesor

```
    npm init -y
```

o si les da error “Invalid Name” usen para personalizar la configuración

```
    npm init
```

y para abrir el proyecto como flash es poner en la terminal y les abre el editor ( si usas VS CODE)

```
    code .
```

La carpeta SRC es el source de todo el proyecto ( index.js , imágenes, utils, assets, helpers, database, etc).

** Instalación de Webpack**
si no quieres escribir ese comando también puedes usar este
la i de install

```
    npm i webpack webpack-cli -D
```

o si usas yarn usa

```
    yarn add webpack webpack-cli -D
```

Y luego ejecutamos webpack
npx lo que hace es ejecutar paquetes directamente de npm, este viene instalado de npm

```
    npx webpack
```

Al hacer esto webpack creo una carpeta llamada dist, esto lo hace por defecto webpack sin preguntarnos.
Modo de desarrollo
Por defecto webpack al compilar nuestro proyecto setea el modo “production” implícitamente pero podemos definirle el modo explícitamente corriendo:

```
    npx webpack --mode production
    npx webpack --mode development
```

La diferencia radica que el modo development deja el código mas legible para los desarrolladores pero con comentarios, el modo production deja el código comprimido y mas limpio para usarse.

![comandos](./img/v3.webp)

## ¿Que significa el “npx” exactamente?

Es una extensión de `npm` para ejecutar una dependencia, generalmente global o sin una instalación como tal de npm.
Si te preguntabas del acrónimo, pues Node Package Execute.

## ¿Se debe instalar webpack cada vez que lo vaya a usar en un proyecto?

Si, ademas, es mas simple , con el tiempo te acostumbras. Puedes subir a tu github un arhivo llamado basewebpack y simplemente descargarlo.

# 📒 v4 - Instalación de Webpack y construcción del proyecto

## 👣 Pasos de la clase
+  1. Clonar el proyecto

```
    git clone https://github.com/gndx/js-portfolio.git
```

+ 2. Instalar webpack con npm.

```
    npm install webpack webpack-cli -D 
```
con Yarn

```
    yarn add webpack webpack-cli -D 
```

![resumen](./img/v4.png)

## ¿Por que cuando tengo fuente de google fonts me las pone en la raiz?

Lo más probable es que tengas archivos que estás importando además de las etiquetas que traen las fuentes de google. 

# 📒 v5 - Configuración de webpack.config.js ⚙️

1.  El archivo de configuración nos va ayudar a poder establecer la configuración y elementos que vamos a utilizar
2.  Para poder crear el archivo de configuración en la raíz del proyecto creamos un archivo llamado `webpack.config.js`
    + En el mismo debemos decir:
        + El punto de entrada
        + Hacia a donde a enviar la configuración de nuestro proyecto
        + Las extensiones que vamos usar

```
    const path = require('path');

    module.exports = {
    // Entry nos permite decir el punto de entrada de nuestra aplicación
    entry: "./src/index.js",
    // Output nos permite decir hacia dónde va enviar lo que va a preparar webpacks
    output: {
        // path es donde estará la carpeta donde se guardará los archivos
        // Con path.resolve podemos decir dónde va estar la carpeta y la ubicación del mismo
        path: path.resolve(__dirname, "dist"),
        // filename le pone el nombre al archivo final
        filename: "main.js"
    },
    resolve: {
        // Aqui ponemos las extensiones que tendremos en nuestro proyecto para webpack los lea
        extensions: [".js"]
    },
    }
```

+ El flag —config indica donde estará nuestro archivo de configuración

```
    npx webpack --mode production --config webpack.config.js
```

+ Para poder hacerlo más amigable el comando puedes crear un script en package.json

```
    "scripts": {
            ...
        "build": "webpack --mode production --config webpack.config.js"
    },
```

RESUMEN: Puedes crear un archivo webpack.config.js en el cual estarán las configuraciones con las cuales webpack trabajara, entre ellas están los puntos de entrada y salida, extensiones de archivos, entre otras características que se verán próximamente en él curso.

👀👀
**Actualmente no es necesario añadir el flag --config webpack.config.js ya que es el archivo que detecta por defecto, entonces basta con hacer npx webpack --mode production**

## webpack.config.js

Este archivo es donde se controla toda la configuración de webpack, de modo que podamos darle un comportamiento personalizado de acuerdo a nuestras necesidades. Este archivo debe estar en la raíz de nuestro proyecto al nivel del package.json pero también podemos colocarlo en otra ruta pero eso es another history .

El archivo tiene que realizar una exportación de un objeto JavaScript que contendrá la configuración de webpack

```
    const path = require('path'); // Para trabajar con archivos y rutas de directorios

    module.exports = {
        mode: 'production', // le pasamos explicitamente el modo desde el archivo
        entry: './src/index.js', // el punto de entrada de mi aplicación
        output: { // Esta es la salida de mi bundle
            path: path.resolve(__dirname, 'public_html/js'),
            // resolve lo que hace es darnos la ruta absoluta de el S.O hasta nuestro archivo
            // para no tener conflictos entre Linux, Windows, etc
            filename: 'main.js', 
            // EL NOMBRE DEL ARCHIVO FINAL,
        },
        resolve: {
            extensions: ['.js'] // LOS ARCHIVOS QUE WEBPACK VA A LEER
        }
    }
    

```

Después de configurar el archivo de configuración, vamos directo a la terminal a ejecutar el siguiente comando para que tome en cuenta nuestras configuraciones

```
    npx webpack --mode production --config webpack.config.js
```

Para hacer más amigable la ejecución del comando, vamos a package.json y hacemos un script

```
    "build": "webpack --mode production"
```

otro ejemplo:

```
        const path = require('path')

        module.exports = {
            /* Aquí indicamos el elemento inicial de nuestra app.
            O sea, nuestro punto de entrada */
            entry: './src/index.js',

            /* Ahora indicamos cual va a ser el archivo de salida,
            donde va a estar todo el código que compile */
            output: {
                /* Aquí indicamos donde queremos que se guarde el proyecto */
                path: path.resolve(__dirname, 'dist'),
                /* Y colocamos el nombre del .js que va guardar */
                filename: 'main.js',
            },

            /* Vamos a indicar con extensiones vamos a trabajar en
            este proyecto */
            resolve: {
                /* Importante pasar las extensiones con las que vamos a
                trabajar, como .jsx (React.js)  */
                extensions: ['.js']
            }
        }
```

## Preguntas y Respuestas ❓

## Yo tengo una duda respecto a webpack cuando no estoy trabajando con Vanilla Javascript. Cuando yo solo tengo un index.html, una carpeta de estilos y un archivo de javascript cuan seria el punto de entrada. Me refiero a que cuando no tenga la misma estructura de archivos que tiene el profesor en esta clase como configuraria el punto de emtrada ???

El punto de entrada debería ser un archivo de javascript, sin importar el nombre que decidas ponerle. Yo usualmente los llamos “main.js” o “index.js”.

## ¿En la config de webpack, porque no se aniade tmbn .css o .html a la parte de extensions en resolve ?

Hey ! En la parte de las extensiones normalmente añades las extensiones de los archivos con los que vas a estar construyendo tu aplicacion como bien lo son .js y .jsx ya que estaras importando modulos(archivos) con estas extensiones , no estaras importando ningun .html y los archivos .css no son parte de la logica de tu aplicacion solo traen los estilos

Hay que tener presente que webpack solo entiende archivos .js y .json.
Los loaders son los que nos ayudan a extender los “lenguajes” que va a interpretar webpack.

## ¿Que es (___dirname) que quiere decir esta parte?

(__dirname) devuelve la ruta de la carpeta en donde se encuentra el archivo donde estamos.
Si tú escribes ‘_dirname’ en ‘/src/template/file.js’, te debería retornar ‘/src/template’.

# 📒 v6 - Babel Loader para JavaScript


+ Babel sirve para transformar código JavaScript moderno en código que cualquier navegador pueda ejecutar. Para trabajar con el y con Webpack se deben añadir las siguientes dependencias al proyecto:
    + babel-loader: Loader para que Webpack lo entienda
    + @babel/core: El núcleo de la librería
    + @babel/preset-env: Preset para JS moderno
    + @babel/plugin-transform-runtime: Trabajar con asíncronismo

+ El archivo .babelrc es el archivo de configuración de Babel, se crea en la raíz del proyecto. Aquí se definen los presets y los plugins con los que Babel va a trabajar:
+ Ahora hay que indicarle a Webpack que trabaje con Babel, para esto se utiliza el babel-loader que instalamos.
+ Para esto se crea un nuevo módulo en el archivo de configuración de Webpack, dentro la propiedad rules que es un arreglo, dentro del arreglo un objeto y dentro de este las siguiente propiedades:
    + Test: Se usan RegEx para indicar que archivos va a procesar
    + Exclude: Indica que archivos no va a procesar. Siempre incluir node_modules
    + Use: Un objeto con la propiedad loader que indica el loader que se usará.

+ Para instalar Babel utilizamos el comando:

```
    npm install babel-loader @babel/core @babel/preset-env @babel/plugin-transform-runtime -D
```

+ Ahora para configurar Babel, vamos a crear un archivo llamado .babelrc

```
    {
        "presets": [
            "@babel/preset-env"
        ],
        "plugins": [
            "@babel/plugin-transform-runtime"
        ]
    }
```

+ Ahora en nuestro archivo de `webpack.config.js` tenemos que indicarle que va a trabajar con Babel. Lo hacemos de la siguiente forma:

```
            module: {
            rules: [
                {
                    /* Indicamos la extención de los archivos que va 
                    a estar compilando */
                    test: /\.m?js$/,
                    /* Recuerda excluir la carpeta node_modules */
                    exclude: /node_modules/,
                    use: {
                        loader: 'babel-loader'
                    }
                }
            ]
        }
    }
```

## Preguntas y Respuestas ❓

## ¿Qué es exactamente un loader? esta seccion del curso lleva como tema loader y plugins, se hace uso de babel-loader pero no espsifica que es un loader o cual es su funcion exacatemnte y no logro encontrar alguna documentacion que me saque de duda, podrian orientarme un poco.

Los loaders perminten preprocesar archivos. Esto te permite empaquetar cualquier recurso estático más allá de JavaScript. Son los que permiten importar archivos de CSS dentro de tu JS, por ejemplo.
link: https://webpack.js.org/loaders/

## ¿No entiendo bien para que sirven los 4 plugins que instalaste de babel?

Son loaders y funcionan para que webpack pueda hacer la conversión que hace babel de forma automática. Tendrías que meterte más a la documentación de babel para entender específicamente lo que hacen. Sin embargo, te puedo decir que la funcionalidad de babel es habilitar la sintaxis de JS actual a un códgio viejo para que cualquier navegador pueda usarlo sin problemas de compatibilidad.

## ¿Qué pasa si no se instalan como dependencias de desarrollo? Es decir sin -D, ¿afecta el proyecto?

Hola Hackguar! Si no se instalan como dependencias de desarrollo se mostraran como dependencias de producción. Muchas veces para desarrollar un proyecto utilizamos dependencias que no se necesitaran en producción. Para la persona que realice el deploy ahorra mucho tiempo que le indiques que paquetes son necesarios en producción.

## ¿Por qué en el script de build ya no usas npx webpack y solo usas webpack?

npx en un ejecutador de los paquetes de Node. Lo que significa que te servirá para ejecutar un comando de un paquete de npm sin la necesidad de haberlo instalado.

Entonces, si no tienes instalado el paquete pero quieres usar su comando, ejecutas npx <comando>; Peeeeeero si ya instalaste en tu entorno local o global (en tu computadora), ya tienes acceso directamente al comando, sin necesidad de ejecutar npx.

El profesor ya no ejecutó npx webpack porque instaló webpack en su sistema.

Puedes probarlo tú mismo. Escribe webpack en tu terminal, si se ejecuta es porque ya está instalado en tu máquina, si no lo reconoce como un comando, puedes ejecutarlo con npx webpacko instalarlo con npm i webpack y después ya no tendrás necesidad de hacer npx webpaxck, solo webpack.

## ¿Según la documentación toca crear babel.config.json o .babelrc.json pero aquí usan solo .babelrc ¿porqué no se rompe?

.babelrc es un alias de .babel.json

Puedes chequear esta documentación de Babel para ver más detalles sobre los archivos de configuración y la diferencia entre ellos.