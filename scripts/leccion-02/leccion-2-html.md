# Lección 2: La estructura básica de HTML

## ¿Qué es exactamente un archivo HTML?

Para empezar, un documento HTML no es más que un archivo de texto plano al que se le incorporan instrucciones específicas. Estas directrices permiten que cualquier navegador web interprete la información y la transforme en una interfaz visual atractiva para los usuarios.

Cada vez que navegas por internet, tu navegador descarga uno o múltiples archivos de este tipo para procesarlos y renderizar en tu pantalla los textos, botones e imágenes que estás consultando.

## Conceptos Fundamentales: Etiqueta, Elemento y Atributo

Antes de sumergirnos en el código, es vital dominar la terminología básica que da vida a este lenguaje:

* **Etiqueta:** Consiste en una palabra clave encerrada entre los símbolos de menor y mayor que (`< >`). En la gran mayoría de las ocasiones, trabajan en parejas (una de apertura y una de cierre).
* **Elemento:** Es el bloque completo que resulta de combinar la etiqueta inicial, el contenido que se encuentra en su interior y la etiqueta final.
* **Atributo:** Se trata de un parámetro o dato adicional que se ubica dentro de la etiqueta de apertura para modificar su comportamiento o aportar información extra, tales como `src` o `href`.

## El esqueleto fundamental de HTML

Todo archivo HTML que aspire a ser correcto debe seguir un patrón o estructura estándar.

Este diseño troncal se sustenta principalmente en tres componentes esenciales:

* `html`
* `head`
* `body`

## El contenedor raíz: html

```
<html>

</html>
```

La etiqueta `html` representa el contenedor supremo de todo el archivo.

Ningún contenido de la página debe quedar fuera de este par de etiquetas. Funciona como el envoltorio general que delimita el inicio y el fin del código HTML.

## La sección de metadatos: head

```
<head>

</head>
```

Por su parte, el bloque `head` opera como el centro de control o configuración del sitio.

Los datos aquí consignados no se proyectan de forma directa en la interfaz visible, pero cumplen un rol crítico. Es aquí donde se inserta el título del documento mediante la etiqueta `title`.

### Especificando el título: title

```
<title>Mi Primera Página</title>
```

Lo que escribas dentro de este elemento será exactamente lo que se visualice en la pestaña superior de tu navegador web.

## La zona visual: body

```
<body>

</body>
```

En contraposición al `head`, la etiqueta `body` albergue absolutamente todo aquello que el visitante sí podrá ver e interactuar en pantalla.

Dentro de este espacio se despliegan:

* Encabezados y títulos llamativos
* Párrafos descriptivos
* Recursos multimedia e imágenes
* Enlaces con atributos interactivos

## La declaración inicial: DOCTYPE

```
<!DOCTYPE html>
```

Esta instrucción obligatoria debe colocarse siempre en la mismísima primera línea de tu documento.

Su función es notificarle al navegador que la página está desarrollada empleando los estándares modernos de HTML5.

## Estructura global unificada

```
<!DOCTYPE html>
<html>
<head>
    <title>Mi Primera Página</title>
</head>
<body>

    <h1>¡Hola, Mundo!</h1>
    <p>Esta es mi primera página web.</p>

</body>
</html>
```

Desglosando el bloque anterior:

* `<!DOCTYPE html>` define la versión del documento.
* `<html>` engloba la totalidad del proyecto.
* `<head>` resguarda la configuración técnica y el título.
* `<body>` concentra la experiencia visual del usuario.

## Jerarquía de encabezados

HTML pone a nuestra disposición seis escalas distintas de títulos para estructurar la información jerárquicamente:

```
<h1>Título principal</h1>
<h2>Subtítulo</h2>
<h3>Sección de tercer nivel</h3>
```

El elemento `h1` posee la máxima jerarquía y tamaño visual, mientras que el `h6` se reserva para los detalles más específicos.

## Bloques de texto y el uso de atributos

```
<p>Este es un párrafo redactado con un <a href="https://codepen.io" target="_blank">enlace externo</a>.</p>
```

Mientras que la etiqueta `p` delimita un bloque textual, la inclusión de atributos como `href` o `target` dota de interactividad y dinamismo al elemento.

## Práctica recomendada en CodePen

Copia este bloque de código y pruébalo directamente en tu entorno de trabajo:

```
<!DOCTYPE html>
<html>
<head>
    <title>Mi Primera Página Web</title>
</head>
<body>

    <h1>¡Hola, Mundo!</h1>
    <p>Este es mi debut con HTML, estructurando contenido desde cero.</p>

    <h2>¿Qué hemos practicado hoy?</h2>
    <p>Comprendimos que la arquitectura web se compone de <strong>etiquetas</strong>, <strong>elementos</strong> y <strong>atributos</strong>.</p>
    
    <p>Puedes visitar <a href="https://codepen.io" target="_blank">CodePen</a> para seguir practicando.</p>

</body>
</html>
```

## Vista previa del resultado

Al ejecutar el código anterior, obtendrás:

* Un encabezado principal destacado con la frase "¡Hola, Mundo!".
* Un bloque de texto explicativo inmediato.
* Un subtítulo seccional secundario.
* Párrafos enriquecidos con enlaces interactivos mediante atributos.

## Reglas de oro: Apertura y Cierre

Casi la totalidad de las etiquetas en este lenguaje operan en pareja:

```
<h1>Este es el contenido</h1>
```

* La etiqueta que abre se escribe como `<h1>`.
* La etiqueta que cierra lleva obligatoriamente una barra inclinada: `</h1>`.

Jamás olvides cerrar las etiquetas que decidas abrir para prevenir fallos de renderizado.

## Buenas prácticas de desarrollo

* Anteponer siempre la línea `<!DOCTYPE html>` al iniciar.
* Mantener una correcta indentación (tabulaciones) para facilitar la lectura del código.
* Asegurar el cierre oportuno de cada etiqueta iniciada.
* Definir siempre un título claro dentro del elemento `title`.

## Conclusión

Dominar la arquitectura fundamental compuesta por `html`, `head` y `body`, sumada al manejo preciso de etiquetas, elementos y atributos, constituye el cimiento indispensable de todo desarrollador web.

Una vez afiances estos fundamentos, estarás listo para incorporar estilos visuales, hojas de diseño y interfaces mucho más complejas. ¡Nos vemos en la siguiente lección!