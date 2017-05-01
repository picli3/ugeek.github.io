---
layout: page
title: "Configurar tu PC para subir contenido a tus repositorios GitHub mediante la terminal"
date: 2017-05-01
tags: [blog, github, terminal, ssh, key]
categories: github
---
#### Publicado por Angel

En el Post de hoy voy a explicar como configurar nuestro PC para poder subir a nuestros repositorios en GitHub, todo aquello que hagamos en local mediante la terminal.  

### Generando tu clave pública SSH
Para comenzar, primero borraremos las posibles ssh creadas, para ello entramos en `~/.ssh` y eliminaremos los ficheros *_rsa y *.pub que haya.

Cuando lo hagas ejecuta el comando:
{% highlight ruby %}
ssh-keygen
{% endhighlight %}


Saldrán una serie de preguntas. puedes ir pulsando intro para que se respondan con valores por defecto. eso no influye.  

Cuando termine, aparecerán un par de ficheros dentro de ~/.ssh/  

Seguramente se llamarán id_rsa y id_rsa.pub o adquirán el nombre que has elegido si has puesto alguno en el paso anterior.

Ahora abre el fichero acabado en .pub con algún editor de textos que te permita copiar el contenido, copia el contenido y ves github.com  

### Ahora vamos a github.com

Haz click en tu foto de perfil de arriba a la derecha, después ve a settings > SSH and GPG keys > New SSH key. Pégalo y finalizar


A partir de ahora ya tienes permisos para subir cambios a tus repositorios en local.

### Clonemos nuestro repositorio para trabajar en local.

Siguiente paso. Ves al repositorio de tu blog en github,haz click en Clone or download en la zona de la derecha, te saldrá  *Clone with HTTPS o Clone with SSH*
![github](/img/post/github_key.png)

Si te sale lo primero, haz click sobre Use SSH y después haz click sobre el botón de copiar que hay debajo (o copia la url que te aparece debajo), si te sale lo segundo, haz click sobre el botón copiar de abajo directamente para copiar la url

Tags: {% assign sorted_tags = page.tags | sort %} {% for tag in sorted_tags %} , <span class="tag"><a href="/tag#{{ tag }}">{{ tag }}</a></span> {% endfor %},