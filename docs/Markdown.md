# Markdown

## ¿Qué es markdown?

Markdown nace como una herramienta para pasar de texto plano a HTML, creada en 2004 por John Gruber.

Puede definirse como un método de escritura, si bien suele ser considerado un lenguaje, que permite añadir formato, como negrita, cursiva, enlaces, viñetas, enlaces, entre otros; en forma de texto plano, lo que desemboca en una escritura simple y eficiente.

Es muy usado en internet, con HTML, pero también se puede encontrar en libros digitales, móviles, Amazon, Google Play, etc.

## Sintáxis de Markdown

A continuación, se mostrará la sintaxis de los elementos más básicos de Markdown, que permitirán el inicio en el mundo de este lenguaje. Para la comprobación de las diferentes pruebas que se van haciendo existen distintos recursos, accesorios de google docs por ejemplo que traduce Markdown al texto que resultaría de este, o páginas que nos muestran en tiempo real el resultado de lo redactado ([Dillinger](https://dillinger.io/)).

*  Encabezado: para lograr un encabezado, solamente basta con colocar “#” previo al texto, y éste tomará el formato de encabezado. La utilización de más numerales indica que se tienen varios encabezados de distinto orden. Por ejemplo, en Dillinger pruebe con:

\# Encabezado 1

# Encabezado 1

\## Encabezado 2

## Encabezado 2

\### Encabezado 3

### Encabezado 3    

*   Párrafos: para separar en párrafos, simplemente basta con dejar una línea en blanco entre estos, es decir, hacer un doble Enter.

* Listas: para generar listas es super sencillo, solo basta con colocar un “-”, “*” o “+” adelante de las palabras de las listas, y se formará. Con esta sintaxis se forman listas desordenadas.
En Dillinger pruebe con:

- Elemento de lista 1

- Elemento de lista 2

* Elemento de lista 3

* Elemento de lista 4

+ Elemento de lista 5

+ Elemento de lista 6

En caso de querer las listas ordenadas, solo basta con poner 4 espacios antes del “-”, “*” o “+”, por ejemplo:

- Elemento de lista 1

- Elemento de lista 2

    * Elemento de lista 3

    * Elemento de lista 4

        + Elemento de lista 5

        + Elemento de lista 6

* Listas ordenadas: solo se necesita poner un número seguido de un punto, delante de la lista:

1. Elemento de lista 1

2. Elemento de lista 2

    * Elemento de lista 3

    * Elemento de lista 4

        1. Elemento de lista 5

        2. Elemento de lista 6

* Formato de texto: para dar formato **negrita** o _cursiva_ al texto, es de la siguiente manera:

\*curisva*

\_cursiva_

\*\*negrita**

\_\_negrita__

\*\*\*negrita y cursiva***

\_\_\_negrita y cursiva___

* Enlaces: para ser más ordenado y que sea más legible es conveniente tener un nombre asociado a ese link, para que se escriba todo el texto y luego se defina el enlace de referencia:

 En [Dillinger][blog] permite ver lo que vamos escribiendo en Markdown.

[blog]: https://dillinger.io

* Código: para escribir código en Markdown, se debe encerrar lo correspondiente al código en “ ` “, que se corresponde con la etiqueta HTML &lt;code>. Por ejemplo:

`Ésto es código`

Si se hacen 4 espacios al principio de la línea se predetermina el formato HTML.

*  Imágenes: es similar a los links:

![Texto alternativo](ruta/a/imagen.jpg “Texto al dejar el cursor sobre la imagen”)



*  Omitir markdown: en caso de que alguno de los caracteres usados en sintáxis anteriores quiera ser usado, es necesario poner la barra invertida delante de éstos, para que queden plasmados en el texto.

\*
\-
\+
\<
\[



* Para seguir aprendiendo más del lenguaje, internet está lleno de diferentes páginas con más recursos, aquí se ha limitado a explicar los básicos. 

### Aplicaciones Markdown

La principal aplicación en Markdown que trataremos, será mediante mkdocs. Para conocer más de esta herramienta, diríjase al apartado de este tema.