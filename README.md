# Markdown Links

## Índice

* [1. Resumen](#1-Resumen)
* [2. Como Usarlo ?](#2-como-usarlo)
* [3. Diagramas de flujo](#3-Diagramas-de-flujo)
* [4. Ejemplos](#4-Ejemplos)

***

## 1. Resumen


Markdown Links es una poderosa herramienta de línea de comandos (CLI) y una biblioteca (library) en JavaScript que te permite detectar y validar enlaces rotos en archivos .md. Al instalar este módulo, podrás verificar el estado de tus enlaces y garantizar su funcionalidad. Con Markdown Links, podrás mantener tus documentos Markdown actualizados y asegurarte de que los enlaces incluidos sigan siendo válidos. Esta herramienta es especialmente útil para escritores, desarrolladores y cualquier persona que trabaje con archivos Markdown y desee mantener la integridad de sus enlaces. ¡No más enlaces rotos!

## 2. Como Usarlo ?

Para que funcione correctamente deberas Instalarlo 

Se puede instalar usando npm install YEISIDIAZ/DEV004-md-links

### CLI (Command Line Interface - Interfaz de Línea de Comando)

El ejecutable de nuestra aplicación debe poder ejecutarse de la siguiente
manera a través de la **terminal**:

`md-links <path-to-file> [options]`

Por ejemplo:

```sh
$ md-links ./some/example.md
$ md-links ./pruebas

```

El comportamiento por defecto no debe validar si las URLs responden ok o no,
solo debe identificar el archivo markdown (a partir de la ruta que recibe como
argumento), analizar el archivo Markdown e imprimir los links que vaya
encontrando, junto con la ruta del archivo donde aparece y el texto
que hay dentro del link

#### Options

##### `--validate`

Si pasamos la opción `--validate`, el módulo debe hacer una petición HTTP para
averiguar si el link funciona o no. Si el link resulta en una redirección a una
URL que responde ok, entonces consideraremos el link como ok.

Por ejemplo:

```sh
$ md-links ./some/example.md --validate
$ md-links ./pruebas --validate
```

Vemos que el _output_ en este caso incluye la palabra `ok` o `fail` después de
la URL, así como el status de la respuesta recibida a la petición HTTP a dicha
URL.

##### `--stats`

Si pasamos la opción `--stats` el output (salida) será un texto con estadísticas
básicas sobre los links.

```sh
$ md-links ./some/example.md --stats
$ md-links ./pruebas --stats
```

También podemos combinar `--stats` y `--validate` para obtener estadísticas que
necesiten de los resultados de la validación.

```sh
$ md-links ./some/example.md --stats --validate
$ md-links ./pruebas --stats --validate
```
## 3. Diagramas de flujo

En este proyecto, se han creado dos diagramas de flujo para establecer claramente los pasos a seguir tanto en la API como en la línea de comandos. Estos diagramas de flujo proporcionan una representación visual de los procesos involucrados en cada parte del proyecto. Para la API, el diagrama de flujo muestra de manera detallada las solicitudes, respuestas y acciones necesarias para el funcionamiento adecuado de la interfaz de programación de aplicaciones. Por otro lado, el diagrama de flujo de la línea de comando ilustra los pasos necesarios para ejecutar comandos, procesar archivos Markdown y mostrar los resultados. Estos diagramas de flujo son herramientas valiosas que ayudan a comprender y seguir el flujo de trabajo de manera clara y efectiva en todo el proyecto.

![api](imgapi.jpg)

![cli](imgcli.jpg)

