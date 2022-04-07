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