---
title: ¿De qué manera se estructura un post en jekyll?
layout: post
author: yourShortName
tag:
    - yourtag1
year: 2026
---

El **nombre de archivo** es el que principalmente determina tanto la fecha en que el post fue publicado como el nombre del post, por lo tanto el formato para ello se basa en el siguiente: **`año-numeroDeMes-numeroDeDia-titulo-del-post-o-nombre-del-post.md`**. Pero, en caso de necesitar titulos acentuados, o necesitar titulos sin cambiar todo el nombre del archivo, puede especificarse en la sección de variables de cada post, la variable `title: Nombre nuevo al post`. (Puedes revisar que este post tiene un titulo con caracteres especiales como **`¿`** y **`?`**, pero no son permitidos como nombre de archivo, por lo tanto se hace uso de dicha variable `title:`)

El `layout: post` corresponde al archivo de `_layouts/post.html` el cual determina la estructura de todos los posts, esto quiere decir, que en dicho archivo llace un layout (un diseño de página exclusivamente para los posts). En este caso, el `_layouts/post.html` incluye el navbar, el titulo del post, la fecha de su publicación, el autor, los tags o etiquetas de dicho post, y el contenido del post.

Por lo tanto puede modificarse moviendo el autor o las etiquetas debajo del post, ocultar la fecha de publicación, mostrar únicamente el titulo del post, o lo que se desee.

El `author:` es algo que ya se especificó en el archivo `_authors/yourShortName.md` pero en teoría corresponde al nombre simplificado de un autor en la carpeta `_authors/` y su valor deberá corresponder tanto al nombre de `_authors/archivo.md` como al short_name (Ej. Un autor llamado Pepito -> `_authors/pepito.md` -> Completar los datos necesarios del archivo `pepito.md` como short_name (nombre de archivo sin el .md), name, y position -> Luego en la creación de un post determinarle `author: pepito`)

Los `tag:` corresponde a las etiquetas (tags) en las cuales el post se clasificará, es decir, si es un post de cocina pues la etiqueta o tag podría ser `cocina` o `recetas`. Estas etiquetas estarán alojadas y podrán ser creadas en la carpeta `_tags/` y al igual que los autores: tendrán un short_name que hará más sencillo el invocarlas bajo su nombre simplificado (y al igual el short_name de las etiquetas debe corresponder al nombre del archivo sin la extensión .md), y tendrán un name que será el nombre completo de dicha etiqueta o un nombre acentuado si se da el caso. (Ej. Un tag establecido como `recetas` debe tener su respectivo archivo `_tags/recetas.md` -> En dicho archivo `recetas.md` se debe establecer su short_name (osea, el nombre del archivo sin la extensión .md (osea, `short_name: recetas`)), se debe establecer su name que correponde al nombre a mostrar en el post (osea `Recetas`, en donde la etiqueta comienza en mayuscula).

El `year` pues es el año de publicación del post, originalmente no estaba especificado en los templates de jekyll, pero quise adicionarlos como una colección al template, para que fuese más sencillo el poder clasificarlos por fechas, en este caso: por años. Al igual que los autores, y los tags, los year cuentan con la misma obligatoriedad de factores, por lo tanto, necesitan que su determinado archivo este creado en `_years/2026.md` y dentro de dicho archivo sus valores de short_name y name.

💡 Para tener un preview rapido de como se vería el sitio, ingresa en la terminal `bundle exec jekyll serve` para desplegar el servidor local, abre el server address en tu navegador web (Ejemplo: http://127.0.0......)
