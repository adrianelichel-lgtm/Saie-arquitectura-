<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>SAIE — Cursos de Arquitectura, Diseño e IA</title>
  <style>
    :root {
      --azul-fuerte: #003366;
      --crema: #F8F3E6;
      --blanco: #ffffff;
      --gris: #555;
      --gris-claro: #f4f4f4;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--blanco);
      color: var(--gris);
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: 0 auto;
    }

    header {
      background-color: var(--azul-fuerte);
      color: var(--crema);
      padding: 1rem 0;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .header-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo img {
      height: 50px;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 1.5rem;
    }

    .btn {
      background-color: var(--crema);
      color: var(--azul-fuerte);
      padding: 0.5rem 1rem;
      border-radius: 4px;
      font-weight: bold;
      border: 2px solid var(--crema);
      transition: all 0.3s;
    }

    .btn:hover {
      background-color: transparent;
      color: var(--crema);
    }

    .hero {
      background: linear-gradient(rgba(0, 51, 102, 0.85), rgba(0, 51, 102, 0.85)), url('https://images.unsplash.com/photo-1503387762-592deb58ef4e?ixlib=rb-4.0.3') no-repeat center center/cover;
      color: var(--crema);
      text-align: center;
      padding: 5rem 1rem;
    }

    .hero h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    .hero-buttons {
      margin-top: 1.5rem;
    }

    .hero-buttons a {
      margin: 0 0.75rem;
      display: inline-block;
    }

    section {
      padding: 4rem 0;
    }

    .section-title {
      text-align: center;
      font-size: 2rem;
      color: var(--azul-fuerte);
      margin-bottom: 2rem;
    }

    .cursos-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
    }

    .curso-card {
      background: var(--blanco);
      border: 2px solid var(--azul-fuerte);
      border-radius: 8px;
      padding: 1.5rem;
      text-align: center;
      transition: transform 0.3s;
      cursor: pointer;
    }

    .curso-card:hover {
      transform: translateY(-5px);
    }

    .curso-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 6px;
      margin-bottom: 1rem;
    }

    .modal {
      display: none;
      position: fixed;
      z-index: 1001;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.7);
      overflow: auto;
    }

    .modal-content {
      background: var(--blanco);
      margin: 10% auto;
      padding: 2rem;
      border-radius: 8px;
      max-width: 800px;
      position: relative;
    }

    .close {
      color: var(--gris);
      float: right;
      font-size: 28px;
      font-weight: bold;
      cursor: pointer;
    }

    .modal-header {
      display: flex;
      align-items: center;
      gap: 1rem;
      margin-bottom: 1rem;
    }

    .modal-header img {
      width: 80px;
      height: auto;
    }

    .modal-body {
      margin: 1.5rem 0;
    }

    .modal-footer {
      text-align: center;
      margin-top: 1.5rem;
    }

    .modal-footer a {
      margin: 0 0.5rem;
    }

    .beneficios {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
      text-align: center;
    }

    .contacto-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
    }

    .contacto-info, .contacto-form {
      padding: 1.5rem;
    }

    .contacto-info {
      background-color: var(--crema);
    }

    form input, form textarea, form select {
      width: 100%;
      padding: 0.75rem;
      margin: 0.5rem 0;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    footer {
      background-color: var(--azul-fuerte);
      color: var(--crema);
      text-align: center;
      padding: 2rem 0;
    }

    footer .logo img {
      height: 60px;
      margin-bottom: 1rem;
    }

    @media (max-width: 768px) {
      .header-content {
        flex-direction: column;
        gap: 1rem;
      }

      nav ul {
        gap: 1rem;
        flex-wrap: wrap;
        justify-content: center;
      }

      .hero h1 {
        font-size: 2rem;
      }

      .contacto-grid {
        grid-template-columns: 1fr;
      }

      .hero-buttons a {
        display: block;
        margin: 0.5rem 0;
      }

      .modal-content {
        margin: 20% auto;
        padding: 1rem;
      }
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <header>
    <div class="container header-content">
      <div class="logo">
        <img src="https://i.ibb.co/tTQf3kdQ/adriax-chelele-v.jpg" alt="SAIE - Soluciones Arquitectónicas e Innovación de Espacios">
      </div>
      <nav>
        <ul>
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#cursos">Cursos</a></li>
          <li><a href="#nosotros">Sobre Nosotros</a></li>
          <li><a href="#contacto">Contacto</a></li>
        </ul>
      </nav>
      <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
    </div>
  </header>

  <!-- HERO -->
  <section id="inicio" class="hero">
    <div class="container">
      <h1>Domina las herramientas del futuro con SAIE</h1>
      <p>Cursos profesionales en AutoCAD, Revit, SketchUp, Photoshop, Illustrator, Excel e Inteligencia Artificial —diseñados para arquitectos, diseñadores y creadores modernos.</p>
      <div class="hero-buttons">
        <a href="#cursos" class="btn">Ver todos los cursos</a>
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Agendar asesoría</a>
      </div>
    </div>
  </section>

  <!-- CURSOS -->
  <section id="cursos" class="container">
    <h2 class="section-title">Nuestros Cursos</h2>
    <div class="cursos-grid">
      <div class="curso-card" onclick="openModal('modal1')">
        <img src="https://i.ibb.co/dwThSPtb/FB-IMG-1763240283155.jpg" alt="Curso de IA">
        <h3>Inteligencia Artificial</h3>
        <p>Desde cero hasta nivel profesional. Generación, automatización y análisis con IA.</p>
      </div>
      <div class="curso-card" onclick="openModal('modal2')">
        <img src="https://i.ibb.co/LX90w1L1/FB-IMG-1763240283155.jpg" alt="Curso de Excel + IA">
        <h3>Excel + IA</h3>
        <p>Básico, intermedio, avanzado y análisis inteligente con IA.</p>
      </div>
      <div class="curso-card" onclick="openModal('modal3')">
        <img src="https://i.ibb.co/PGM3T2MS/FB-IMG-1763240311451.jpg" alt="Curso de Photoshop + IA">
        <h3>Photoshop + IA</h3>
        <p>Edición, renders arquitectónicos y postproducción con IA.</p>
      </div>
      <div class="curso-card" onclick="openModal('modal4')">
        <img src="https://i.ibb.co/Vk3zGMc/FB-IMG-1763240198032.jpg" alt="Curso de Illustrator + IA">
        <h3>Illustrator + IA</h3>
        <p>Diseño vectorial, branding y logotipos con IA creativa.</p>
      </div>
      <div class="curso-card" onclick="openModal('modal5')">
        <img src="https://i.ibb.co/7LQk13m/FB-IMG-1763240367547.jpg" alt="Curso de SketchUp + V-Ray + IA">
        <h3>SketchUp + V-Ray + IA</h3>
        <p>Renders fotorrealistas y presentaciones impactantes.</p>
      </div>
      <div class="curso-card" onclick="openModal('modal6')">
        <img src="https://i.ibb.co/ccJ8sJ7r/FB-IMG-1763240198032.jpg" alt="Curso de AutoCAD 2D + IA">
        <h3>AutoCAD 2D + IA</h3>
        <p>Planes arquitectónicos, estructurales y técnicos con IA.</p>
      </div>
      <div class="curso-card" onclick="openModal('modal7')">
        <img src="https://i.ibb.co/FbhWzqJ8/FB-IMG-1763240367547.jpg" alt="Curso de Revit + BIM + IA">
        <h3>Revit + BIM + IA</h3>
        <p>Modelado integral: arquitectura, estructura, MEP y BIM.</p>
      </div>
    </div>
  </section>

  <!-- MODALES -->
  <div id="modal1" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal1')">&times;</span>
      <div class="modal-header">
        <img src="https://i.ibb.co/dwThSPtb/FB-IMG-1763240283155.jpg" alt="IA Course">
        <h2>Curso Completo de Inteligencia Artificial</h2>
      </div>
      <div class="modal-body">
        <p>¡Domina la tecnología que está transformando el mundo! Aprende IA de forma práctica, clara y orientada a resultados reales. Descubre cómo la IA puede ayudarte a crear, automatizar, analizar, diseñar y optimizar casi cualquier tipo de tarea.</p>
        <p><strong>Temas:</strong> IA Generativa, Automatización Inteligente, Análisis y Datos con IA, Creación de Contenidos, Integración con Software Profesional.</p>
        <p><strong>Herramientas:</strong> ChatGPT, Claude, Copilot, Gemini, Midjourney, Firefly, Runway.</p>
        <p><strong>Incluye:</strong> Certificación profesional, soporte 24/7, acceso a prompts y plantillas.</p>
      </div>
      <div class="modal-footer">
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
        <a href="#" class="btn" onclick="closeModal('modal1')">Cerrar</a>
      </div>
    </div>
  </div>

  <div id="modal2" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal2')">&times;</span>
      <div class="modal-header">
        <img src="https://i.ibb.co/LX90w1L1/FB-IMG-1763240283155.jpg" alt="Excel Course">
        <h2>Curso Completo de Excel Profesional + IA</h2>
      </div>
      <div class="modal-body">
        <p>¡Domina la herramienta más utilizada en oficinas, empresas y despachos profesionales! Aprende Excel desde lo básico hasta lo avanzado, con integración de IA para automatización, análisis predictivo y generación de soluciones en segundos.</p>
        <p><strong>Temas:</strong> Fórmulas profesionales, tablas dinámicas, dashboards, macros, automatización con IA.</p>
        <p><strong>Incluye:</strong> Certificación profesional, ejercicios prácticos, plantillas descargables, soporte 24/7.</p>
      </div>
      <div class="modal-footer">
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
        <a href="#" class="btn" onclick="closeModal('modal2')">Cerrar</a>
      </div>
    </div>
  </div>

  <div id="modal3" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal3')">&times;</span>
      <div class="modal-header">
        <img src="https://i.ibb.co/PGM3T2MS/FB-IMG-1763240311451.jpg" alt="Photoshop Course">
        <h2>Curso Completo de Photoshop Profesional + IA</h2>
      </div>
      <div class="modal-body">
        <p>¡Domina el programa líder en edición digital, retoque y presentación profesional! Aprende Photoshop desde lo básico hasta nivel avanzado, integrando IA para agilizar flujos, generar imágenes y mejorar presentaciones.</p>
        <p><strong>Aplicado a arquitectura:</strong> Postproducción de renders, láminas arquitectónicas, composición de escenas urbanas, corrección de perspectiva.</p>
        <p><strong>Incluye:</strong> Certificación profesional, material descargable, soporte continuo.</p>
      </div>
      <div class="modal-footer">
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
        <a href="#" class="btn" onclick="closeModal('modal3')">Cerrar</a>
      </div>
    </div>
  </div>

  <div id="modal4" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal4')">&times;</span>
      <div class="modal-header">
        <img src="https://i.ibb.co/Vk3zGMc/FB-IMG-1763240198032.jpg" alt="Illustrator Course">
        <h2>Curso Completo de Adobe Illustrator + IA</h2>
      </div>
      <div class="modal-body">
        <p>¡Domina el software líder en diseño vectorial y conviértete en un creador profesional! Aprende Illustrator desde cero hasta nivel avanzado, integrando IA para acelerar tu flujo de trabajo, generar ideas y transformar conceptos en arte listo para imprimir.</p>
        <p><strong>Temas:</strong> Diseño vectorial, ilustración digital, branding, empaques, preparación de archivos para imprenta.</p>
        <p><strong>Incluye:</strong> Certificación profesional, plantillas, recursos premium, soporte 24/7.</p>
      </div>
      <div class="modal-footer">
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
        <a href="#" class="btn" onclick="closeModal('modal4')">Cerrar</a>
      </div>
    </div>
  </div>

  <div id="modal5" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal5')">&times;</span>
      <div class="modal-header">
        <img src="https://i.ibb.co/7LQk13m/FB-IMG-1763240367547.jpg" alt="SketchUp Course">
        <h2>Curso de SketchUp + V-Ray + Photoshop + IA</h2>
      </div>
      <div class="modal-body">
        <p>¡Da vida a tus ideas y crea presentaciones visuales impactantes! Aprende a modelar, renderizar y presentar proyectos 3D con calidad profesional, utilizando SketchUp, V-Ray y Photoshop, integrando IA para optimizar materiales, iluminación y escenas.</p>
        <p><strong>Incluye:</strong> Metodología práctica, certificación profesional, material actualizado, soporte continuo.</p>
      </div>
      <div class="modal-footer">
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
        <a href="#" class="btn" onclick="closeModal('modal5')">Cerrar</a>
      </div>
    </div>
  </div>

  <div id="modal6" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal6')">&times;</span>
      <div class="modal-header">
        <img src="https://i.ibb.co/ccJ8sJ7r/FB-IMG-1763240198032.jpg" alt="AutoCAD Course">
        <h2>Curso de AutoCAD 2D Básico – Avanzado + IA</h2>
      </div>
      <div class="modal-body">
        <p>¡Domina AutoCAD desde cero hasta un nivel profesional! Aprende a diseñar planos arquitectónicos, estructurales y técnicos con precisión, eficiencia y calidad, integrando IA para optimizar tareas repetitivas y potenciar tu productividad.</p>
        <p><strong>Temas:</strong> Comandos esenciales, capas, bloques, acotación, layouts, automatización con IA.</p>
        <p><strong>Incluye:</strong> Certificación profesional, instructores certificados, soporte 24/7.</p>
      </div>
      <div class="modal-footer">
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
        <a href="#" class="btn" onclick="closeModal('modal6')">Cerrar</a>
      </div>
    </div>
  </div>

  <div id="modal7" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal7')">&times;</span>
      <div class="modal-header">
        <img src="https://i.ibb.co/FbhWzqJ8/FB-IMG-1763240367547.jpg" alt="Revit Course">
        <h2>Curso Completo de Revit + BIM con IA</h2>
      </div>
      <div class="modal-body">
        <p>¡Domina el software que está revolucionando el diseño y la construcción! Aprende Revit de forma completa y profesional, abarcando Architecture, Structure, MEP y BIM, integrando IA para automatizar procesos, optimizar modelos y aumentar tu productividad.</p>
        <p><strong>Temas:</strong> Modelado BIM, familias paramétricas, coordinación entre disciplinas, documentación técnica, clash detection.</p>
        <p><strong>Incluye:</strong> Certificación profesional, instructores con experiencia real, metodología práctica.</p>
      </div>
      <div class="modal-footer">
        <a href="https://wa.me/525519192522" class="btn" target="_blank">Contáctanos</a>
        <a href="#" class="btn" onclick="closeModal('modal7')">Cerrar</a>
      </div>
    </div>
  </div>

  <!-- POR QUÉ ELEGIRNOS -->
  <section style="background-color: var(--gris-claro);">
    <div class="container">
      <h2 class="section-title">¿Por qué elegirnos?</h2>
      <div class="beneficios">
        <div>🎓 Certificación profesional con valor curricular</div>
        <div>👨‍🏫 Instructores con experiencia real en obra y diseño</div>
        <div>🤖 IA integrada en todos los cursos</div>
        <div>📚 Material descargable y ejercicios reales</div>
        <div>💬 Soporte continuo, incluso después del curso</div>
        <div>💼 Enfoque 100% práctico</div>
      </div>
    </div>
  </section>

  <!-- SOBRE NOSOTROS -->
  <section id="nosotros" class="container">
    <h2 class="section-title">Sobre Nosotros</h2>
    <p style="text-align: center; max-width: 800px; margin: 0 auto;">
      Somos un equipo de arquitectos y diseñadores apasionados por la innovación, la enseñanza y la tecnología.  
      Fundado por <strong>Adrián Elichel Arq.</strong>, SAIE nace con el objetivo de empoderar a nuevos profesionales con las herramientas que el mercado exige hoy: diseño técnico, visualización 3D e <strong>Inteligencia Artificial</strong>.<br><br>
      No enseñamos solo software: enseñamos soluciones reales para proyectos reales.
    </p>
  </section>

  <!-- CONTACTO -->
  <section id="contacto" class="container">
    <h2 class="section-title">Contáctanos</h2>
    <div class="contacto-grid">
      <div class="contacto-info">
        <h3>📍 Dirección</h3>
        <p>Av. Río Churubusco 344, Granjas México, Iztacalco<br>08400 Ciudad de México, CDMX, México</p>
        <h3>📞 Teléfonos</h3>
        <p>Adrián Elichel Arq.: <strong>55 1919 2522</strong><br>José Valencia: <strong>55 6248 2314</strong></p>
        <h3>📧 Redes</h3>
        <p><a href="https://www.facebook.com/share/1ABJrDALaR/" target="_blank">Facebook</a></p>
      </div>
      <div class="contacto-form">
        <form action="https://formsubmit.co/tuemail@dominio.com" method="POST">
          <input type="text" name="nombre" placeholder="Nombre" required>
          <input type="email" name="email" placeholder="Correo electrónico" required>
          <input type="tel" name="telefono" placeholder="Teléfono">
          <select name="curso">
            <option value="">Curso de interés</option>
            <option value="IA">Inteligencia Artificial</option>
            <option value="Excel+IA">Excel + IA</option>
            <option value="Photoshop+IA">Photoshop + IA</option>
            <option value="Illustrator+IA">Illustrator + IA</option>
            <option value="SketchUp+Vray">SketchUp + V-Ray + IA</option>
            <option value="AutoCAD+IA">AutoCAD + IA</option>
            <option value="Revit+BIM">Revit + BIM + IA</option>
          </select>
          <textarea name="mensaje" rows="4" placeholder="Mensaje"></textarea>
          <button type="submit" class="btn">Enviar</button>
        </form>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="container">
      <div class="logo">
        <img src="https://i.ibb.co/tTQf3kdQ/adriax-chelele-v.jpg" alt="SAIE - Soluciones Arquitectónicas e Innovación de Espacios">
      </div>
      <p>Donde la arquitectura se encuentra con el futuro.</p>
      <p>© 2025 SAIE — Todos los derechos reservados</p>
      <p>
        <a href="https://www.facebook.com/share/1ABJrDALaR/" target="_blank">Facebook</a>
      </p>
    </div>
  </footer>

  <script>
    function openModal(id) {
      document.getElementById(id).style.display = "block";
    }

    function closeModal(id) {
      document.getElementById(id).style.display = "none";
    }

    window.onclick = function(event) {
      const modals = document.getElementsByClassName('modal');
      for (let i = 0; i < modals.length; i++) {
        if (event.target == modals[i]) {
          modals[i].style.display = "none";
        }
      }
    }
  </script>

</body>
</html>
