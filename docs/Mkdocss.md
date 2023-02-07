# MkDocs: guia de primeros pasos
#### Introducción
Mkdocs es un software generador de sitios estáticos orientado a la creación de plataformas de documentación. Está escrito en python y se basa en escribir los archivos del servidor de documentos en formato Markdown.

#### Instalación 
Ya que MkDocs es un programa desarrollado en Python antes de poder instalarlo se debe asegurar de que _Python_ y el administrador de paquetes del mismo _pip _ estén instalados. 
Se puede verificar esto utilizando los comandos:  
```
python --version  
pip --version
```
![](/Imagenes/img1.jpg)

~~~
Nota: MkDocs es compatible con las versiones 3.5, 3.6, 3.7, 3.8 y pypy 3 de Python 
~~~

Una vez que tenemos python y el instalador de paquetes de software pip, para instalar MkDocs tenemos que ejecutamos el comando:
```
pip install mkdocs
```
![](/Imagenes/img2.jpg)

Para ver la versión y corroborar que se haya instalado correctamente corremos el comando: 
```
mkdocs --version
```
![](/Imagenes/img3.jpg)

#### Crear un Proyecto
Una vez instalado MkDocs iniciamos un proyecto desde el terminal de comandos ejecutando:
```
mkdocs new nombredelproyecto
cd nombredelproyecto
```
![](/Imagenes/img4.jpg)

También podemos revisar en la ubicación que creamos el proyecto que se haya creado correctamente. En el mismo hay un solo archivo de texto con la configuración del proyecto  llamado *mkdocs.yml* y una carpeta nombrada docs que contendrá sus archivos fuente de documentación. En esta carpeta habrá una página de documentación llamada *Index.md*, que actúa como página principal, y esta carpeta está destinada a ubicar los archivos *markdown*.  
![](/Imagenes/img5.jpg)

Para obtener una vista previa de la documentación Mkdocs nos permite utilizar un dev-server que ya tiene incorporado. Para utilizarlo debemos asegurarnos estar parados en el mismo directorio que *mkdocs.yml* para luego iniciar el servidor ejecutando:  
```
mkdocs serve
```
![](/Imagenes/img6.jpg)

Ahora si abrimos http://127.0.0.1:8000/ en nuestro navegador vamos a ver que se muestra la página de inicio predeterminada.
![](/Imagenes/img7.jpg)


#### Elegir un tema en MkDocs
Dentro del archivo de configuracion que brinda MkDocs podemos cambiar variables como el nombre de busqueda, la topologia del documento, el tema, los colores, entre otras cosas. En este caso el thema utilizado es *Material* de MkDocs.
##### Instalación
 Para instalar un nuevo tema se puede realizar mediante *pip*, com *docker* o a traves de *Git*.  

- Con pip  
```
pip install mkdocs-material
```
- Con docker
```
docker pull squidfunk/mkdocs-material
```
- Con Git
```
git clone https://github.com/squidfunk/mkdocs-material.git
```
El tema residirá en la carpeta mkdocs-material/material. Al clonar desde git, debe instalar todas las dependencias necesarias usted mismo:
```
pip install -r mkdocs-material/requirements.txt
```
Una vez instalado se debe cambiar el nombre del tema en el archivo de configuracion *mkdocs.yml*  
`theme:`    
    `name: material`  
![](/Imagenes/img8.jpg)  
Para obtener mas informacion sobre otros themas se puede cnsultar a [https://www.mkdocs.org/user-guide/custom-themes/](https://www.mkdocs.org/user-guide/custom-themes/).