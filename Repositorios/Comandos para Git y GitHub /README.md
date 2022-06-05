# **COMANDOS PARA GIT Y GITHUB**

En este archivo se mostraran los principales comandos necesarios para la creación
de repositorios locales en Git y remotos desde GitHub desde la terminal de Ubuntu, así como su modificación y actualización.


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
Cuando modificamos un archivo y lo guardamos