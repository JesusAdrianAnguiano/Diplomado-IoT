# **TEORÍA Y COMANDOS PARA GIT Y GITHUB**

En este archivo se añadirá teoria de Git y GitHub además se mostraran los principales comandos necesarios para la creación de repositorios locales en Git y remotos desde GitHub desde la terminal de Ubuntu, así como su modificación y actualización.

## Git y GitHub

> Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia, la confiabilidad y compatibilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente. -Wikipedia.
 
>GitHub es una forja para alojar proyectos utilizando el sistema de control de versiones Git. Se utiliza principalmente para la creación de código fuente de programas de ordenador. El software que opera GitHub fue escrito en Ruby on Rails. Desde enero de 2010, GitHub opera bajo el nombre de GitHub, Inc. -Wikipedia.
***
Básicamente son para generar repositorios, en estos puedes controlar las versiones que se van creando de un proyecto (por lo general de programación), además estos repositorios pueden ser remotos, es decir, pueden trabajar como servidores, el equipo de trabajo de un proyecto puede adjuntar o descargar contenido desde la plataforma de GitHub.



### Crear repositorios
1. Primero se debe crear una carpeta en donde se encontrará el repositorio.
2. Para crear repositorios en Git desde la terminal se utiliza el comando:
~~~
git init [nombre del repositorio]
~~~
3. Asegurate de usar este comando estando en la direccion de tu carpeta
4. Cuando se ejecuta el comando se crea una carpeta y dentro de esta un archivo oculto llamado .git

### Analizar si los archivos sufrieron cambios
Git se encarga de revisar si los archivos dentro de tu repositorio están modificados, de ser así, al ejecutar el comando:
~~~
git status
~~~
Nos mostrará si los archivos dentro de la rama en la que estamos ha sido modificada, esto remarcando el nombre del archivo en **rojo**.
### Supervisar archivos ó fase de stage

![Staging Area](https://git-scm.com/images/about/index1@2x.png){width=250 height=150}

Cuando modificamos un archivo y lo guardamos es necesario hacer un stage, o lo que es
