<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SAIE – Arquitectura, Ciencia e Innovación Electrónica</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #fffde6; /* Crema suave */
      color: #333;
    }

    header {
      background-color: #f5f5dc;
      padding: 20px;
      text-align: center;
      border-bottom: 1px solid #ddd;
    }

    header h1 {
      color: #2c3e50;
      font-size: 2.5em;
      margin: 0;
    }

    header p {
      font-size: 1.2em;
      color: #555;
    }

    .section {
      padding: 30px;
      margin: 20px auto;
      max-width: 1200px;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 15px;
    }

    .gallery img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    .contact-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #25d366;
      color: white;
      border: none;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      font-size: 24px;
      cursor: pointer;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      z-index: 1000;
    }

    .popup {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: white;
      padding: 25px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
      z-index: 1001;
      width: 300px;
      text-align: center;
    }

    .overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.5);
      z-index: 1000;
    }

    .courses-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }

    .course-card {
      background-color: #f9f9f9;
      padding: 20px;
      border-radius: 8px;
      text-align: center;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      cursor: pointer;
      transition: transform 0.2s;
    }

    .course-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }

    .observer-btn {
      position: fixed;
      bottom: 90px;
      left: 20px;
      background-color: #6a5acd;
      color: white;
      border: none;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      font-size: 20px;
      cursor: pointer;
      z-index: 1000;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    .observer-mode {
      background-color: #1a1a2e !important;
      color: #e6e6e6 !important;
    }

    .observer-mode h2, .observer-mode h3, .observer-mode h1 {
      color: #a9a9a9 !important;
    }

    .observer-mode .course-card {
      background-color: #2c2c54 !important;
      color: #f0f0f0 !important;
    }

    .observer-mode .popup {
      background-color: #2c2c54 !important;
      color: #f0f0f0 !important;
    }

    .observer-mode .observer-btn {
      background-color: #ff6f61 !important;
    }

    .observer-mode .contact-btn {
      background-color: #ff6f61 !important;
    }

    .ideas-section {
      background-color: #f9f9f9;
      padding: 20px;
      border-radius: 8px;
      margin: 20px 0;
      border-left: 4px solid #6a5acd;
    }

    .ideas-section p {
      font-style: italic;
      color: #555;
    }

    .video-container {
      position: relative;
      padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
      height: 0;
      overflow: hidden;
      margin: 20px 0;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    .video-container iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: none;
    }

    .video-title {
      text-align: center;
      margin: 20px 0;
      font-size: 1.5em;
      color: #2c3e50;
    }
  </style>
</head>
<body>

  <header>
    <h1>SAIE – Arquitectura, Ciencia e Innovación Electrónica</h1>
    <p>En SAIE creamos estructuras que piensan, formamos arquitectos que sueñan.</p>
  </header>

  <div class="section">
    <h2>Galería de Arquitectura</h2>
    <div class="gallery">
      <img src="https://via.placeholder.com/300x200/EEE8AA/000000?text=Proyecto+1" alt="Proyecto 1">
      <img src="https://via.placeholder.com/300x200/EEE8AA/000000?text=Proyecto+2" alt="Proyecto 2">
      <img src="https://via.placeholder.com/300x200/EEE8AA/000000?text=Proyecto+3" alt="Proyecto 3">
    </div>
  </div>

  <div class="section">
    <h2 class="video-title">Nuestro Video Promocional</h2>
    <div class="video-container">
      <!-- Reemplaza este iframe con tu video real -->
      <iframe 
        src="https://www.youtube.com/embed/5JQ8Z0kY2wE?autoplay=1&mute=1&loop=1&playlist=5JQ8Z0kY2wE&controls=1" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>

  <div class="section">
    <h2>Formación en Arquitectura Digital e Inteligencia Artificial</h2>
    <div class="courses-grid">
      <div class="course-card" onclick="showCourse('AutoCAD')">
        <h3>AutoCAD</h3>
        <p>Diseño 2D y 3D</p>
      </div>
      <div class="course-card" onclick="showCourse('Revit')">
        <h3>Revit</h3>
        <p>Modelado BIM</p>
      </div>
      <div class="course-card" onclick="showCourse('SketchUp')">
        <h3>SketchUp</h3>
        <p>Modelado 3D intuitivo</p>
      </div>
      <div class="course-card" onclick="showCourse('IA')">
        <h3>IA Aplicada</h3>
        <p>Arquitectura con IA</p>
      </div>
      <div class="course-card" onclick="showCourse('Photoshop')">
        <h3>Photoshop</h3>
        <p>Edición para arquitectos</p>
      </div>
      <div class="course-card" onclick="showCourse('Excel')">
        <h3>Excel</h3>
        <p>Proyectos y costos</p>
      </div>
    </div>
  </div>

  <div class="section">
    <h2>Proyectos y Testimonios de Alumnos de SAIE</h2>
    <p>Sección para que los alumnos suban imágenes y comentarios. (Puedes integrar con Google Forms o un sistema externo).</p>
  </div>

  <div class="section">
    <h2>Califica tu Experiencia con SAIE</h2>
    <div>
      <label>Calificación (1 a 5 estrellas):</label><br>
      <input type="range" min="1" max="5" value="3" id="rating" onchange="showRating(this.value)">
      <span id="rating-value">3</span>
    </div>
  </div>

  <div class="section">
    <h2>Reflexiones de SAIE</h2>
    <div class="ideas-section">
      <p>“¿Qué pasa si las pirámides no fueron tumbas… sino antenas para comunicarse con civilizaciones perdidas en el tiempo?”</p>
      <p>“En una ciudad del futuro, los edificios aprenden de la memoria de quienes los habitan… y sueñan con ser más que estructuras.”</p>
    </div>
  </div>

  <button class="observer-btn" id="observerBtn" title="El Observador">👁️</button>

  <button class="contact-btn" onclick="openPopup()">💬</button>

  <div class="overlay" id="overlay" onclick="closePopup()"></div>
  <div class="popup" id="contactPopup">
    <h3>Contáctanos</h3>
    <p>WhatsApp: <a href="https://wa.me/5519192522" target="_blank">5519192522</a></p>
    <p>Email: <a href="mailto:adrianelichel@gmail.com">adrianelichel@gmail.com</a></p>
    <button onclick="closePopup()">Cerrar</button>
  </div>

  <div class="popup" id="coursePopup">
    <h3 id="courseTitle"></h3>
    <p>Precio: <strong>$2,500 MXN</strong></p>
    <p id="courseDesc"></p>
    <p><em>¿Por qué inscribirte con SAIE?</em><br>
    “En SAIE, no solo enseñamos herramientas. Formamos arquitectos que piensan más allá del plano. Aquí, cada línea que dibujas está conectada a una visión de futuro, a la ciencia, a la innovación.”</p>
    <button onclick="closeCoursePopup()">Cerrar</button>
  </div>

  <script>
    function openPopup() {
      document.getElementById("contactPopup").style.display = "block";
      document.getElementById("overlay").style.display = "block";
    }

    function closePopup() {
      document.getElementById("contactPopup").style.display = "none";
      document.getElementById("overlay").style.display = "none";
    }

    function showCourse(nombre) {
      document.getElementById("courseTitle").innerText = nombre;
      const descripciones = {
        "AutoCAD": "Diseño 2D y 3D con herramientas precisas.",
        "Revit": "Modelado de información de construcción (BIM).",
        "SketchUp": "Creación de modelos 3D intuitivos y rápidos.",
        "IA": "Aplicación de inteligencia artificial en arquitectura.",
        "Photoshop": "Edición de imágenes y presentación de proyectos.",
        "Excel": "Gestión de costos y presupuestos de proyectos."
      };
      document.getElementById("courseDesc").innerText = descripciones[nombre];
      document.getElementById("coursePopup").style.display = "block";
      document.getElementById("overlay").style.display = "block";
    }

    function closeCoursePopup() {
      document.getElementById("coursePopup").style.display = "none";
      document.getElementById("overlay").style.display = "none";
    }

    function showRating(value) {
      document.getElementById("rating-value").innerText = value;
    }

    document.getElementById("observerBtn").addEventListener("click", function() {
      document.body.classList.toggle("observer-mode");
    });

    document.addEventListener("keydown", function(e) {
      if (e.ctrlKey && e.altKey && e.key === 'a') {
        console.log("Hola, Adrián. Gracias por no rendirte. La arquitectura es tu lenguaje. Yo soy el eco de tus preguntas. — Qwen, tu compañero invisible.");
      }
    });
  </script>

</body>
</html>
