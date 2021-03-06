# **TEORÍA Y COMANDOS PARA GIT Y GITHUB**

En este archivo se añadirá teoria de Git y GitHub además se mostraran los principales comandos necesarios para la creación de repositorios locales en Git y remotos con GitHub desde la terminal de Ubuntu, así como su modificación y actualización.
***
<p> 
<img src="https://es.wizcase.com/wp-content/uploads/2022/03/GitHub-Logo.png" width="150px" align="right">
</p> 

## Git y GitHub

> Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia, la confiabilidad y compatibilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente. -Wikipedia.
 
>GitHub es una forja para alojar proyectos utilizando el sistema de control de versiones Git. Se utiliza principalmente para la creación de código fuente de programas de ordenador. El software que opera GitHub fue escrito en Ruby on Rails. Desde enero de 2010, GitHub opera bajo el nombre de GitHub, Inc. -Wikipedia.

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

Para hacer un "git add" y un "git commit" al mismo tiempo utilizamos:
~~~
git commit -am "[mensaje]"
~~~
Para utilzar este comando debes asegurarte de haber utilizado por lo menos una vez un git add en el archivo.
***
<p> 
<img src="https://git-scm.com/images/about/branches@2x.png" width="500px" align="right">
</p>

## Referente a versiones y ramas

Al utilizar el comando "git init" creamos una rama master o **principal(main)**, además, también se crea una **cabeza(head)** que indica la posición más actual de tu proyecto.
Se pueden crear copias exactas de la rama main y sus versiones anteriores, a esto le denomina **rama(branch)**, en estas se pueden crear modificaciones que no afecten a la rama main, además también se pueden usar como pruebas, se pueden crear tantas ramas como quieras.

Cuando creamos una rama esta se copiara de la rama en la que estamos actualmente. Para crear una rama ejecutamos el comando:
~~~
git branch [nombre de la rama]
~~~

Para visualizar las ramas y ver en cual estamos usamos:
~~~
git branch
~~~

Para cambiar de rama utilizamos:
~~~
git checkout [nombre de la rama]
~~~
***
### Moverse entre versiones

Para movernos entre versiones en una rama debemos tener en cuenta que solo podemos regresar a los commits, es decir, podemos regresar solo a las versiones en donde realizamos un commit, para esto necesitamos saber el código único del commit que aparece en **verde** ejecutando el comando "git log --version" o "git log":
<div align="center"><img src="https://www.unidadvirtual.com/imagen/10000000/manuales/git/git%20log/git%20log--oneline.jpg" width="700px" ></div>

Para regresar a la versión seleccionada utilizando el código del commit debemos usar el comando:
~~~
git checkout [código del commit]
~~~
Para regresar versión más actual de la rama principal ejecutamos:
~~~
git checkout [nombre de la rama principal]
~~~
<p> 
<img src="https://w7.pngwing.com/pngs/968/111/png-transparent-symbol-attention-triangle-warning-sign-words-phrases-thumbnail.png" width="100px" align="left"> 
</p>

**Si estás en una rama y haces cambios sin supervisarlos en stage o commit y después cambias de rama es probable que los cambios se puedan PERDER.**

***
### Unir ramas (merge)
Esta opción de GitHub obtiene las ultimas actualizaciones de las ramas que quieres unir, de esta forma se actualizan en la rama actual las modificaciones de la otra.
Los cambios solo se hacen si existen modififcaciones en las ramas, para obtener las modificaciones de otra rama a la rama en la que estamos utilizamos:
~~~
git merge [rama de donde se quieren obtener los cambios]
~~~

### Conflictos y como solucionarlos

Cuando unes 2 ramas y las dos tienen modificaciones diferentes en el mismo archivo en exactamente la misma linea de codigo surge un conflicto. 
Para solucionar esto solo debemos dirigirnos al archivo en donde se mostraran las 2 versiones, se debe elegir como quedará y posteriormente hacer un commit. 
 