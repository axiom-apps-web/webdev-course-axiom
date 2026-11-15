
# Script - Lección 5: Proyecto Final y Buenas Prácticas

¡Hola a todos! Bienvenidos a la lección 5 de nuestro curso de HTML y CSS para principiantes.

En las lecciones anteriores aprendimos a construir una página web con HTML y a darle estilos utilizando CSS.

En la lección 4 trabajamos con la página de Ana, agregando colores, bordes, fuentes y otros estilos. Ahora vamos a utilizar lo aprendido para crear nuestra propia página de perfil personal.

## Parte 1: Proyecto - Tu página de perfil

Para comenzar, abrimos CodePen en https://codepen.io/pen/.

Recuerden que CodePen nos permite escribir código directamente desde el navegador, sin instalar ningún programa.

Nuestro proyecto tendrá seis elementos principales.

### TODO 1: Un título con nuestro nombre

Primero escribimos:

```html
<h1>Hola, soy Ana</h1>
```

La etiqueta `h1` permite mostrar el título principal de nuestra página.

### TODO 2: Un párrafo de presentación

Ahora agregamos:

```html
<p>Tengo 14 años y me encanta la tecnología.</p>
```

La etiqueta `p` se utiliza para escribir párrafos.

### TODO 3: Agregar una imagen

Utilizamos la etiqueta `img`:

```html
<img src="https://picsum.photos/300/200"
     alt="Paisaje de ejemplo">
```

El atributo `src` indica la dirección de la imagen y `alt` proporciona un texto alternativo.

### TODO 4: Crear una lista de hobbies

Para mostrar nuestros pasatiempos favoritos, usamos:

```html
<h2>Mis hobbies</h2>
<ul>
  <li>Escuchar música</li>
  <li>Jugar videojuegos</li>
  <li>Dibujar</li>
</ul>
```

La etiqueta `ul` crea una lista y `li` representa cada elemento.

### TODO 5: Agregar un enlace

Ahora podemos colocar un enlace a nuestra página favorita:

```html
<a href="https://www.wikipedia.org">
  Mi página favorita
</a>
```

El atributo `href` indica hacia dónde nos llevará el enlace.

### TODO 6: Personalizar nuestra página con CSS

En el panel CSS de CodePen escribimos:

```css
body {
  background-color: lightyellow;
  font-family: Arial, sans-serif;
}

h1 {
  color: tomato;
  text-align: center;
  border: 3px solid black;
  padding: 10px;
}
```

Con estas propiedades cambiamos el color del fondo, el tipo de letra, el color del título y sus bordes.

¡Y listo! Ya tenemos nuestra primera página de perfil personal.

## Práctica

Ahora les toca a ustedes.

Pausen el video y cambien el nombre de Ana por el suyo.

También pueden agregar una imagen diferente, escribir sus propios hobbies y modificar los colores.

## Parte 2: Errores comunes y consejos

Antes de terminar, vamos a conocer algunos errores que suelen aparecer cuando estamos comenzando a programar.

### Error 1: Olvidar cerrar una etiqueta

Por ejemplo:

```html
<p>Hola, soy Ana
```

En este caso olvidamos cerrar el párrafo.

La forma correcta es:

```html
<p>Hola, soy Ana</p>
```

### Error 2: Olvidar el punto y coma en CSS

En CSS debemos separar correctamente las declaraciones.

```css
h1 {
  color: tomato;
}
```

El punto y coma permite separar las propiedades de una regla.

### Error 3: La imagen no aparece

Si nuestra imagen no se visualiza, debemos revisar que la dirección escrita en el atributo `src` sea correcta.

También debemos comprobar que la imagen esté disponible.

### Error 4: Los estilos no cambian

Si modificamos el código CSS y no observamos resultados, debemos revisar que las llaves estén completas y que las propiedades estén correctamente escritas.

Por ejemplo, debemos escribir `color` y no `colr`.

## Consejos finales

Mi recomendación es probar cada cambio que realicen en su código.

Si encuentran algún error, revisen las etiquetas HTML y las propiedades CSS.

Recuerden que equivocarse también forma parte del aprendizaje.

## Cierre de la lección

¡Felicitaciones! Hemos llegado al final de nuestro minicurso.

Ahora conocen los fundamentos de HTML y CSS y pueden construir su propia página web.

Los invitamos a seguir practicando, experimentando con nuevos diseños y desarrollando su creatividad.

¡Muchas gracias por acompañarnos y sigan aprendiendo programación!

