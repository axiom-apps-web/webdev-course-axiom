# Script - Lección 3: Elementos HTML Fundamentales

¡Hola a todos! Sean bienvenidos a la leccion 3. En los videos anteriores aprendimos qué es un sitio web y cómo se estructura un archivo HTML. Hoy vamos a conocer las etiquetas que más usarán para construir cualquier página: títulos, párrafos, listas, imágenes y enlaces. Al final del video habremos creado una página de presentación completa, sin instalar nada, usando únicamente CodePen en el navegador.

## TODO 1 y 2: Título principal y párrafo
Empecemos por el título principal. Se escribe con la etiqueta `h1` y es el título más importante de la página, por eso solo se usa uno. Una etiqueta se abre con `<h1>` y se cierra con `</h1>`, con una barra; todo el conjunto se llama elemento. Debajo escribimos un párrafo con la etiqueta `p`. Dentro del párrafo resaltamos palabras: `strong` las pone en negrita, para lo importante, y `em` en cursiva, para dar énfasis. Fíjense que un elemento puede ir dentro de otro; a eso le llamamos anidar:

    <h1>Hola, soy Ana</h1>

    <p>Tengo <strong>14 años</strong> y me encanta la <em>tecnología</em>. Estoy aprendiendo a crear páginas web.</p>

## TODO 3, 4 y 5: Línea separadora, subtítulos y salto de línea
Para separar secciones usamos `hr`, que dibuja una línea horizontal. Luego escribimos un subtítulo con `h2` y un sub-subtítulo con `h3`. Los títulos tienen niveles, como el índice de un libro: `h1` es el más importante, luego `h2`, `h3` y así hasta `h6`. Usamos cada nivel por su importancia, no por su tamaño. Por último, con `br` hacemos un salto de línea dentro del mismo párrafo, sin crear uno nuevo. Las etiquetas `hr` y `br` son especiales porque no tienen contenido, así que no necesitan etiqueta de cierre:

    <hr>

    <h2>Sobre mí</h2>
    <h3>Mi día favorito</h3>

    <p>Los sábados juego fútbol por la mañana<br>y por la tarde dibujo en casa.</p>

## Práctica 1
Pausen el video y completen los TODO del 1 al 5 con su propia información. Cuando terminen, continuamos con las listas.

## TODO 6 y 7: Lista con viñetas y lista anidada
Las listas sirven para agrupar ideas. La lista con viñetas se escribe con `ul`, que significa lista sin orden, y cada punto va dentro de un `li`, de list item. Si queremos más detalles, podemos poner otra lista dentro de un `li`; esto se llama lista anidada. En nuestro ejemplo, dentro de "Videojuegos" ponemos dos juegos favoritos. Fíjense bien en dónde se cierra cada etiqueta: la lista interna va antes del cierre `</li>`:

    <h2>Mis hobbies</h2>
    <ul>
        <li>Dibujar</li>
        <li>Jugar fútbol</li>
        <li>Videojuegos
            <ul>
                <li>Minecraft</li>
                <li>Rocket League</li>
            </ul>
        </li>
    </ul>

## TODO 8: Lista numerada
Si el orden importa, como en una lista de metas, usamos `ol`, de ordered list. Los números aparecen solos, no hay que escribirlos. Usamos `ul` cuando el orden no importa y `ol` cuando sí, como en pasos o rankings:

    <h2>Mis 3 metas</h2>
    <ol>
        <li>Crear mi primera página web</li>
        <li>Aprender CSS</li>
        <li>Compartir mi trabajo con mis amigos</li>
    </ol>

## Práctica 2
Pausen el video y creen sus listas de hobbies y metas. Intenten anidar una lista dentro de otra.

## TODO 9: Imágenes
Una página sin imágenes es aburrida. Para agregar una usamos la etiqueta `img`, que necesita atributos: datos extra que escribimos dentro de la etiqueta con la forma `nombre="valor"`. El atributo `src` indica dónde está la imagen, `alt` es una descripción en texto que ayuda a las personas con discapacidad visual y aparece si la imagen no carga, y `width` define el ancho en píxeles. Igual que `br` y `hr`, la etiqueta `img` no lleva cierre:

    <img src="https://picsum.photos/300/200" alt="Paisaje de ejemplo" width="300">

## TODO 10: Enlaces
Lo que hace especial a la web son los enlaces. Se crean con la etiqueta `a`, de anchor, que significa ancla, y el texto que va entre las etiquetas es el que se puede pulsar. El atributo `href` indica a dónde lleva el enlace, y `target="_blank"` hace que se abra en una pestaña nueva. Usen textos claros: "Visita Wikipedia" es mejor que "haz clic aquí":

    <p>Mi sitio favorito: <a href="https://www.wikipedia.org" target="_blank">Visita Wikipedia</a></p>

## TODO 11: Una imagen que también es enlace
Un elemento puede ir dentro de otro, y las imágenes no son la excepción. Si ponemos un `img` dentro de un `a`, al pulsar la imagen se abre el enlace. Es otro ejemplo de elementos anidados:

    <a href="https://www.wikipedia.org" target="_blank">
        <img src="https://picsum.photos/150/100" alt="Imagen que lleva a Wikipedia" width="150">
    </a>

## Práctica 3
Pausen el video, agreguen su imagen y un enlace a su sitio favorito. Pruébenlo para comprobar que funciona.

## TODO 12: Citas
Para destacar una frase o una cita usamos `blockquote`. El navegador la separa un poco del margen izquierdo para que se note:

    <blockquote>Cada gran proyecto empieza con una primera línea de código.</blockquote>

## TODO 13: Tablas
Las tablas organizan datos en filas y columnas, como una hoja de cálculo. La etiqueta `table` es la tabla completa, cada fila es un `tr`, de table row, las celdas de encabezado son `th`, que se ven en negrita, y las celdas normales son `td`. El atributo `border="1"` dibuja un borde para que veamos las celdas; más adelante lo haremos mejor con CSS. Cada fila debe tener el mismo número de celdas para que la tabla quede ordenada:

    <table border="1">
        <tr>
            <th>Materia</th>
            <th>Nota</th>
        </tr>
        <tr>
            <td>Matemáticas</td>
            <td>18</td>
        </tr>
        <tr>
            <td>Tecnología</td>
            <td>20</td>
        </tr>
    </table>

## Práctica 4 (opcional)
Si quieren un reto, completen la cita y la tabla. Pueden hacerlo después del video.

## Reto de la Lección
Repasemos lo aprendido: títulos con `h1` a `h6`, párrafos con `p`, negrita y cursiva con `strong` y `em`, listas con `ul`, `ol` y `li`, imágenes con `img`, enlaces con `a`, citas con `blockquote` y tablas con `table`. Les dejamos como reto cambiar nuestro ejemplo por su propia información: su nombre, sus hobbies, sus metas y sus materias favoritas, y agregar una segunda tabla o lista con su videojuego o pasatiempo favorito. En el siguiente módulo le daremos color y estilo a todo esto con CSS. ¡Nos vemos en el Módulo 4!