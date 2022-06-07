# **TEORÍA Y COMANDOS PARA GIT Y GITHUB**

En este archivo se añadirá teoria de Git y GitHub además se mostraran los principales comandos necesarios para la creación de repositorios locales en Git y remotos desde GitHub desde la terminal de Ubuntu, así como su modificación y actualización.
***
## Git y GitHub

> Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia, la confiabilidad y compatibilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente. -Wikipedia.
 
>GitHub es una forja para alojar proyectos utilizando el sistema de control de versiones Git. Se utiliza principalmente para la creación de código fuente de programas de ordenador. El software que opera GitHub fue escrito en Ruby on Rails. Desde enero de 2010, GitHub opera bajo el nombre de GitHub, Inc. -Wikipedia.
***
Básicamente son para generar repositorios, en estos puedes controlar las versiones que se van creando de un proyecto (por lo general de programación), además estos repositorios pueden ser remotos, es decir, pueden trabajar como servidores, el equipo de trabajo de un proyecto puede adjuntar o descargar contenido desde la plataforma de GitHub.
***
### Crear repositorios

1. Primero se debe crear una carpeta en donde se encontrará el repositorio.
2. Para crear repositorios en Git desde la terminal se utiliza el comando:
~~~
git init [nombre del repositorio]
~~~
3. Asegurate de usar este comando estando en la direccion de tu carpeta
4. Cuando se ejecuta el comando se crea una carpeta y dentro de esta un archivo oculto llamado .git
***
### Analizar si los archivos sufrieron cambios

Git se encarga de revisar si los archivos dentro de tu repositorio están modificados, de ser así, al ejecutar el comando:
~~~
git status
~~~
Nos mostrará si los archivos dentro de la rama en la que estamos ha sido modificada, esto remarcando el nombre del archivo en **rojo**.
***
### Supervisar archivos ó fase de staging

<p> 
<img src="https://git-scm.com/images/about/index1@2x.png" width="500px"align="left">
</p>

Cuando modificamos un archivo y lo guardamos es necesario hacer un stage, que es mover los archivos supervisados previamente a un pre-commit, es decir, eliges los archivos a los que les harás posteriormente un **commit**, esto se procede utilizando el comando:
~~~
git add [archivo modificado]
~~~
Cuando tenemos una **gran cantidad de archivos en modificados** y para no escribir en comandos todos estos utilizamos un comando que envía al area de staging todos los archivos modificados:
~~~
git add .
~~~
Posterior a este comando los archivos modificados que aparecen al ejecutar "git status" aparecerán en **verde**.
***
### Crear commits

Un commit es una modificación documentada, en este se muestra quién hizo la modificación, a qué hora la hizo, en que rama, etc. Cada commit tiene un código único con el cual podemos por ejemplo regresar a la versión en la que se hizo este o tambiém ver de que trata la modificación viendo el mensaje que contiene dicho commit.
Para hacer un commit es necesario tener los archivos en el area de staging, teniendo esto ejecutamos:
~~~
git commit -m "[Mensaje del commit]"
~~~
Es muy importante colocar un mensaje en el commit, ya que este nos servirá para saber que contienen las modificaciones hechas.
***
### Comandos relacionados a commits

Para **visualizar todos los commits** que se han realizado en un archivo de forma detallada se puede ejecutar el comando:
~~~
git log
~~~
Para verlos de forma resumida en una linea:
~~~
git log --oneline
~~~
Si además de ver los commits queremos ver los cambios dentro de estos utilizamos:
~~~
git show
~~~

<p> 
<img src="https://git-scm.com/images/about/branches@2x.png" width="500px" align="right">
</p>

## Referente a versiones y ramas

Al utilizar el comando "git init" creamos una rama master o **principal(main)**, además, también se crea una **cabeza(head)** que indica la posición más actual de tu proyecto.
Se pueden crear copias exactas de la rama main y sus versiones anteriores, a esto le denomina **rama(branch)**, en estas se pueden crear modificaciones que no afecten a la rama main, además también se pueden usar como pruebas, se pueden crear tantas ramas como quieras.


Para crear una rama ejecutamos el comando:
~~~
git branch [nombre de la rama]
~~~
Esta rama se copiara de la rama en la que estamos actualmente.

Para visualizar las ramas y ver en cual estamos usamos:
~~~
git branch
~~~

Para cambiar de rama utilizamos:
~~~
git checkout [nombre de la rama]~~~
