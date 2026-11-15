# Script - Lección 4: Introducción a CSS y Estilos Básicos

¡Hola a todos! Sean bienvenidos a la lección 4. En el video anterior construimos la página de presentación de Ana con títulos, párrafos, listas, imágenes, enlaces y una tabla. Funciona muy bien, pero se ve bastante simple: todo es negro sobre blanco. Hoy vamos a darle color y estilo con CSS. Recuerden la idea de la casa: HTML es el esqueleto con paredes y habitaciones, y CSS es la decoración, es decir, los colores, las formas y los espacios. Igual que antes, no vamos a instalar nada: todo lo haremos en CodePen, desde el navegador.

## Antes de empezar: el panel CSS de CodePen
Abran el archivo inicial de esta lección. Copien lo que está dentro de `<body>` en el panel HTML de CodePen y lo que está dentro de `<style>` en el panel CSS. Verán que la página de Ana aparece abajo, igual que al final de la lección anterior. El panel CSS es donde escribiremos hoy. Todo lo que pongamos ahí cambiará cómo se ve la página, sin tocar su contenido.

## TODO 1: Mi primera regla
CSS funciona con reglas. Una regla tiene tres partes. Primero el **selector**, que dice a quién le aplicamos el estilo; por ejemplo `h1`, el título principal. Luego, entre llaves, la **propiedad**, que dice qué queremos cambiar, como `color`. Y por último el **valor**, que dice cómo lo cambiamos, por ejemplo `tomato`, que es un tono de rojo. La propiedad y el valor se separan con dos puntos, y al final siempre va un punto y coma:

    h1 {
      color: tomato;
    }

Miren el resultado: el título de Ana ahora es rojo. Y fíjense que no tocamos el HTML. CSS puede usar nombres de colores en inglés como `tomato`, `blue`, `gold` o `lightgreen`. Prueben otros.

## TODO 2 y 3: Centrar, poner borde y dar espacio
Una regla puede tener varias propiedades, una debajo de otra, cada una con su punto y coma. Con `text-align: center` centramos el texto. Con `border` dibujamos un borde, y le damos tres datos: el grosor (`3px`, tres píxeles), el estilo (`solid`, una línea continua) y el color (`black`). Como el borde queda muy pegado al texto, agregamos `padding`, que es el espacio interno entre el contenido y el borde:

    h1 {
      color: tomato;
      text-align: center;
      border: 3px solid black;
      padding: 10px;
    }

## Práctica 1
Pausen el video. Cambien el color del título, céntrenlo y prueben un borde. Pueden cambiar el grosor, el color o probar `dashed` en lugar de `solid` para un borde con rayitas. Cuando terminen, continuamos.

## TODO 4 y 5: Estilos para toda la página
Si queremos cambiar toda la página, usamos el selector `body`, que es la etiqueta que envuelve todo lo que se ve. Con `background-color` cambiamos el color de fondo, y con `font-family` el tipo de letra. Escribimos dos fuentes separadas por coma: si la primera no está disponible, el navegador usa la segunda. `sans-serif` significa "una letra sin adornos", y está en todos los navegadores:

    body {
      background-color: lightyellow;
      font-family: Arial, sans-serif;
    }

¿Notaron que el texto de todos los párrafos y listas cambió de letra? Eso pasa porque los elementos que están dentro de `body` heredan su fuente. Por eso decimos que los estilos caen "en cascada", y de ahí viene la C de CSS: *Cascading Style Sheets*, hojas de estilo en cascada.

## TODO 6: Color de los subtítulos
El selector `h2` afecta a **todos** los `h2` de la página a la vez. Con una sola regla pintamos "Sobre mí", "Mis hobbies" y "Mis 3 metas":

    h2 {
      color: darkslateblue;
    }

## Práctica 2
Pausen el video y elijan su propia combinación de colores para el fondo y los subtítulos. Un consejo: usen un fondo claro con letras oscuras, o al revés, para que el texto se lea bien.

## TODO 7: Marco para las imágenes
Con el selector `img` le damos estilo a todas las imágenes. Les ponemos un borde de color, y con `border-radius` redondeamos las esquinas. Mientras más grande el número, más redondas quedan:

    img {
      border: 4px solid tomato;
      border-radius: 10px;
    }

## TODO 8 y 9: Una tabla más ordenada
En la lección anterior dibujamos el borde de la tabla con el atributo `border="1"` y dijimos que lo haríamos mejor con CSS. Ahora es el momento. Podemos aplicar la misma regla a varios elementos a la vez si los separamos con comas. Así le damos borde y espacio a todas las celdas, `th` y `td`, de una sola vez. Luego, solo a los encabezados `th` les ponemos fondo rojo y letras blancas:

    th, td {
      border: 1px solid gray;
      padding: 8px;
    }

    th {
      background-color: tomato;
      color: white;
    }

## Práctica 3
Pausen el video. Denle un marco a sus imágenes y estilo a su tabla. Prueben distintos valores de `border-radius`, por ejemplo `50%`: ¿qué le pasa a la imagen?

## TODO 10 y 11: Clases, para dar estilo solo a algunos elementos
Hasta ahora cada regla cambiaba **todos** los elementos de un tipo. Pero, ¿y si solo queremos resaltar un párrafo y no todos? Para eso existen las **clases**. Primero, en el HTML, le ponemos un nombre al elemento con el atributo `class`. Vamos a ponérselo al primer párrafo y a la cita:

    <p class="destacado">Tengo <strong>14 años</strong> y me encanta la <em>tecnología</em>...</p>

    <blockquote class="destacado">Cada gran proyecto empieza con una primera línea de código.</blockquote>

Luego, en el CSS, escribimos el nombre de la clase con un **punto** adelante. Ese punto le dice al navegador "busca los elementos que tengan esta clase":

    .destacado {
      background-color: white;
      border-left: 5px solid tomato;
      padding: 10px;
    }

Con `border-left` dibujamos el borde solo en el lado izquierdo, como una marca de resaltador. Ahora solo esos dos elementos se ven destacados; los demás párrafos siguen igual.

## Práctica 4
Pausen el video y creen su propia clase. Pónganle el nombre que quieran, por ejemplo `.importante`, úsenla en uno o dos elementos y denle un color de fondo distinto.

## Errores comunes
Si algo no cambia, revisen estas tres cosas:
- **Falta el punto y coma** al final de una propiedad: esa línea y la siguiente dejan de funcionar.
- **Falta una llave** `{` o `}`: esa regla, y a veces las que vienen después, dejan de funcionar.
- **Un nombre mal escrito**: `colr` en vez de `color`, o una clase que en el HTML se llama `destacado` y en el CSS `.destacada`. Los nombres deben ser exactamente iguales.

## Reto de la Lección
Repasemos lo aprendido: una regla CSS tiene **selector**, **propiedad** y **valor**; usamos `color`, `background-color` y `font-family` para colores y letras; `text-align` para centrar; `border`, `border-radius` y `padding` para bordes y espacios; selectores de etiqueta como `h1` o `body`, varios selectores separados por coma, y clases con un punto adelante. Les dejamos como reto cambiar los colores de la página de Ana por los de su equipo o anime favorito, y crear una clase nueva para resaltar su meta más importante. En la siguiente lección juntaremos todo lo aprendido para crear su propia página de perfil. ¡Nos vemos en el Módulo 5!