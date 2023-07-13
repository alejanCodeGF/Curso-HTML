# Curso de HTML basico

## Descripción

Este proyecto contiene materiales y ejercicios prácticos de HTML.

He aprendido los fundamentos del lenguaje y he adquirido las habilidades para crear y estructurar contenido web, y te lo resumo aquí.

Si lo veo necesario, lo iré editando a futuro para que esté lo más completo posible.

¡Espero que te sirva!

## Autor

**AlejanCodeGF**

- [Linkedin](https://www.linkedin.com/in/alejan-gomez-fernandez/)
- [Porfolio web]()

## Datos de contacto

**alejan.gomez.fernandez@gmail.com**

---

`>` No sé si hace falta decirlo, pero obviamente lo que esté en el HTML, CSS y JS será público, así que no poner cosas privadas, vaya (ni en comentarios).

## Links interesantes

[**{Link a un cheatsheet interactivo}**](https://htmlcheatsheet.com/)

## Comentar en el código

```
<!--COMENTARIO-->
```

## Teoría antes de empezar

```
Al archivo que quieras que arranque la web, le pones el nombre de "index.html"
    > Es el que mostrará la web primero

Estructura:
[<etiqueta atributo="valor">contenido</etiqueta>]
    > Habrá algunos que no necesiten etiqueta de cierre, para esos
    [<etiqueta atributo="valor" />]

> Algunos dirán que no le pongas el "/", para que quede más limpio
> Yo lo he hecho teniendo en cuenta el cierre, lo que veas

Display:
block -> Completan la línea hasta el final del contenedor (h1, h2... p, etc.)
    > Por más pequeño que sea el texto, no se puede poner nada más a la derecha.
inline -> Ocupan el contenido únicamente (inputs, etc.)

Links:
1. Rutas locales (las que están en nuestra carpeta)
    > "nombre_archivo.html" / "nombre_carpeta/nombre_archivo.html"
    > ../archivo -> ir a una carpeta anterior (si quieres 2 ../../etc)
2. Rutas externas (las de fuera de nuestra carpeta)
    > "https/www...."

> Bool (booleano) significa que no hace falta introducir ningún dato para activarlo
    > Se suele poner por nomenclatura de nombre el mismo atributo
        > (P.e: <ol reversed = "reversed">, o <video controls = "controls">)

> Algunos dirán que lo pongas vacío (<ol reversed>), que se ve más limpio
```

## Especificar version del HTML

```
HTML5 -> <!DOCTYPE HTML>
HTML4 -> <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
XHTML1 ->
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

`>` A partir de ahora, todo el código irá rodeado de `<html></html>`

```
<html>
    <head>
        ...
    </head>
    <body>
        ...
    </body>
</html>
```

`>` Lo que esté tabulado (sin ">"), será un atributo de la etiqueta que tenga encima

## `<head>`

`>` Aquí van los elementos que no se ven directamente en la web

```
<title> -> Añadir título en la pestaña
<meta> -> Añadir metadatos
<link> -> Linkear algo (archivo css, icono, etc.)
```

### _Metadatos / link_

```
Metadatos -> Información, que describe datos (recursos)
<meta>
    charset -> Cambiar la codificación (poder poner tildes y eso)
        = "utf-8" -> El mas usado para los idiomas europeos
    name -> Crear una "carpeta" de datos (con "content" lo rellenas)
        ="keywords" -> Etiquetas para el SEO, separadas por comas
        ="description" -> Descripción de la pagina web (entre 70-140 char)
        ="autor" -> Nombre del autor de la web
        ="copyright" -> Poner el nombre de la empresa dueña de los derechos
            > (P.e: Facebook (meta) tiene instagram)
        ="robots" -> Hablar con el buscador
            > Si la web debería ser indexada o no (que aparezca en el buscador)
                > content = "index" / "noindex"
            > Si debería dar importancia en el SEO
            (Le dicen al buscador si debe explorar las páginas a las que llevan o no)
                > content = "follow" / "nofollow"
    content -> De ese name, poner los datos
        > (P.e: name="keywords" content="harina, pasteles, huevos, lacteos")

<link>
    rel -> Qué es lo que linkamos
        ="icon" -> Icono de la pestaña
            > Importante que tenga formato .ico
        ="stylesheet" -> Archivo de estilo (css)
    type -> Qué formato tiene
        ="image/png"
        ="text/css"
    href -> Link donde esté ese archivo
```

```
Ejemplos:
<meta name="description" content="Este es un ejemplo de metadato en HTML">
<meta name="keywords" content="HTML, metadato, ejemplo">

<link rel="icon" type="image/png" href="Logo_web.ico">
<link rel="stylesheet" type="text/css" href="style.css">
```

## `<body>`

`>` Todos los elementos que se ven

### _Textos_

```
<hi> -> Añadir títulos (y solo títulos)
    > i = 1,2,...,6 (1 título, 2 subtítulo, 3 subsubtítulo...)
    > Añadir un unico h1 (por el SEO)
<p> -> Párrafo de texto
<hr /> -> Línea de separación
<br /> -> Salto de línea
<span> -> Aplicar estilos a un grupo de letras (CSS)
<a> -> Poner links a webs
    href = "https://...", o puede ser de la misma web
        > Para mandar a una parte de la misma web:
            > Poner al elemento que queramos ir un "id"
            > href="#nombre_id"
    target = "_blank" -> abrirá el link en otra pestaña
```

### _Multimedia_

```
<img /> -> Poner una imagen
    > png, jpg o gif lo aceptan todos los navegadores
    src = "link" o "imagen" (si está en la misma carpeta "imagen.png")
    width = ... |
    height = ...|
        > Si pones uno de los 2, se escala automáticamente
    alt -> Texto alternativo si no carga la imagen / contenido
        > VITAL para el SEO
    title -> Texto que sale cuando pasas el ratón por encima de la imagen
<video /> -> Poner un vídeo
    src = "link" o "vídeo"
        > Debe ser formato vídeo
    controls (bool)
        > Nos permite acceder a los controles del vídeo
        > Lo define el navegador
        > Si no esta no hacemos nada vaya
<audio /> -> Poner un audio
    > Lo mismo que el vídeo vaya
    > En formato vídeo reproduce el audio
```

### _Formularios_

```
<form> -> Rodeando el formulario de la info que quieras enviar
    action = "/formulario.php" (Donde se enviará el formulario)
    method -> Enviar la info del formulario
        = "GET" -> Parámetros en la URL
            > Hay tope de información, se suele usar para navegadores
        = "POST" -> No hay limite de información, el mas usado
        > Ningún método es seguro
<label /> -> Texto, que si haces click enfoca la atención al input
    for -> id del input asociado
    > Es un poco una tontería
    > (P.e: Pones el texto "email" al lado del input, y cuando clickes el texto (y no el input), puedes empezar a escribir)
<input /> -> Para introducir la info (texto, checkbox, etc.)
    id -> Valor unico del elemento
    name -> "key" del json al enviar el formulario
        > Muy importante para enviar los datos
        > (P.e:{"Nombre":"Alejandro", "Edad":"..."})
    value -> Valor por defecto
        > Se mantiene, no como el placeholder
    placeholder -> Texto de ayuda
        > Cuando vayas a escribir desaparece ese texto
    type
        = "text" (Por defecto) -> Introducir texto
        = "email" -> Solo permite enviar si tiene formato mail (aaa@bbb.ccc)
            > Mejor hacerlo por el backend, pueden inventarse el mail
        = "number" -> No permite escribir texto
            > Flecha arriba y abajo para sumar y restar numeros
        = "password" -> Cuando escriba salen los ***
        = "radio" -> De varias opciones poder elegir solo 1
        = "checkbox" -> De varias opciones poder elegir las que quieras
        = "range" -> Mover una flechita para selecionar un numero
            > Rollo lo de instagram, de poner un rango de si te gusta más o menos
            min (numero minimo)
            max (numero maximo)
        = "date" -> Fecha
        = "time" -> Hora
        = "color" -> Seleccionar un color
<textarea> -> Muy parecido al input text, pero un poco diferente
    id...
    ...
    cols = "número de columnas" (entiendo que char)
    row = "número de filas"
    readonly (bool) -> No se podrá borrar el texto ni escribir encima
    > No se usa "value", como el input, para hacerlo poner el texto entre las etiquetas
<button> -> Un botón, vaya
    > Se puede poner texto al botón, incluso una imagen (entre las etiquetas)
    type
        = "button" Para que el js haga cosas
        = "reset" Dejar los valores del form por defecto
        = "submit" Enviar los datos del form
```

### _Listas_

```
<ul> -> Lista no ordenada
<ol> -> Lista ordenada (1,2,3...)
    start -> Número desde donde quieres empezar la lista
        > Los siguientes lo continuarán
    type -> Tipo de ordenación
        = "A" (A,B,C,D...)
        = "a" (a,b,c,d...)
        = "I" (I,II,III,IV...)
        = "i" (i,ii,iii,iv...)
    reversed (bool) -> Enumera al revés, el último elemento será el primer numero
<li> -> Cada elemento de la lista irá rodeado de esta etiqueta

<dl> -> Lista de descripción
    > (Rollo elemento1-descripción1, elemento2-descripción2, etc.)
<dt> -> Cada elemento de la lista irá rodeado de esta etiqueta
<dd> -> Cada descripción del elemento de la lista irá rodeado de esta etiqueta

> Se pueden añadir listas dentro de listas
```

### _Tablas_

```
Las tablas se organiza por filas y elementos

<table> -> Rodeando la tabla
<tr> -> Table row, fila de la tabla
<td> -> Celdas
    > Elementos que ponemos dentro de las filas <tr>
    colspan = "num de columnas"
        > Juntar varias columnas para poner 1 elemento
    rowspan = "num de filas"
        > Juntar varias filas para poner 1 elemento
<th> -> Como td, pero para poner los apartados de la tabla (encabezado)
<caption> -> Comentario arriba de la tabla
    > (P.e: nombre de la tabla)

Para organizar la tabla usar estos 3 grupos:
<thead> -> Sección de encabezado
    > (P.e: nombre, edad... (ponerlo con <th>))
<tbody> -> Elementos de la tabla (datos)
<tfoot> -> Representar información resumen
    > (P.e: mediana, valor maximo, etc.)
```

```
> Ejemplo bastante completo en la carpeta
```

### _Organizar la web_

```
Para organizar la web lo pondremos por "grupos"
Cada grupo tiene elementos dentro, de forma organizada
    > Separar y agrupar contenido para organizar mejor

<div> -> El básico, contenedor normal genérico
<header> -> Contenedor de arriba de la web
    > Siempre se mantiene igual mientras navegas por otros enlaces de la web
<nav> -> Navegador (buscador, cuenta, logo, etc)
    > Normalmente dentro del header
<main> -> Contenido principal de la web
    > (P.e: Donde se verán las noticias, si es un periodico)
<article> -> Separar lo del main por articles
    > (P.e: Las noticias individuales)
<section> -> Separar el contenido del article
    > No se si es lo mismo que <figure>
        > Hay sitios que lo veo con esa etiqueta nose
<aside> -> Información relacionada
<footer> -> Pie de página (copyright, contactanos, links relacionados, etc.)
```

### _Enlazar JavaScript_

```
Normalmente va al final del <body>, es más visible

<script> -> Para añadir el archivo de JS
    src = "archivo.js"
```
