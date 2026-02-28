<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Majestic Soul Events | Dando a luz tus mejores momentos</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --gold-primary: #D4AF37;
            --gold-light: #F4E8C1;
            --gold-dark: #B8941F;
            --navy: #0A1628;
            --navy-light: #1A2B47;
            --white: #FFFFFF;
            --            --white: #FFFFFF;
            --cream: #F9F6F0;
        }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--navy);
            color: var(--white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navegación */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 22, 40, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 5%;
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            transition: all 0.3s ease;
        }

        nav.scrolled {
            padding: 0.5rem 5%;
            box-shadow: 0 5px 30px rgba(212, 175, 55, 0.1);
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-nav {
            height: 60px;
            filter: drop-shadow(0 0 10px rgba(212, 175, 55, 0.3));
            transition: transform 0.3s ease;
        }

        .logo-nav:hover {
            transform: scale(1.05);
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--gold-light);
            text-decoration: none;
            font-weight: 400;
            letter-spacing: 1px;
            position: relative;
            transition: color 0.3s ease;
            font-size: 0.95rem;
            text-transform: uppercase;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 1px;
            background: var(--gold-primary);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--gold-primary);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.1) 0%, transparent 70%);
            animation: pulse 15s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }

        .hero-content {
            text-align: center;
            z-index: 2;
            padding: 2rem;
            max-width: 900px;
        }

        .logo-hero {
            width: 350px;
            max-width: 90%;
            margin-bottom: 2rem;
            filter: drop-shadow(0 10px 40px rgba(0,0,0,0.5));
            animation: fadeInDown 1s ease;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            color: var(--gold-primary);
            margin-bottom: 1rem;
            letter-spacing: 3px;
            animation: fadeInUp 1s ease 0.3s both;
        }

        .hero .tagline {
            font-size: 1.5rem;
            color: var(--gold-light);
            font-style: italic;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.5s both;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 3rem;
            background: transparent;
            color: var(--gold-primary);
            border: 2px solid var(--gold-primary);
            text-decoration: none;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            animation: fadeInUp 1s ease 0.7s both;
        }

        .cta-button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: var(--gold-primary);
            transition: left 0.4s ease;
            z-index: -1;
        }

        .cta-button:hover {
            color: var(--navy);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
        }

        .cta-button:hover::before {
            left: 0;
        }

        /* Sección Servicios */
        .services {
            padding: 6rem 5%;
            background: var(--cream);
            color: var(--navy);
        }

        .section-title {
            text-align: center;
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            color: var(--navy);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background: var(--gold-primary);
            margin: 1rem auto 0;
        }

        .section-subtitle {
            text-align: center;
            color: #666;
            font-size: 1.1rem;
            margin-bottom: 4rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .services-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }

        .service-card {
            background: var(--white);
            padding: 3rem 2rem;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.08);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(212, 175, 55, 0.1);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--gold-primary), var(--gold-dark));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.4s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            color: var(--gold-primary);
        }

        .service-card h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--navy);
        }

        .service-card p {
            color: #666;
            line-height: 1.8;
        }

        /* Sección Nosotros */
        .about {
            padding: 6rem 5%;
            background: var(--navy);
            position: relative;
            overflow: hidden;
        }

        .about::before {
            content: '';
            position: absolute;
            right: -10%;
            top: -10%;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(212, 175, 55, 0.05) 0%, transparent 70%);
            border-radius: 50%;
        }

        .about-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .about-content h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            color: var(--gold-primary);
            margin-bottom: 1.5rem;
        }

        .about-content p {
            color: #ccc;
            font-size: 1.1rem;
            line-height: 1.9;
            margin-bottom: 1.5rem;
        }

        .about-image {
            position: relative;
        }

        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            border: 2px solid rgba(212, 175, 55, 0.3);
        }

        .about-image::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            right: 20px;
            bottom: 20px;
            border: 2px solid var(--gold-primary);
            border-radius: 10px;
            z-index: -1;
        }

        /* Galería */
        .gallery {
            padding: 6rem 5%;
            background: linear-gradient(to bottom, var(--cream), var(--white));
        }

        .gallery-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 1.5rem;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            height: 400px;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .gallery-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to top, rgba(10, 22, 40, 0.9), transparent);
            display: flex;
            align-items: flex-end;
            padding: 2rem;
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        .gallery-overlay h4 {
            color: var(--gold-primary);
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
        }

        /* Contacto */
        .contact {
            padding: 6rem 5%;
            background: var(--navy);
            position: relative;
        }

        .contact-container {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            color: var(--gold-primary);
            margin-bottom: 2rem;
        }

        .contact-detail {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
            color: #ccc;
            font-size: 1.1rem;
        }

        .contact-detail span {
            color: var(--gold-primary);
            font-size: 1.3rem;
        }

        .contact-detail a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .contact-detail a:hover {
            color: var(--gold-primary);
        }

        .contact-form {
            background: rgba(255,255,255,0.03);
            padding: 3rem;
            border-radius: 10px;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            color: var(--gold-light);
            margin-bottom: 0.5rem;
            font-weight: 300;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(212, 175, 55, 0.3);
            color: var(--white);
            border-radius: 5px;
            font-family: 'Lato', sans-serif;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--gold-primary);
            background: rgba(255,255,255,0.08);
        }

        .submit-btn {
            width: 100%;
            padding: 1rem;
            background: var(--gold-primary);
            color: var(--navy);
            border: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-radius: 5px;
        }

        .submit-btn:hover {
            background: var(--gold-light);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.2);
        }

        /* Footer */
        footer {
            background: #050a12;
            padding: 3rem 5%;
            text-align: center;
            border-top: 1px solid rgba(212, 175, 55, 0.2);
        }

        .footer-logo {
            height: 80px;
            margin-bottom: 1.5rem;
            opacity: 0.8;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .social-links a {
            color: var(--gold-primary);
            font-size: 1.5rem;
            transition: all 0.3s ease;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid rgba(212, 175, 55, 0.3);
            border-radius: 50%;
            text-decoration: none;
        }

        .social-links a:hover {
            background: var(--gold-primary);
            color: var(--navy);
            transform: translateY(-3px);
        }

        .footer-text {
            color: #666;
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 968px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .about-container,
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .about-image {
                order: -1;
            }
        }

        /* Animación de scroll */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>

    <!-- Navegación -->
    <nav id="navbar">
        <div class="nav-container">
            <img src="/mnt/kimi/upload/1000446210.jpg" alt="Majestic Soul Events" class="logo-nav">
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#galeria">Galería</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <img src="/mnt/kimi/upload/1000446210.jpg" alt="Majestic Soul Events Logo" class="logo-hero">
            <h1>Majestic Soul Events</h1>
            <p class="tagline">"Dando a luz tus mejores momentos"</p>
            <a href="#contacto" class="cta-button">Planifica tu Evento</a>
        </div>
    </section>

    <!-- Servicios -->
    <section class="services" id="servicios">
        <h2 class="section-title">Nuestros Servicios</h2>
        <p class="section-subtitle">Creamos experiencias inolvidables con atención meticulosa a cada detalle</p>
        
        <div class="services-grid">
            <div class="service-card fade-in">
                <div class="service-icon">💍</div>
                <h3>Bodas</h3>
                <p>Transformamos tu día especial en un cuento de hadas. Desde la ceremonia hasta la recepción, cuidamos cada detalle para que solo te preocupes de decir "sí, quiero".</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">🎉</div>
                <h3>Eventos Corporativos</h3>
                <p>Conferencias, lanzamientos de productos y cenas de gala. Elevamos la imagen de tu empresa con eventos que impresionan y conectan.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">🎂</div>
                <h3>Fiestas Privadas</h3>
                <p>Cumpleaños, aniversarios, graduaciones y celebraciones íntimas. Diseñamos ambientes únicos que reflejan tu personalidad y estilo.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">🎭</div>
                <h3>Eventos Temáticos</h3>
                <p>Desde elegantes veladas de gala hasta fiestas vintage. Creamos universos completos donde cada elemento cuenta una historia.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">🎵</div>
                <h3>Entretenimiento</h3>
                <p>Selección de DJs, bandas en vivo, performers y artistas. La música y el espectáculo perfectos para cada momento.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">✨</div>
                <h3>Decoración & Ambientación</h3>
                <p>Diseño floral, iluminación arquitectónica y montajes espectaculares. Convertimos espacios ordinarios en escenarios majestuosos.</p>
            </div>
        </div>
    </section>

    <!-- Nosotros -->
    <section class="about" id="nosotros">
        <div class="about-container">
            <div class="about-content fade-in">
                <h2>Una Historia de Pasión y Elegancia</h2>
                <p>En Majestic Soul Events creemos que cada celebración es una oportunidad para crear recuerdos eternos. Nacimos de la pasión por transformar momentos ordinarios en experiencias extraordinarias.</p>
                <p>Nuestro equipo de profesionales combina creatividad, organización impecable y un ojo agudo para los detalles. No solo planeamos eventos; diseñamos emociones, creamos atmósferas y damos vida a tus sueños.</p>
                <p>Con años de experiencia en la industria, hemos tenido el privilegio de ser parte de cientos de historias de amor, éxito y celebración. Cada evento es único, cada cliente es especial, y cada momento merece ser majestuoso.</p>
            </div>
            <div class="about-image fade-in">
                <img src="https://images.unsplash.com/photo-1519167758481-83f550bb49b3?w=800&q=80" alt="Evento elegante">
            </div>
        </div>
    </section>

    <!-- Galería -->
    <section class="gallery" id="galeria">
        <h2 class="section-title">Galería de Momentos</h2>
        <p class="section-subtitle">Un vistazo a nuestras creaciones más memorables</p>
        
        <div class="gallery-grid">
            <div class="gallery-item fade-in">
                <img src="https://images.unsplash.com/photo-1519741497674-611481863552?w=800&q=80" alt="Boda elegante">
                <div class="gallery-overlay">
                    <h4>Boda en Jardín</h4>
                </div>
            </div>
            
            <div class="gallery-item fade-in">
                <img src="https://images.unsplash.com/photo-1511578314322-379afb476865?w=800&q=80" alt="Evento corporativo">
                <div class="gallery-overlay">
                    <h4>Gala Corporativa</h4>
                </div>
            </div>
            
            <div class="gallery-item fade-in">
                <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?w=800&q=80" alt="Decoración">
                <div class="gallery-overlay">
                    <h4>Cena de Aniversario</h4>
                </div>
            </div>
            
            <div class="gallery-item fade-in">
                <img src="https://images.unsplash.com/photo-1478146896981-b80c463ab360?w=800&q=80" alt="Celebración">
                <div class="gallery-overlay">
                    <h4>Fiesta de Cumpleaños</h4>
                </div>
            </div>
            
            <div class="gallery-item fade-in">
                <img src="https://images.unsplash.com/photo-1464366400600-7168b8af9bc3?w=800&q=80" alt="Mesa decorada">
                <div class="gallery-overlay">
                    <h4>Decoración Floral</h4>
                </div>
            </div>
            
            <div class="gallery-item fade-in">
                <img src="https://images.unsplash.com/photo-1505236858219-8359eb29e329?w=800&q=80" alt="Iluminación">
                <div class="gallery-overlay">
                    <h4>Iluminación Ambiental</h4>
                </div>
            </div>
        </div>
    </section>

    <!-- Contacto -->
    <section class="contact" id="contacto">
        <h2 class="section-title" style="color: var(--gold-primary); margin-bottom: 3rem;">Comencemos tu Historia</h2>
        
        <div class="contact-container">
            <div class="contact-info fade-in">
                <h3>Información de Contacto</h3>
                
                <!-- DIRECCIÓN ACTUALIZADA -->
                <div class="contact-detail">
                    <span>📍</span>
                    <p>David, Chiriquí, Panamá</p>
                </div>
                
                <!-- TELÉFONO ACTUALIZADO - CLICKEABLE -->
                <div class="contact-detail">
                    <span>📞</span>
                    <p><a href="tel:+50762271617">+507 6227-1617</a></p>
                </div>
                
                <!-- EMAIL ACTUALIZADO - CLICKEABLE -->
                <div class="contact-detail">
                    <span>✉️</span>
                    <p><a href="mailto:majesticsoulevents@gmail.com">majesticsoulevents@gmail.com</a></p>
                </div>
                
                <!-- HORARIO ACTUALIZADO -->
                <div class="contact-detail">
                    <span>🕐</span>
                    <p>Lunes a Domingo: 8:00 AM - 9:30 PM</p>
                </div>
                
            </div>
            
            <div class="contact-form fade-in">
                <form>
                    <div class="form-group">
                        <label>Nombre completo</label>
                        <input type="text" placeholder="Tu nombre" required>
                    </div>
                    <div class="form-group">
                        <label>Correo electrónico</label>
                        <input type="email" placeholder="tu@email.com" required>
                    </div>
                    <div class="form-group">
                        <label>Tipo de evento</label>
                        <input type="text" placeholder="Boda, cumpleaños, corporativo...">
                    </div>
                    <div class="form-group">
                        <label>Fecha estimada</label>
                        <input type="date">
                    </div>
                    <div class="form-group">
                        <label>Cuéntanos tu visión</label>
                        <textarea rows="4" placeholder="Describe tu evento soñado..."></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Enviar Mensaje</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <img src="/mnt/kimi/upload/1000446210.jpg" alt="Majestic Soul Events" class="footer-logo">
        
        <!-- REDES SOCIALES ACTUALIZADAS -->
        <div class="social-links">
            <a href="https://www.instagram.com/majesticsoulevents?igsh=MWQwZWVzeWN6bGJ2ag==" target="_blank" title="Instagram">📸</a>
            <a href="https://wa.me/50762271617" target="_blank" title="WhatsApp">💬</a>
            <a href="mailto:majesticsoulevents@gmail.com" title="Email">✉️</a>
        </div>
        
        <p class="footer-text">© 2026 Majestic Soul Events. Todos los derechos reservados.<br>
        "Dando a luz tus mejores momentos"</p>
    </footer>

    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Fade in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: "0px 0px -50px 0px"
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
    </script>

</body>
</html>
