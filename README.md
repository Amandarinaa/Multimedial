# Taller Multimedial De Grado 
## Indice: 
1. [Crear Página](#ejercicio-1-cear-p%C3%A1gina) <br>
2. [Link a Otra Página](#ejercicio-2-link-a-otra-p%C3%A1gina) <br>
3. [3 Páginas](#ejercicio--3-p%C3%A1ginas) <br>



### Ejercicio 1: Cear Página

```
<!DOCTYPE html>
<!-- Indica al navegador que este documento usa HTML5 -->

<html>
<!-- Inicio del documento HTML -->

<head>
<!-- Sección donde van metadatos, título y estilos -->

<meta charset="UTF-8">
<!-- Define la codificación de caracteres para que se vean bien tildes y símbolos -->

<title>Multimedial</title>
<!-- Título de la página que aparece en la pestaña del navegador -->

<style>
/* Aquí comienza la sección de estilos CSS que define la apariencia visual */

body{
/* "body" se refiere a todo el contenido visible de la página */

  background-color: white;
  /* Define que el fondo de toda la página sea blanco */

  color: black;
  /* Define que el color del texto sea negro */

  margin: 0;
  /* Elimina los márgenes que los navegadores agregan por defecto */

  height: 100vh;
  /* Hace que el alto del cuerpo sea igual al 100% de la altura de la pantalla */

  display: flex;
  /* Activa el sistema Flexbox para organizar y centrar elementos */

  justify-content: center;
  /* Centra el contenido horizontalmente */

  align-items: center;
  /* Centra el contenido verticalmente */

  font-family: Arial, sans-serif;
  /* Define la tipografía del texto */

  font-size: 60px;
  /* Define el tamaño grande del texto */

}
/* Fin de las reglas de estilo del body */

</style>
<!-- Fin de la sección de estilos -->

</head>
<!-- Fin de la sección head -->

<body>
<!-- Inicio del contenido visible de la página -->

Multimedial
<!-- Texto que aparece en el centro de la pantalla -->

</body>
<!-- Fin del contenido visible -->

</html>
<!-- Fin del documento HTML -->

```

### Ejercicio 2: Link a otra página

```
pagina 1:

<!DOCTYPE html>
<html lang="es">
<head>
<title>Mi sitio</title>
</head>

<body>

  

<h1>Página principal</h1>

<a href="pagina2.html">Ir a la segunda página</a>

</body>
</html>
```

```
pagina 2
<!DOCTYPE html>
<html lang="es">
<head>
<title>Página 2</title>
<meta charset="UTF-8">
</head>

<body>


<h1>Esta es la segunda página</h1>

<a href="index.html" >Volver a la página principal</a>
<!--<a href="index.html" target="_blank">Volver a la página principal en otra pestaña</a>-->

<!--<a href="https://www.wikipedia.org" target="_blank"> Ir a Wikipedia</a>-->
</body>
</html>
```

### Ejercicio #: 3 Páginas
index.html obra.html contacto.html

index.html:
```
<h1>Mi sitio</h1>

<a href="obra.html">Obra</a><br>
<a href="contacto.html">Contacto</a>
```
obra.html
```
<h1>Mi obra</h1>

<p>Descripción de mi trabajo artístico</p>

<a href="index.html">Inicio</a><br>
<a href="contacto.html">Contacto</a>
```
contacto.html
```
<h1>Contacto</h1>

<p>email@email.com</p>

<a href="index.html">Inicio</a><br>
<a href="obra.html">Obra</a>
```
## Ejercicio insertar imágenes en cada página.
### Supongamos que tienes estas imágenes en la misma carpeta:
obra.jpg contacto.jpg inicio.jpg

### Ejemplo:
index.html:
```
<!DOCTYPE html>
<html>
<head>
<title>Inicio</title>
</head>

<body>

<h1>Mi sitio</h1>

<img src="inicio.jpg" alt="Imagen de inicio" width="300">

<br><br>

<a href="obra.html">Obra</a><br>
<a href="contacto.html">Contacto</a>

</body>
</html>
```
obra.html:
```
<!DOCTYPE html>
<html>
<head>
<title>Obra</title>
</head>

<body>

<h1>Mi obra</h1>

<img src="obra.jpg" alt="Imagen de la obra" width="300">

<p>Descripción de mi trabajo artístico</p>

<a href="index.html">Inicio</a><br>
<a href="contacto.html">Contacto</a>

</body>
</html>
```
contacto.html:
```
<!DOCTYPE html>
<html>
<head>
<title>Contacto</title>
</head>

<body>

<h1>Contacto</h1>

<img src="contacto.jpg" alt="Imagen de contacto" width="300">

<p>email@email.com</p>

<a href="index.html">Inicio</a><br>
<a href="obra.html">Obra</a>

</body>
</html>
```
### Cosas importantes (errores comunes)
La imagen debe estar en la misma carpeta o usar rutas correctas El nombre debe coincidir exactamente:

X Obra.jpg ≠ obra.jpg Siempre usar alt (accesibilidad + buenas prácticas)

### Bonus: Hacer la imagen clickeable (como link)
```
<a href="obra.html">
  <img src="inicio.jpg" alt="Ir a obra" width="300">
</a>
```
Esto transforma la imagen en un botón visual.

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bitácora — Amanda Solís Biénzobas</title>
  <style>
    :root {
      color-scheme: light;
      --pastel-pink: #f9dce8;
      --fuchsia: #d00070;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      background: var(--pastel-pink);
      color: var(--fuchsia);
      text-align: center;
    }

    main {
      min-height: 100vh;
      display: grid;
      place-items: center;
      padding: 2rem;
    }

    h1 {
      margin: 0;
      font-family: Didot, "Bodoni 72", "Times New Roman", serif;
      font-size: clamp(3.5rem, 12vw, 8rem);
      font-weight: 400;
      letter-spacing: 0.08em;
    }

    p {
      margin: 1rem 0 0;
      font-family: Didot, "Bodoni 72", "Times New Roman", serif;
      font-size: clamp(1.5rem, 4vw, 2.2rem);
      letter-spacing: 0.04em;
    }

    .intro-page {
      min-height: 100vh;
      display: grid;
      place-items: center;
      padding: clamp(2rem, 6vw, 5rem);
    }

    .intro-content {
      width: min(48rem, 100%);
      text-align: left;
    }

    .intro-content p {
      margin: 0;
      font-size: clamp(1.2rem, 2.4vw, 1.7rem);
      letter-spacing: normal;
      line-height: 1.35;
    }

    .intro-content p + p {
      margin-top: 1.5rem;
    }

    .exercise {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      padding: clamp(2rem, 6vw, 5rem);
      text-align: left;
    }

    .exercise-content {
      max-width: min(40rem, 100%);
    }

    .exercise-content p {
      margin: 0;
    }

    .exercise-content p + p {
      margin-top: 0.5rem;
      font-size: clamp(1.2rem, 2.4vw, 1.7rem);
      letter-spacing: normal;
      line-height: 1.35;
    }

    .exercise-content .summary {
      margin-top: 1.5rem;
    }

    .exercise-content .second-part {
      margin-top: 1.5rem;
    }

    .exercise-content .section-heading {
      margin-top: 1.5rem;
      font-size: clamp(1.5rem, 4vw, 2.2rem);
      letter-spacing: 0.04em;
      line-height: normal;
    }

    .sketch {
      margin: 1.5rem 0 0;
    }

    .sketch figcaption {
      margin-bottom: 0.5rem;
      font-family: Didot, "Bodoni 72", "Times New Roman", serif;
      font-size: clamp(1.2rem, 2.4vw, 1.7rem);
      font-weight: 700;
      line-height: 1.35;
    }

    .sketch img {
      display: block;
      width: 100%;
      max-width: 32rem;
      height: auto;
    }

    .proposal-page {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 1.5rem;
      padding: 2rem;
    }

    .proposal-page .section-heading {
      margin-top: 0;
    }

    .proposal-intro {
      max-width: min(48rem, 100%);
      margin: 0;
      font-size: clamp(1.2rem, 2.4vw, 1.7rem);
      letter-spacing: normal;
      line-height: 1.35;
      text-align: center;
    }

    .proposal-card {
      width: min(48rem, 100%);
      padding: clamp(1.25rem, 3vw, 2rem);
      background: #fff3f8;
      border: 1px solid #f2c5d8;
      border-radius: 0.75rem;
    }

    .proposal-card p {
      margin: 0;
      font-size: clamp(1.05rem, 2vw, 1.35rem);
      letter-spacing: normal;
      line-height: 1.55;
      text-align: left;
    }

    .proposal-card p + p {
      margin-top: 1rem;
    }

    .proposal-continuation {
      width: min(48rem, 100%);
      text-align: left;
    }

    .proposal-continuation p {
      margin: 0;
      font-size: clamp(1.05rem, 2vw, 1.35rem);
      letter-spacing: normal;
      line-height: 1.55;
    }

    .proposal-continuation p + p {
      margin-top: 1rem;
    }

    .final-delivery {
      width: min(48rem, 100%);
      text-align: left;
    }

    .final-delivery p {
      margin: 0;
      font-size: clamp(1.05rem, 2vw, 1.35rem);
      letter-spacing: normal;
      line-height: 1.55;
    }

    .final-delivery p + p {
      margin-top: 0.75rem;
    }

    .exercise-link a {
      color: inherit;
    }
  </style>
</head>
<body>
  <main>
    <h1>BITÁCORA TouchDesigner</h1>
    <p>Amanda Solís Biénzobas</p>
  </main>
  <section class="intro-page">
    <div class="intro-content">
      <p>Esta bitácora funciona como un registro de trabajo con el programa TouchDesigner, pero también funciona como poemario, porque ¿qué tipo de poeta sería yo si no volviera todo lo que hago en un poema?</p>
      <p>La primera parte indica de forma objetiva los cambios e implementaciones hechas en este programa, pero luego no me haré cargo de mis poesías y palabras.</p>
    </div>
  </section>
  <section class="exercise">
    <div class="exercise-content">
      <p>Ejercicios:</p>
      <p>Primera parte:</p>
      <p>Para el ejercicio I trabajamos con disipación de partículas en imágenes. Luego, en el ejercicio II trabajamos con sliders, y para el ejercicio III trabajamos la creación de un objeto en tres dimensiones.</p>
      <p class="summary">Estos tres ejercicios lo integré en uno solo. Donde puedes interactuar con los tres elementos.</p>
      <p class="exercise-link"><a href="sliders.4.toe" download>Descargar ejercicio para TouchDesigner (.toe)</a></p>
      <p class="second-part">Segunda parte:</p>
      <p>Para el proyecto final de este ramo trabajé con textos propios, los cuales fui modificando en un inicio.</p>
      <p>Utilicé un tutorial de youtube como base para crear una obra interactiva.</p>
      <p class="exercise-link"><a href="https://youtu.be/RZfB_uvWiMY?si=Bbot70-yhk3h_fL5" target="_blank" rel="noopener noreferrer">https://youtu.be/RZfB_uvWiMY?si=Bbot70-yhk3h_fL5</a></p>
      <p>Luego de crear la base de este proyecto fui modificando los nodos que ya estaban en el programa para llegar al resultado que quería.</p>
      <p>Fui experimentando en los nodos de rgbaDelay, feedback y feedback1, rgbkey1, y dentro de la base1 donde modifiqué y agregué distintos textos.</p>
      <p class="section-heading">Resumen de la obra:</p>
      <p>La obra consiste en una pantalla o proyección horizontal, de 720 x 1280 píxeles. Dentro de ella hay un fondo negro con palabras blancas que se desplazan horizontalmente por la pantalla; cada línea de palabras dice algo distinto: “ser mujer”, “me permite”, “encontrar lo que amo”. Las palabras no se ven de inmediato en la pantalla; es necesario mover el cursor para poder ir divisando las frases, como si fuera una lupa.</p>
      <figure class="sketch">
        <figcaption>Boceto:</figcaption>
        <img src="‎Screenshot_20261020_162315_Clip Studio.jpg‎" alt="Boceto de una obra interactiva con un monitor, textos en pantalla y una mano que interactúa con ellos">
      </figure>
    </div>
  </section>
  <section class="proposal-page">
    <p class="section-heading">Propuesta conceptual</p>
    <p class="proposal-intro">Para conocer mi propuesta conceptual me parece importante conocer un resumen de mi trabajo artístico.</p>
    <article class="proposal-card">
      <p>Mi trabajo transita entre la fotografía de detalles corporales, la intervención textual y la materialidad editorial. Utilizando fanzines, libros de artista y soportes de papel vegetal con transparencias, la palabra escrita no solo se lee, sino que funciona y se percibe como imagen. Esta aproximación editorial permite descentralizar la obra de los circuitos de exhibición tradicionales (como galerías y museos), apostando por la serialidad y una circulación orgánica, táctil e íntima de mano en mano.</p>
      <p>Me interesa trabajar con la corporalidad del espectador y su interacción con mi obra, por lo que esta obra se integra dentro de mis expectativas al momento de crear.</p>
    </article>
    <div class="proposal-continuation">
      <p>Cada frase que emerge y se despliega en la pantalla constituye un fragmento de las reflexiones escritas en el marco de mi examen de grado, un espacio de investigación visual e intelectual donde abordo activamente la reapropiación del término mujer desde una perspectiva feminista.</p>
      <p>A través de esta instalación, el texto deja de ser un simple registro académico para transformarse en un gesto estético y político. La pantalla opera como un soporte donde la palabra escrita adquiere una dimensión temporal, permitiendo al espectador habitar el proceso de deconstrucción y resignificación del concepto.</p>
      <p>Las frases, al aparecer de manera intermitente o fragmentaria, invitan a una lectura pausada que interpela directamente a quien observa. No se trata solo de exponer un discurso, sino de generar un espacio de resonancia afectiva y conceptual donde el lenguaje se evidencia como una herramienta viva de reflexión. Así, la obra se ubica en el cruce entre la teoría feminista, la creación artística y la experiencia personal, proponiendo que la reapropiación simbólica de las palabras es un paso fundamental para nombrar y habitarnos desde nuestras propias narrativas.</p>
    </div>
    <div class="final-delivery">
      <p>Para finalizar entrego el documento con mi trabajo.</p>
      <p class="exercise-link"><a href="texto1.7.toe" download>Descargar documento final de TouchDesigner (.toe)</a></p>
    </div>
  </section>
</body>
</html>
