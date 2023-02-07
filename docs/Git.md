# Git

#### ¿Qué es y para que se usa?
Git es un sistema de control de versiones, desarrollado para tener un seguimiento de archivos de código y poder compartir esos archivos entre diferentes usuarios.
Su propósito es llevar registro de los cambios en archivos de computadora incluyendo coordinar el trabajo que varias personas realizan sobre archivos compartidos en un repositorio de código.

#### ¿Con qué se utiliza?
Git es utilizado junto a diferentes plataformas de alojamiento de código como GitHub, GitLab, BitBucket, etc.
En nuestro caso vamos a utilizar GitLab.

#### Comandos


> git status

Este comando se ejecuta para saber en qué estado se encuentran actualmente los archivos, si han sido modificados, eliminados o creados.

Al ejecutar este comando, desde consola, nos muestra en que rama nos encontramos, seguido de un mensaje avisando si estamos en la última versión de esa rama. Luego, nos va nombrando los cambios que hay en nuestros archivos de forma local, comparados con los que se encuentran en la nube: si hay cambios sin cometer, si nuevos archivos fueron creados, modificados o eliminados.

> git init

Este comando se ejecuta una sola vez por lo general. Lo que hace es crear un nuevo repositorio de Git, ya sea para un proyeto existente o generar uno vacio. Se genera un subdirectorio .git, el cual contiene todos los datos del repositorio, ya sean subdirectorios de objetos, referencias, y otros archivos. Tambien se encarga de generar la configuracion de Git en la ruta del subdirectorio.

> git clone

Se utiliza para copiar o clonar repositorios existentes en nuevos directorios. Este proceso genera una conexion automatica llamada "origin" que apunta al repositorio original, lo cual facilita el proceso de interactuar con el mismo. Existen diferentes maneras de utilizar este comando, ya que podemos clonar solo una carpeta del repositorio, o con una etiqueta especifica, tambien solo la rama que deseamos y no la rama central.

> git merge <nombre_rama>

Comando utilizado para nombrar una rama en el cual se esta trabajando.

> git pull

El comando git pull se emplea para extraer y descargar contenido desde un repositorio y actualizar al instante el repositorio local para reflejar ese contenido.

> git commit -m "< mensaje >"

Confirma los cambios realizados.
El mensaje se utiliza para asociar a los cambios realizados una breve descripcion.

> git push

El comando git push se usa para cargar contenido del repositorio local a un repositorio remoto.

> git add <nombre_archivo>

Sirve para añadir un archivo o un conjunto de archivos (nombrando un directorio) al repositorio local.

> git checkout -b <nombre_rama_nueva>

Crea una rama a partir de la que te encuentres parado con el nombre “nombre_rama_nueva”, y luego salta sobre la rama nueva, por lo que quedas parado en esta última.

> git branch

Lista todas las ramas locales.

#### Metodo de trabajo

Para trabajar en el desarrollo de aplicaciones utilizaremos una estructura de trabajo basada en ramas (branch).

#### Que es una branch?

Consiste en un entorno de trabajo, que permite realizar modificaciones o cambios a los archivos sin afectar a todo el proyecto. De esta manera nos aseguraremos de que el proyecto se desarrolle lo mas ordenado posible.

A partir de esa definicion, vamos a realizar una consideracion muy importante que intenta evitar conflicots futuros y es que debemos ____evitar trabajar por separado en un mismo archivo____. Con esto nos referimos a que, dentro de un grupo de trabajo, los desarrolladores deben evitar trabajar en un mismo archivo de forma individual, ya que los cambios que realicen pueden ser distintos y cuando todo se una en la rama principal puede generar conflictos y retardar el proceso.


#### Estructura de trabajo

Como dijimos, vamos a trabajar con ramas, en un proyecto siempre hay una rama principal denominada ___master___. Esta rama es aquella en la cual no se trabaja, solo se suben las actualizaciones de los archivos cuando el desarrolllo es estable. 

Para realizar el trabajo e ir corroborando el correcto funcionamiento de las modificaciones, se realiza una segunda rama. Esta idea sigue el siguiente esquema:

![Estructura trabajo](Imagenes/git-model.png)

Como se aprecia en la imagen, la rama de trabajo esta separada de la rama master. A su vez, a partir de esta, se pueden desprender otras ramas que pueden cumplimentar con diferentes tareas propias del desarrollo de la aplicacion. Una vez finalizado el desarrollo en la rama, se realiza un merge a la rama master, de forma que, todo el contenido del proyeto se encuentre actualizado.


#### Como trabajar? 

Luego de clonar el repositorio en nuestra PC, crearemos nuestra rama de trabajo con el siguiente comando:

>git checkout -b "nombre de la rama"

De esta forma, creamos la rama y nos posicionamos sobre ella.

El paso siguiente es colocar los archivos del repositorio en nuestra rama para poder trabajar, para ello, debemos incluir los mismo con el comando 'git add'. Para facilitar el uso agregaremos todos los archivos del repositorio con:

>git add . 

A partir de este momento podemos empezar a realizar todoas las modificaciones que necesitemos. 

Una vez finalizado este proceso debemos realizar el commit de las modificaiones, de forma que queden listas para realizar el merge a la rama superior. Para ello utilizaremos:

> git commit -m "mensaje o comentario"

Con la opcion '-m' agregamos un mensaje a la modificacion, lo cual es de gran importancia realizar, ya que facilita el orden del proyecto, la busqueda y correccion de errores, etc.

Finalmente cuando tenemos las modificiaciones guardadas y comentadas, podemos realizar el push a la rama superior, pudiendo ser esta la rama master o no. Para ello utilizaremos:

> git push origin "rama en la que trabajo"

Cuando se ingresa este comando se genera un link de GitLab que nos permite enviar una solicitud de merge, en la cual podemos agregar comentarios, revisiones, entre otras cosas. Esta solicitud debe ser revisada y aceptada por el usuario correspondiente. Este usuario ademas podra decidir si la rama de la cual proviene la solicitud de merge sera eliminada o no. Por lo general, se recomienda eliminar la rama, ya que si el trabajo esta finalizado, esa rama no volvera a ser utilizada. 

#### Comandos a tener en cuenta

>git status 

Comando que nos proporcionara informacion sobre la rama en la que estamos situados, los archivos que se encuentran en ella, si hay cambios guardados o no, etc.

>git checkout

Nos permite movernos entre las ramas que tengamos creadas.

>git pull origin master

Este comando nos actualiza el repositorio que tenemos clonado, lo cual es muy recomendable para empezar a trabajr con todos los archivos actualizados.

#### Conflictos

Cuando dos personas trabajan en un mismo archivo, cada uno en su propia rama, y luego intentan realizar el merge a la rama superior, vamos a notar que esto no es posible, debido a que existe un conflicto entre ambas modificaciones dentro del archivo. Una de las formas de evitar esto es realizar un 'git pull' antes de realizar un 'git push', de manera que siempre tengamos actualizados los archivos y que si hay cambios en el archivo en el cual estamos trabajando, aparezcan de inmediato y poder realizar las correcciones correspondientes.

Si esto no se realiza a la hora de realizar la solicitud de merge en la propia pagina de GitLab, se nos notificara del conflicto y se nso brindara la posibilidad de realizar los cambios necesarios.

Como se dijo en el principio del documento es importante evitar que dos personas trabajen sobre un mismo archivo, en ramas separadas. Es importante tener buena comunicacion dentro del equipo e intentar ser lo mas ordenados posible.
