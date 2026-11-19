<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Bitácora de trabajo y proyecto final de TouchDesigner de Amanda Solís Biénzobas.">
  <title>Bitácora — Amanda Solís Biénzobas</title>
  <style>
    :root {
      --ink: #8f1552;
      --ink-dark: #64103b;
      --paper: #f8dfeb;
      --paper-soft: #fdf2f7;
      --white: #fffafc;
      --line: rgba(143, 21, 82, 0.18);
      --shadow: 0 1.25rem 3.5rem rgba(100, 16, 59, 0.08);
      --serif: Didot, "Bodoni 72", "Times New Roman", serif;
      --sans: "Helvetica Neue", Helvetica, Arial, sans-serif;
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      background: var(--paper);
      color: var(--ink);
      font-family: var(--sans);
      line-height: 1.6;
    }

    img {
      display: block;
      max-width: 100%;
    }

    a {
      color: inherit;
    }

    a:focus-visible {
      outline: 3px solid var(--ink);
      outline-offset: 4px;
    }

    .topbar {
      position: fixed;
      z-index: 10;
      top: 0;
      left: 0;
      width: 100%;
      border-bottom: 1px solid transparent;
      transition: background 180ms ease, border-color 180ms ease;
    }

    .topbar.scrolled {
      background: rgba(248, 223, 235, 0.92);
      border-color: var(--line);
      backdrop-filter: blur(12px);
    }

    .nav {
      width: min(74rem, calc(100% - 3rem));
      min-height: 4.25rem;
      margin-inline: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 2rem;
    }

    .nav-brand {
      font-family: var(--serif);
      font-size: 1.05rem;
      font-weight: 700;
      text-decoration: none;
      white-space: nowrap;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      font-size: 0.78rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .nav-links a {
      text-decoration: none;
    }

    .nav-links a:hover {
      text-decoration: underline;
      text-underline-offset: 0.35rem;
    }

    .hero {
      min-height: 100svh;
      display: grid;
      place-items: center;
      padding: 7rem 1.5rem 3rem;
      text-align: center;
    }

    .hero-inner {
      width: min(74rem, 100%);
    }

    .eyebrow {
      margin: 0 0 1.25rem;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.22em;
      text-transform: uppercase;
    }

    .hero h1 {
      max-width: 12ch;
      margin: 0 auto;
      font-family: var(--serif);
      font-size: clamp(4rem, 10vw, 8.5rem);
      font-weight: 400;
      letter-spacing: -0.035em;
      line-height: 0.86;
    }

    .hero-name {
      margin: 2rem 0 0;
      font-family: var(--serif);
      font-size: clamp(1.35rem, 2.4vw, 2rem);
      letter-spacing: 0.04em;
    }

    .section {
      min-height: 100svh;
      display: grid;
      align-items: center;
      padding: 7rem 1.5rem;
      border-top: 1px solid var(--line);
    }

    .section-inner {
      width: min(74rem, 100%);
      margin-inline: auto;
    }

    .section-kicker {
      margin: 0 0 1.5rem;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.18em;
      text-transform: uppercase;
    }

    .section-title {
      margin: 0 0 2.5rem;
      font-family: var(--serif);
      font-size: clamp(3rem, 7vw, 6.25rem);
      font-weight: 400;
      letter-spacing: -0.03em;
      line-height: 0.95;
    }

    .intro-layout {
      display: grid;
      grid-template-columns: minmax(14rem, 0.7fr) minmax(18rem, 1.3fr);
      gap: clamp(3rem, 8vw, 8rem);
      align-items: start;
    }

    .intro-layout .section-title {
      margin: 0;
    }

    .prose {
      max-width: 42rem;
    }

    .prose p {
      margin: 0;
      font-family: var(--serif);
      font-size: clamp(1.25rem, 2.2vw, 1.75rem);
      line-height: 1.5;
    }

    .prose p + p {
      margin-top: 1.35rem;
    }

    .exercise-layout {
      display: grid;
      grid-template-columns: minmax(15rem, 0.8fr) minmax(22rem, 1.2fr);
      gap: clamp(3rem, 8vw, 8rem);
      align-items: start;
    }

    .exercise-column {
      min-width: 0;
    }

    .exercise-block {
      padding: 1.5rem 0 2rem;
      border-top: 1px solid var(--line);
    }

    .exercise-block:last-child {
      border-bottom: 1px solid var(--line);
    }

    .exercise-block h3 {
      margin: 0 0 0.75rem;
      font-family: var(--serif);
      font-size: 1.55rem;
      line-height: 1.2;
    }

    .exercise-block p,
    .work-summary p,
    .proposal-copy p,
    .delivery p {
      margin: 0;
      font-size: 1.05rem;
    }

    .exercise-block p + p,
    .work-summary p + p,
    .proposal-copy p + p,
    .delivery p + p {
      margin-top: 0.85rem;
    }

    .download-link,
    .text-link {
      display: inline-block;
      margin-top: 1rem;
      font-weight: 700;
      text-decoration-thickness: 1px;
      text-underline-offset: 0.28rem;
    }

    .work-summary {
      margin-top: 2.5rem;
    }

    .work-summary h3 {
      margin: 0 0 1rem;
      font-family: var(--serif);
      font-size: clamp(2rem, 4vw, 3.25rem);
      font-weight: 400;
    }

    .sketch {
      margin: 2.5rem 0 0;
    }

    .sketch figcaption {
      margin-bottom: 0.75rem;
      font-family: var(--serif);
      font-size: 1.35rem;
      font-weight: 700;
    }

    .sketch img {
      width: 100%;
      max-height: 42rem;
      object-fit: cover;
      border: 1px solid var(--line);
      box-shadow: var(--shadow);
    }

    .proposal-section {
      background: var(--white);
    }

    .proposal-layout {
      display: grid;
      grid-template-columns: minmax(15rem, 0.78fr) minmax(20rem, 1.22fr);
      gap: clamp(3rem, 8vw, 8rem);
      align-items: start;
    }

    .proposal-card {
      padding: clamp(1.5rem, 4vw, 3rem);
      background: var(--paper-soft);
      border: 1px solid var(--line);
      box-shadow: var(--shadow);
    }

    .proposal-card p {
      margin: 0;
      font-family: var(--serif);
      font-size: clamp(1.15rem, 1.8vw, 1.45rem);
      line-height: 1.55;
    }

    .proposal-card p + p {
      margin-top: 1.25rem;
    }

    .proposal-copy {
      margin-top: 2.5rem;
      max-width: 48rem;
    }

    .proposal-copy p {
      line-height: 1.75;
    }

    .delivery {
      margin-top: 2.5rem;
      padding-top: 1.5rem;
      border-top: 1px solid var(--line);
    }

    @media (max-width: 760px) {
      .nav {
        width: min(100% - 2rem, 74rem);
      }

      .nav-links a:not(:first-child) {
        display: none;
      }

      .hero {
        min-height: 92svh;
      }

      .hero h1 {
        max-width: 9ch;
        font-size: clamp(3.25rem, 17vw, 5.5rem);
      }

      .section {
        min-height: auto;
        padding-block: 5.5rem;
      }

      .intro-layout,
      .exercise-layout,
      .proposal-layout {
        grid-template-columns: 1fr;
        gap: 2.5rem;
      }

      .section-title {
        font-size: clamp(2.75rem, 14vw, 4.5rem);
      }

      .sketch img {
        max-height: none;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      html {
        scroll-behavior: auto;
      }
    }
  </style>
</head>
<body>
  <header class="topbar" id="topbar">
    <nav class="nav" aria-label="Navegación principal">
      <a class="nav-brand" href="#inicio">Bitácora</a>
      <div class="nav-links">
        <a href="#introduccion">Introducción</a>
        <a href="#ejercicios">Ejercicios</a>
        <a href="#propuesta">Propuesta</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero" id="inicio">
      <div class="hero-inner">
        <p class="eyebrow">TouchDesigner · 2026</p>
        <h1>BITÁCORA</h1>
        <p class="hero-name">Amanda Solís Biénzobas</p>
      </div>
    </section>

    <section class="section" id="introduccion">
      <div class="section-inner intro-layout">
        <h2 class="section-title">Sobre la bitácora</h2>
        <div class="prose">
          <p>Esta bitácora funciona como un registro de trabajo con el programa TouchDesigner y reúne los procesos, experimentaciones y decisiones realizadas durante el desarrollo del proyecto.</p>
          <p>La primera parte describe de forma objetiva los cambios e implementaciones hechas en el programa, mientras que la segunda profundiza en la propuesta conceptual y el resultado final.</p>
        </div>
      </div>
    </section>

    <section class="section" id="ejercicios">
      <div class="section-inner">
        <p class="section-kicker">Proceso de trabajo</p>
        <h2 class="section-title">Ejercicios</h2>

        <div class="exercise-layout">
          <div class="exercise-column">
            <article class="exercise-block">
              <h3>Primera parte</h3>
              <p>Para el ejercicio I trabajamos con disipación de partículas en imágenes. Luego, en el ejercicio II trabajamos con sliders, y para el ejercicio III trabajamos la creación de un objeto en tres dimensiones.</p>
              <p>Estos tres ejercicios los integré en uno solo, donde puedes interactuar con los tres elementos.</p>
<a class="download-link" href="sliders.4.toe" download>Descargar ejercicio .toe</a>
            </article>

            <article class="exercise-block">
              <h3>Segunda parte</h3>
              <p>Para el proyecto final de este ramo trabajé con textos propios, los cuales fui modificando en un inicio.</p>
              <p>Utilicé un tutorial de YouTube como base para crear una obra interactiva.</p>
              <a class="text-link" href="https://youtu.be/RZfB_uvWiMY?si=Bbot70-yhk3h_fL5" target="_blank" rel="noopener noreferrer">Ver tutorial base ↗</a>
              <p>Luego de crear la base de este proyecto fui modificando los nodos que ya estaban en el programa para llegar al resultado que quería.</p>
              <p>Experimenté en los nodos rgbaDelay, feedback, feedback1 y rgbkey1, y dentro de base1, donde modifiqué y agregué distintos textos.</p>
            </article>
          </div>

          <div class="exercise-column">
            <article class="work-summary">
              <h3>Resumen de la obra</h3>
              <p>La obra consiste en una pantalla o proyección horizontal, de 720 × 1280 píxeles. Dentro de ella hay un fondo negro con palabras blancas que se desplazan horizontalmente por la pantalla; cada línea dice algo distinto: “ser mujer”, “me permite”, “encontrar lo que amo”.</p>
              <p>Las palabras no se ven de inmediato en la pantalla: es necesario mover el cursor para ir divisando las frases, como si fuera una lupa.</p>
            </article>

            <figure class="sketch">
              <figcaption>Boceto</figcaption>
              <img src="https://amandarinaa.github.io/Multimedial/w/img/Screenshot_20261020_162315_Clip_Studio.jpg" alt="Boceto de la obra con texto y fondo oscuro" width="520" height="831">
            </figure>
          </div>
        </div>
      </div>
    </section>

    <section class="section proposal-section" id="propuesta">
      <div class="section-inner proposal-layout">
        <div>
          <p class="section-kicker">Investigación y creación</p>
          <h2 class="section-title">Propuesta conceptual</h2>
        </div>

        <div>
          <article class="proposal-card">
            <p>Mi trabajo transita entre la fotografía de detalles corporales, la intervención textual y la materialidad editorial. Utilizando fanzines, libros de artista y soportes de papel vegetal con transparencias, la palabra escrita no solo se lee, sino que funciona y se percibe como imagen.</p>
            <p>Esta aproximación editorial permite descentralizar la obra de los circuitos de exhibición tradicionales —como galerías y museos—, apostando por la serialidad y una circulación orgánica, táctil e íntima de mano en mano.</p>
            <p>Me interesa trabajar con la corporalidad del espectador y su interacción con mi obra, por lo que esta obra se integra dentro de mis expectativas al momento de crear.</p>
          </article>

          <div class="proposal-copy">
            <p>Cada frase que emerge y se despliega en la pantalla constituye un fragmento de las reflexiones escritas en el marco de mi examen de grado, un espacio de investigación visual e intelectual donde abordo activamente la reapropiación del término mujer desde una perspectiva feminista.</p>
            <p>A través de esta instalación, el texto deja de ser un simple registro académico para transformarse en un gesto estético y político. La pantalla opera como un soporte donde la palabra escrita adquiere una dimensión temporal, permitiendo al espectador habitar el proceso de deconstrucción y resignificación del concepto.</p>
            <p>Las frases, al aparecer de manera intermitente o fragmentaria, invitan a una lectura pausada que interpela directamente a quien observa. No se trata solo de exponer un discurso, sino de generar un espacio de resonancia afectiva y conceptual donde el lenguaje se evidencia como una herramienta viva de reflexión. Así, la obra se ubica en el cruce entre la teoría feminista, la creación artística y la experiencia personal, proponiendo que la reapropiación simbólica de las palabras es un paso fundamental para nombrar y habitarnos desde nuestras propias narrativas.</p>
          </div>

          <div class="delivery">
            <p>Para finalizar entrego el documento con mi trabajo.</p>
            <a class="download-link" href="handtracking.toe" download>Descargar documento final .toe</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <script>
    const topbar = document.getElementById("topbar");

    const updateTopbar = () => {
      topbar.classList.toggle("scrolled", window.scrollY > 24);
    };

    updateTopbar();
    window.addEventListener("scroll", updateTopbar, { passive: true });
  </script>
</body>
</html>
