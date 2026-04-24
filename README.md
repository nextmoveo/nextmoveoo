
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NEXTMOVE - Umzüge & Transport in Deutschland</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(15, 23, 42, 0.95);
            padding: 1rem 2rem;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            text-decoration: none;
        }

        .logo img {
            height: 40px;
            width: auto;
        }

        .logo-text {
            color: #22c55e;
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #22c55e;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            background: linear-gradient(rgba(15, 23, 42, 0.8), rgba(15, 23, 42, 0.9)),
                        url('imgs/furniture_movers_nextmove.png');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            padding: 6rem 2rem 2rem;
        }

        .hero-content {
            max-width: 800px;
            color: white;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2rem;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: #22c55e;
            color: white;
        }

        .btn-primary:hover {
            background: #16a34a;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid white;
            color: white;
        }

        .btn-secondary:hover {
            background: white;
            color: #0f172a;
        }

        /* Stats */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            padding: 4rem 2rem;
            background: #f8fafc;
        }

        .stat {
            text-align: center;
            padding: 2rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: #22c55e;
        }

        .stat-label {
            color: #64748b;
            margin-top: 0.5rem;
        }

        /* Features */
        .features {
            background: #22c55e;
            padding: 4rem 2rem;
            color: white;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .feature {
            text-align: center;
            padding: 1.5rem;
        }

        .feature h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        /* Services */
        .services {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 1rem;
            color: #0f172a;
            font-size: 2.5rem;
        }

        .section-subtitle {
            text-align: center;
            color: #64748b;
            margin-bottom: 3rem;
            font-size: 1.2rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: white;
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .service-icon {
            width: 60px;
            height: 60px;
            background: #22c55e;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
            color: white;
            font-size: 1.5rem;
        }

        .service-card h3 {
            margin-bottom: 0.5rem;
            color: #0f172a;
        }

        .service-card p {
            color: #64748b;
            margin-bottom: 1rem;
        }

        .service-price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #22c55e;
        }

        /* Process */
        .process {
            background: #0f172a;
            color: white;
            padding: 4rem 2rem;
        }

        .process-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .process-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-top: 3rem;
        }

        .process-step {
            text-align: center;
        }

        .step-number {
            width: 80px;
            height: 80px;
            background: #22c55e;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: bold;
            margin: 0 auto 1.5rem;
        }

        .process-step h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        .process-step p {
            color: #94a3b8;
        }

        /* Why Us */
        .why-us {
            padding: 4rem 2rem;
            background: #f8fafc;
        }

        .why-us-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .benefits-list {
            list-style: none;
            margin-top: 2rem;
        }

        .benefits-list li {
            padding: 1rem;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .benefits-list li::before {
            content: "✓";
            color: #22c55e;
            font-weight: bold;
            font-size: 1.5rem;
        }

        /* Reviews */
        .reviews {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .review-card {
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .review-text {
            font-style: italic;
            color: #475569;
            margin-bottom: 1.5rem;
        }

        .review-author {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            background: #22c55e;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        .author-info h4 {
            color: #0f172a;
        }

        .author-info span {
            color: #64748b;
            font-size: 0.9rem;
        }

        /* Contact */
        .contact {
            background: #0f172a;
            color: white;
            padding: 4rem 2rem;
        }

        .contact-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }

        .contact-info h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .contact-item {
            margin-bottom: 1.5rem;
        }

        .contact-item h4 {
            color: #22c55e;
            margin-bottom: 0.5rem;
        }

        .contact-item a {
            color: white;
            text-decoration: none;
        }

        .contact-item a:hover {
            color: #22c55e;
        }

        /* Form */
        .contact-form {
            background: #1e293b;
            padding: 2rem;
            border-radius: 12px;
        }

        .form-title {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: white;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #94a3b8;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #334155;
            border-radius: 8px;
            background: #0f172a;
            color: white;
            font-size: 1rem;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #22c55e;
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin: 1.5rem 0;
        }

        .checkbox-group input {
            width: auto;
        }

        .form-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 1.5rem;
        }

        .btn-whatsapp {
            background: #25D366;
            color: white;
            padding: 1rem 1.5rem;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: background 0.3s;
            font-size: 1rem;
        }

        .btn-whatsapp:hover {
            background: #128C7E;
        }

        .btn-email {
            background: #3b82f6;
            color: white;
            padding: 1rem 1.5rem;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: background 0.3s;
            font-size: 1rem;
        }

        .btn-email:hover {
            background: #2563eb;
        }

        /* FAQ */
        .faq {
            padding: 4rem 2rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            background: white;
            border-radius: 8px;
            margin-bottom: 1rem;
            overflow: hidden;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .faq-question {
            padding: 1.5rem;
            background: white;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
        }

        .faq-answer {
            padding: 0 1.5rem 1.5rem;
            color: #64748b;
        }

        .faq-item.active .faq-answer {
            display: block;
        }

        /* Footer */
        footer {
            background: #020617;
            color: #94a3b8;
            padding: 3rem 2rem;
        }

        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .footer-section h3 {
            color: white;
            margin-bottom: 1rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section a {
            color: #94a3b8;
            text-decoration: none;
        }

        .footer-section a:hover {
            color: #22c55e;
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid #1e293b;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            background: white;
            padding: 3rem;
            border-radius: 12px;
            max-width: 500px;
            text-align: center;
            color: #333;
        }

        .modal-content h2 {
            color: #22c55e;
            margin-bottom: 1rem;
        }

        .modal-close {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 2rem;
            cursor: pointer;
            color: #64748b;
        }

        /* Mobile Menu */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Scroll to order button */
        .scroll-to-order {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            background: #22c55e;
            color: white;
            padding: 1rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            box-shadow: 0 4px 15px rgba(34, 197, 94, 0.4);
            z-index: 999;
            display: none;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s;
        }

        .scroll-to-order.visible {
            display: flex;
        }

        .scroll-to-order:hover {
            background: #16a34a;
            transform: translateY(-3px);
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .stats {
                grid-template-columns: 1fr;
            }

            .form-buttons {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <nav>
        <a href="#home" class="logo">
            <img src="imgs/logo.png" alt="NEXTMOVE Logo">
            <span class="logo-text">NEXTMOVE</span>
        </a>
        <div class="nav-links">
            <a href="#home">Startseite</a>
            <a href="#services">Leistungen</a>
            <a href="#process">Ablauf</a>
            <a href="#about">Über uns</a>
            <a href="#reviews">Bewertungen</a>
            <a href="#contact">Kontakt</a>
        </div>
        <button class="mobile-menu-btn">☰</button>
    </nav>

    <!-- Floating Order Button -->
    <a href="#contact" class="scroll-to-order" id="orderBtn">
        📋 Anfrage stellen
    </a>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Über 2.500 erfolgreiche Umzüge</h1>
            <p>Ihr professioneller Partner für Umzüge in Deutschland</p>
            <p>Zuverlässiger Haushaltsumzug, Transport und Einpackservice. Wir kümmern uns um alles – schnell, sicher und zu fairen Preisen.</p>
            <div class="hero-buttons">
                <a href="#contact" class="btn btn-primary">Kostenlose Offerte</a>
                <a href="tel:+4917664008327" class="btn btn-secondary">📞 Anrufen</a>
                <a href="https://wa.me/4917664008327" class="btn btn-secondary">💬 WhatsApp</a>
            </div>
        </div>
    </section>

    <section class="stats">
        <div class="stat">
            <div class="stat-number">2500+</div>
            <div class="stat-label">Zufriedene Kunden</div>
        </div>
        <div class="stat">
            <div class="stat-number">2+</div>
            <div class="stat-label">Jahre Erfahrung</div>
        </div>
        <div class="stat">
            <div class="stat-number">50+</div>
            <div class="stat-label">Städte in Deutschland</div>
        </div>
    </section>

    <section class="features">
        <div class="features-grid">
            <div class="feature">
                <h3>Vollversichert</h3>
                <p>Bis 500.000 €</p>
            </div>
            <div class="feature">
                <h3>24/7 Verfügbar</h3>
                <p>Notfall-Service</p>
            </div>
            <div class="feature">
                <h3>Faire Preise</h3>
                <p>Keine versteckten Kosten</p>
            </div>
            <div class="feature">
                <h3>Professionelles Team</h3>
                <p>Erfahrene Umzugshelfer</p>
            </div>
        </div>
    </section>

    <section class="services" id="services">
        <h2 class="section-title">Unsere Leistungen</h2>
        <p class="section-subtitle">Unsere Transportleistungen</p>
        <p style="text-align: center; color: #64748b; margin-bottom: 3rem;">Professioneller Transport-Service für Ihre Möbel und Büros in ganz Deutschland</p>

        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🚚</div>
                <h3>Möbeltransport</h3>
                <p>Spezialtransport für empfindliche und wertvolle Möbelstücke. Sicher und zuverlässig.</p>
                <div class="service-price">Ab 149 €</div>
            </div>

            <div class="service-card">
                <div class="service-icon">🏢</div>
                <h3>Büroübersiedlung</h3>
                <p>Professionelle Firmenübersiedlung mit minimaler Betriebsunterbrechung.</p>
                <div class="service-price">Individuelles Angebot</div>
            </div>

            <div class="service-card">
                <div class="service-icon">📦</div>
                <h3>Einpackservice</h3>
                <p>Professionelle Verpackung und Sicherung Ihrer Gegenstände. Wir verpacken alles sicher.</p>
                <!-- Price removed as requested -->
            </div>

            <div class="service-card">
                <div class="service-icon">🔧</div>
                <h3>Montage und Demontage</h3>
                <p>Fachmännische Möbelmontage und Demontage. Wir bauen Ihre Möbel sicher ab und auf.</p>
                <!-- Price removed as requested -->
            </div>
        </div>
    </section>

    <section class="process" id="process">
        <div class="process-container">
            <h2 class="section-title" style="color: white;">So funktioniert's</h2>
            <p class="section-subtitle" style="color: #94a3b8;">In 4 einfachen Schritten</p>
            <p style="text-align: center; color: #64748b; margin-bottom: 3rem;">Unser bewährter Prozess macht Ihren Umzug so einfach wie möglich</p>

            <div class="process-grid">
                <div class="process-step">
                    <div class="step-number">01</div>
                    <h3>Kostenlose Beratung</h3>
                    <p>Kontaktieren Sie uns und beschreiben Sie Ihre Anforderungen. Wir beraten Sie kostenlos.</p>
                </div>

                <div class="process-step">
                    <div class="step-number">02</div>
                    <h3>Angebot erhalten</h3>
                    <p>Erhalten Sie innerhalb von 24 Stunden ein transparentes und unverbindliches Angebot.</p>
                </div>

                <div class="process-step">
                    <div class="step-number">03</div>
                    <h3>Der Umzugstag</h3>
                    <p>Unser Team arriveiert pünktlich und führt den Umzug professionell durch.</p>
                </div>

                <div class="process-step">
                    <div class="step-number">04</div>
                    <h3>Zufriedenheit</h3>
                    <p>Wir verlassen erst, wenn Sie 100% zufrieden sind. Ihre Zufriedenheit ist unser Ziel.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="why-us" id="about">
        <div class="why-us-container">
            <h2 class="section-title">Warum NEXTMOVE?</h2>
            <p class="section-subtitle">Vertrauen Sie den Experten</p>
            <p style="text-align: center; color: #475569; margin-bottom: 2rem;">
                Mit über 2 Jahren Erfahrung und mehr als 2.500 erfolgreichen Umzügen sind wir Ihr zuverlässiger Partner in ganz Deutschland. Unser engagiertes Team sorgt dafür, dass Ihr Umzug reibungslos und stressfrei abläuft.
            </p>

            <ul class="benefits-list">
                <li>Festpreis-Garantie – keine Überraschungen</li>
                <li>Feste Zeitfenster – Pünktlichkeit garantiert</li>
                <li>Eigene LKWs – keine Subunternehmer</li>
                <li>Geschultes Personal – schonender Umgang</li>
                <li>Kostenlose Nachsorge bei Problemen</li>
            </ul>

            <div style="text-align: center; margin-top: 3rem;">
                <a href="#contact" class="btn btn-primary">Termin vereinbaren</a>
            </div>
        </div>
    </section>

    <section class="reviews" id="reviews">
        <h2 class="section-title">Kundenbewertungen</h2>
        <p class="section-subtitle">Das sagen unsere Kunden</p>
        <p style="text-align: center; color: #64748b; margin-bottom: 3rem;">Über 2.500 zufriedene Kunden in ganz Deutschland</p>

        <div class="reviews-grid">
            <div class="review-card">
                <p class="review-text">„Hervorragender Service! Das Team war pünktlich, freundlich und sehr vorsichtig mit unseren Möbeln. Der ganze Umzug war in 4 Stunden erledigt. Absolut empfehlenswert!"</p>
                <div class="review-author">
                    <div class="author-avatar">AM</div>
                    <div class="author-info">
                        <h4>Ahmed M.</h4>
                        <span>Berlin → München</span>
                    </div>
                </div>
            </div>

            <div class="review-card">
                <p class="review-text">„Wir haben den Einpackservice genutzt und waren begeistert. Alle Kartons waren professionell verpackt. Nichts wurde beschädigt. Fairer Preis für exzellenten Service."</p>
                <div class="review-author">
                    <div class="author-avatar">SK</div>
                    <div class="author-info">
                        <h4>Sarah K.</h4>
                        <span>Hamburg → Frankfurt</span>
                    </div>
                </div>
            </div>

            <div class="review-card">
                <p class="review-text">„Perfekte Organisation von Anfang bis Ende. Die Beratung war kompetent, das Angebot transparent. Beim Umzug selbst war alles genau wie besprochen. Top!"</p>
                <div class="review-author">
                    <div class="author-avatar">MH</div>
                    <div class="author-info">
                        <h4>Mohammed H.</h4>
                        <span>Köln → Stuttgart</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="contact-container">
            <div class="contact-info">
                <h2>Jetzt anfragen</h2>
                <p style="color: #94a3b8; margin-bottom: 2rem;">Kostenlose Offerte einholen</p>
                <p style="color: #64748b; margin-bottom: 2rem;">Füllen Sie das Formular aus und erhalten Sie innerhalb von 24 Stunden Ihr persönliches Angebot. Unverbindlich und kostenlos.</p>

                <div class="contact-item">
                    <h4>Hauptsitz</h4>
                    <p>Kuhstr. 15<br>47906 Kempen, Deutschland</p>
                </div>

                <div class="contact-item">
                    <h4>Zweite Niederlassung</h4>
                    <p>Großgartacher Straße 226<br>74080 Heilbronn, Deutschland</p>
                </div>

                <div class="contact-item">
                    <h4>E-Mail</h4>
                    <a href="mailto:nextmove77ii@gmail.com">nextmove77ii@gmail.com</a>
                </div>

                <div class="contact-item">
                    <h4>WhatsApp & Telefon</h4>
                    <a href="https://wa.me/4917664008327">+49 176 640 08327</a><br>
                    <a href="tel:+4917664008327">📞 Jetzt anrufen</a>
                </div>

                <div class="contact-item">
                    <h4>Öffnungszeiten</h4>
                    <p>Täglich: 08:00 - 21:00<br>Notfall: 24/7</p>
                </div>

                <div class="contact-item">
                    <h4>Folgen Sie uns</h4>
                    <div style="display: flex; gap: 1rem; margin-top: 0.5rem;">
                        <a href="https://www.instagram.com/omarwassouf8?igsh=ajExMDI0dHlwd3dj" target="_blank" style="color: #E1306C; font-size: 1.5rem;">
                            <svg width="28" height="28" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                        </a>
                        <a href="https://www.facebook.com/share/1GQUpcCfyH/" target="_blank" style="color: #1877F2; font-size: 1.5rem;">
                            <svg width="28" height="28" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                            </svg>
                        </a>
                    </div>
                </div>
            </div>

            <form class="contact-form" id="contactForm">
                <h3 class="form-title">Anfrageformular</h3>
                <p style="color: #94a3b8; margin-bottom: 1.5rem; font-size: 0.9rem;">* Pflichtfelder</p>

                <div class="form-group">
                    <label for="name">Vollständiger Name *</label>
                    <input type="text" id="name" name="name" required>
                </div>

                <div class="form-group">
                    <label for="phone">Telefonnummer *</label>
                    <input type="tel" id="phone" name="phone" required>
                </div>

                <div class="form-group">
                    <label for="email">E-Mail-Adresse *</label>
                    <input type="email" id="email" name="email" required>
                </div>

                <div class="form-group">
                    <label for="pickup">Abholadresse *</label>
                    <input type="text" id="pickup" name="pickup" required>
                </div>

                <div class="form-group">
                    <label for="destination">Zieladresse *</label>
                    <input type="text" id="destination" name="destination" required>
                </div>

                <div class="form-group">
                    <label for="date">Wunschdatum *</label>
                    <input type="date" id="date" name="date" required>
                </div>

                <div class="form-group">
                    <label for="time">Uhrzeit *</label>
                    <select id="time" name="time" required>
                        <option value="">Bitte wählen</option>
                        <option value="08:00 - 12:00">08:00 - 12:00</option>
                        <option value="12:00 - 16:00">12:00 - 16:00</option>
                        <option value="16:00 - 20:00">16:00 - 20:00</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="size">Wohnungsgröße *</label>
                    <select id="size" name="size" required>
                        <option value="">Bitte wählen</option>
                        <option value="1 Zimmer">1 Zimmer</option>
                        <option value="2 Zimmer">2 Zimmer</option>
                        <option value="3 Zimmer">3 Zimmer</option>
                        <option value="4 Zimmer">4 Zimmer</option>
                        <option value="5+ Zimmer">5+ Zimmer</option>
                        <option value="Büro/Gewerbe">Büro/Gewerbe</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="service">Gewünschte Leistung *</label>
                    <select id="service" name="service" required>
                        <option value="">Bitte wählen</option>
                        <option value="Möbeltransport">Möbeltransport</option>
                        <option value="Büroübersiedlung">Büroübersiedlung</option>
                        <option value="Einpackservice">Einpackservice</option>
                        <option value="Montage und Demontage">Montage und Demontage</option>
                        <option value="Komplettumzug">Komplettumzug</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="notes">Zusätzliche Anmerkungen</label>
                    <textarea id="notes" name="notes" rows="4"></textarea>
                </div>

                <div class="checkbox-group">
                    <input type="checkbox" id="privacy" name="privacy" required>
                    <label for="privacy">Ich stimme der Datenschutzerklärung zu *</label>
                </div>

                <div class="form-buttons">
                    <button type="submit" class="btn-whatsapp" onclick="submitViaWhatsApp()">
                        💬 Anfrage per WhatsApp senden
                    </button>
                    <button type="button" class="btn-email" onclick="submitViaEmail()">
                        ✉️ Per E-Mail senden
                    </button>
                </div>
            </form>
        </div>
    </section>

    <section class="faq">
        <h2 class="section-title">Häufige Fragen</h2>
        <p class="section-subtitle">Noch Fragen?</p>

        <div class="faq-item">
            <div class="faq-question">
                Wie viel kostet ein Umzug durchschnittlich?
                <span>+</span>
            </div>
            <div class="faq-answer">
                Die Kosten variieren je nach Wohnungsgröße und Entfernung. Ein durchschnittlicher Umzug einer 3-Zimmer-Wohnung kostet zwischen 400€ und 800€. Wir erstellen Ihnen gerne ein individuelles, unverbindliches Angebot.
            </div>
        </div>

        <div class="faq-item">
            <div class="faq-question">
                Wie lang im Voraus sollte ich buchen?
                <span>+</span>
            </div>
            <div class="faq-answer">
                Wir empfehlen mindestens 2-4 Wochen Vorlaufzeit, besonders in den beliebten Umzugsmonaten Mai-September. Für kurzfristige Umzüge sind wir jedoch auch flexibel verfügbar.
            </div>
        </div>

        <div class="faq-item">
            <div class="faq-question">
                Sind meine Sachen versichert?
                <span>+</span>
            </div>
            <div class="faq-answer">
                Ja, alle unsere Umzüge sind bis 500.000€ Vollkasko-versichert. Zusätzlich bieten wir auf Wunsch eine erweiterte Transportversicherung für wertvolle Gegenstände an.
            </div>
        </div>

        <div class="faq-item">
            <div class="faq-question">
                Kann ich auch nur bestimmte Leistungen buchen?
                <span>+</span>
            </div>
            <div class="faq-answer">
                Absolut! Sie können einzelne Services wie Nur-Transport, Einpackservice oder Einlagerung separat buchen. Kontaktieren Sie uns für ein maßgeschneidertes Angebot.
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-container">
            <div class="footer-section">
                <h3>NEXTMOVE</h3>
                <p>NEXTMOVE - Ihre professionelle Umzugsfirma in Deutschland. Seit über 2 Jahren bieten wir erstklassigen Umzugsservice für Privatkunden und Unternehmen.</p>
            </div>

            <div class="footer-section">
                <h3>Leistungen</h3>
                <ul>
                    <li><a href="#services">Haushaltsumzug</a></li>
                    <li><a href="#services">Einpackservice</a></li>
                    <li><a href="#services">Einlagerung</a></li>
                    <li><a href="#services">Büroübersiedlung</a></li>
                    <li><a href="#services">Möbeltransport</a></li>
                    <li><a href="#services">Montage und Demontage</a></li>
                </ul>
            </div>

            <div class="footer-section">
                <h3>Service</h3>
                <ul>
                    <li><a href="#process">Ablauf</a></li>
                    <li><a href="#about">Über uns</a></li>
                    <li><a href="#reviews">Bewertungen</a></li>
                    <li><a href="#contact">Kontakt</a></li>
                    <li><a href="#faq">FAQ</a></li>
                </ul>
            </div>

            <div class="footer-section">
                <h3>Kontakt</h3>
                <ul>
                    <li>Kuhstr. 15, 47906 Kempen</li>
                    <li>Großgartacher Str. 226, 74080 Heilbronn</li>
                    <li><a href="mailto:nextmove77ii@gmail.com">nextmove77ii@gmail.com</a></li>
                    <li><a href="tel:+4917664008327">+49 176 640 08327</a></li>
                    <li>Täglich: 08:00 - 21:00</li>
                </ul>
                <div style="margin-top: 1rem;">
                    <a href="https://www.instagram.com/omarwassouf8?igsh=ajExMDI0dHlwd3dj" target="_blank" style="color: #E1306C; margin-right: 1rem; font-size: 1.2rem;">Instagram</a>
                    <a href="https://www.facebook.com/share/1GQUpcCfyH/" target="_blank" style="color: #1877F2; font-size: 1.2rem;">Facebook</a>
                </div>
            </div>
        </div>

        <div class="copyright">
            <p>© 2026 NEXTMOVE. Alle Rechte vorbehalten.</p>
            <p><a href="#" style="margin: 0 0.5rem;">Impressum</a> | <a href="#" style="margin: 0 0.5rem;">Datenschutz</a> | <a href="#" style="margin: 0 0.5rem;">AGB</a></p>
        </div>
    </footer>

    <!-- Success Modal -->
    <div class="modal" id="successModal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal()">×</span>
            <h2>Anfrage erfolgreich gesendet!</h2>
            <p>Wir werden uns in Kürze bei Ihnen melden.</p>
        </div>
    </div>

    <script>
        // FAQ Toggle
        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', () => {
                const item = question.parentElement;
                item.classList.toggle('active');

                const spans = question.querySelectorAll('span');
                spans.forEach(span => {
                    span.textContent = item.classList.contains('active') ? '−' : '+';
                });
            });
        });

        // Scroll to order button visibility
        window.addEventListener('scroll', () => {
            const orderBtn = document.getElementById('orderBtn');
            if (window.scrollY > 500) {
                orderBtn.classList.add('visible');
            } else {
                orderBtn.classList.remove('visible');
            }
        });

        // Get form data
        function getFormData() {
            return {
                name: document.getElementById('name').value,
                phone: document.getElementById('phone').value,
                email: document.getElementById('email').value,
                pickup: document.getElementById('pickup').value,
                destination: document.getElementById('destination').value,
                date: document.getElementById('date').value,
                time: document.getElementById('time').value,
                size: document.getElementById('size').value,
                service: document.getElementById('service').value,
                notes: document.getElementById('notes').value
            };
        }

        // Validate form
        function validateForm() {
            const form = document.getElementById('contactForm');
            const requiredFields = form.querySelectorAll('[required]');
            let isValid = true;

            requiredFields.forEach(field => {
                if (!field.value.trim()) {
                    field.style.borderColor = '#ef4444';
                    isValid = false;
                } else {
                    field.style.borderColor = '#334155';
                }
            });

            return isValid;
        }

        // Submit via WhatsApp
        function submitViaWhatsApp() {
            if (!validateForm()) {
                alert('Bitte füllen Sie alle Pflichtfelder aus.');
                return;
            }

            const data = getFormData();
            const message = `Neue Anfrage von NEXTMOVE Website:

Name: ${data.name}
Telefon: ${data.phone}
E-Mail: ${data.email}

Abholadresse: ${data.pickup}
Zieladresse: ${data.destination}

Wunschdatum: ${data.date}
Uhrzeit: ${data.time}

Wohnungsgröße: ${data.size}
Gewünschte Leistung: ${data.service}

Zusätzliche Anmerkungen: ${data.notes || 'Keine'}`;

            const whatsappUrl = `https://wa.me/4917664008327?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
        }

        // Submit via Email
        function submitViaEmail() {
            if (!validateForm()) {
                alert('Bitte füllen Sie alle Pflichtfelder aus.');
                return;
            }

            const data = getFormData();
            const subject = 'Neue Anfrage - NEXTMOVE';
            const body = `Neue Anfrage von NEXTMOVE Website:

Name: ${data.name}
Telefon: ${data.phone}
E-Mail: ${data.email}

Abholadresse: ${data.pickup}
Zieladresse: ${data.destination}

Wunschdatum: ${data.date}
Uhrzeit: ${data.time}

Wohnungsgröße: ${data.size}
Gewünschte Leistung: ${data.service}

Zusätzliche Anmerkungen: ${data.notes || 'Keine'}`;

            window.location.href = `mailto:nextmove77ii@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
        }

        // Close modal
        function closeModal() {
            document.getElementById('successModal').classList.remove('active');
        }

        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Mobile menu toggle
        document.querySelector('.mobile-menu-btn').addEventListener('click', () => {
            const navLinks = document.querySelector('.nav-links');
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
    </script>

<script>
/**
 * Iframe 元素高亮注入脚本
 * 需要在目标网站中引入此脚本来支持跨域 iframe 高亮功能
 *
 * 使用方法：
 * 1. 将此脚本添加到目标网站的 HTML 中
 * 2. 或通过浏览器扩展、用户脚本等方式注入
 */

(function () {
  "use strict";

  // 检查是否在 iframe 中
  if (window.self === window.top) {
    return; // 不在 iframe 中，不执行
  }

  // 检查是否已经初始化过
  if (window.__iframeHighlightInitialized) {
    return;
  }
  window.__iframeHighlightInitialized = true;
  console.log("Iframe 高亮脚本已加载");

  // 创建高亮覆盖层
  var overlay = document.createElement("div");
  overlay.id = "iframe-highlight-overlay";
  overlay.style.cssText = "\n    position: fixed;\n    top: 0;\n    left: 0;\n    width: 100vw;\n    height: 100vh;\n    pointer-events: none;\n    z-index: 999999;\n    overflow: hidden;\n  ";

  // 创建悬停高亮框（虚线边框）
  var highlightBox = document.createElement("div");
  highlightBox.id = "iframe-highlight-box";
  highlightBox.style.cssText = "\n    position: absolute;\n    border: 2px dashed #007AFF;\n    background: rgba(0, 122, 255, 0.08);\n    pointer-events: none;\n    display: none;\n    transition: all 0.1s ease;\n    box-shadow: 0 0 0 1px rgba(255, 255, 255, 0.8);\n    border-radius: 2px;\n  ";

  // 创建选中节点的常驻高亮框（实线边框）
  var selectedBox = document.createElement("div");
  selectedBox.id = "iframe-selected-box";
  selectedBox.style.cssText = "\n    position: absolute;\n    border: 2px solid #007AFF;\n    pointer-events: none;\n    display: none;\n    box-shadow: 0 0 0 1px rgba(255, 255, 255, 0.9), 0 0 8px rgba(255, 107, 53, 0.4);\n    border-radius: 2px;\n    z-index: 1000000;\n  ";

  // 创建悬停标签显示
  var tagLabel = document.createElement("div");
  tagLabel.id = "iframe-tag-label";
  tagLabel.style.cssText = "\n    position: absolute;\n    background: #007AFF;\n    color: white;\n    padding: 2px 6px;\n    font-size: 11px;\n    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;\n    border-radius: 2px;\n    pointer-events: none;\n    display: none;\n    white-space: nowrap;\n    z-index: 1000001;\n    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);\n    font-weight: 500;\n  ";

  // 创建选中节点标签
  var selectedLabel = document.createElement("div");
  selectedLabel.id = "iframe-selected-label";
  selectedLabel.style.cssText = "\n    position: absolute;\n    background: #007AFF;\n    color: white;\n    padding: 3px 8px;\n    font-size: 11px;\n    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;\n    border-radius: 3px;\n    pointer-events: none;\n    display: none;\n    white-space: nowrap;\n    z-index: 1000002;\n    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.4);\n    font-weight: 600;\n  ";
  overlay.appendChild(highlightBox);
  overlay.appendChild(selectedBox);
  overlay.appendChild(tagLabel);
  overlay.appendChild(selectedLabel);
  document.body.appendChild(overlay);

  // 存储当前选中的元素
  var selectedElement = null;
  var highlightEnabled = false;

  // 更新选中元素的高亮显示
  function updateSelectedHighlight(element) {
    console.log("updateSelectedHighlight called with:", element);
    if (!element) {
      selectedBox.style.display = "none";
      selectedLabel.style.display = "none";
      selectedElement = null;
      console.log("Cleared selected highlight");
      return;
    }
    selectedElement = element;
    var rect = element.getBoundingClientRect();
    console.log("Selected element rect:", rect);

    // 更新选中高亮框位置
    selectedBox.style.display = "block";
    selectedBox.style.left = "".concat(rect.left - 2, "px");
    selectedBox.style.top = "".concat(rect.top - 2, "px");
    selectedBox.style.width = "".concat(rect.width + 4, "px");
    selectedBox.style.height = "".concat(rect.height + 4, "px");

    // 更新选中标签位置和内容
    selectedLabel.style.display = "block";
    selectedLabel.textContent = "\u2713 <".concat(element.tagName.toLowerCase(), ">");

    // 计算标签位置，确保不超出视窗
    var labelTop = rect.top - 28;
    var labelLeft = rect.left;

    // 如果标签会超出顶部，显示在元素下方
    if (labelTop < 5) {
      labelTop = rect.bottom + 5;
    }

    // 如果标签会超出右侧，向左调整
    var labelWidth = selectedLabel.offsetWidth || 100; // 预估宽度
    if (labelLeft + labelWidth > window.innerWidth - 10) {
      labelLeft = window.innerWidth - labelWidth - 10;
    }
    selectedLabel.style.left = "".concat(Math.max(5, labelLeft), "px");
    selectedLabel.style.top = "".concat(labelTop, "px");
    console.log("Selected highlight positioned at:", {
      left: selectedBox.style.left,
      top: selectedBox.style.top,
      width: selectedBox.style.width,
      height: selectedBox.style.height
    });
  }
  function getElementSelector(element) {
    if (!(element instanceof Element)) throw new Error('Argument must be a DOM element');
    var segments = [];
    var current = element;
    while (current !== document.documentElement) {
      var selector = '';
      // 优先检查唯一ID
      if (current.id && document.querySelectorAll("#".concat(current.id)).length === 1) {
        segments.unshift("#".concat(current.id));
        break; // ID唯一，无需继续向上
      }

      // 生成类名选择器（取第一个有效类名）
      var classes = Array.from(current.classList).filter(function (c) {
        return !c.startsWith('js-');
      });
      var className = classes.length > 0 ? ".".concat(classes[0]) : '';

      // 生成位置索引（nth-child）
      var tag = current.tagName.toLowerCase();
      if (!className) {
        var siblings = Array.from(current.parentNode.children);
        var index = siblings.findIndex(function (el) {
          return el === current;
        }) + 1;
        selector = "".concat(tag, ":nth-child(").concat(index, ")");
      } else {
        selector = className;
      }
      segments.unshift(selector);
      current = current.parentElement;
    }

    // 处理根元素
    if (current === document.documentElement) {
      segments.unshift('html');
    }
    return segments.join(' > ');
  }

  // 获取元素文本内容
  function getElementText(element) {
    var _element$textContent;
    if (element.tagName === "INPUT") {
      return element.value || element.placeholder || "";
    }
    if (element.tagName === "TEXTAREA") {
      return element.value || element.placeholder || "";
    }
    var text = ((_element$textContent = element.textContent) === null || _element$textContent === void 0 ? void 0 : _element$textContent.trim()) || "";
    return text.length > 50 ? text.substring(0, 50) + "..." : text;
  }

  // 获取元素属性信息
  function getElementAttributes(element) {
    var attrs = {};
    for (var i = 0; i < element.attributes.length; i++) {
      var attr = element.attributes[i];
      attrs[attr.name] = attr.value;
    }
    return attrs;
  }

  // 鼠标悬停事件处理
  function handleMouseOver(e) {
    if (!highlightEnabled) return;
    var target = e.target;
    if (!target || target === overlay || target === highlightBox || target === tagLabel || target === selectedBox || target === selectedLabel) {
      return;
    }

    // 避免高亮 html 和 body 元素
    if (target === document.documentElement || target === document.body) {
      return;
    }

    // 如果是已选中的元素，不显示悬停高亮
    if (target === selectedElement) {
      highlightBox.style.display = "none";
      tagLabel.style.display = "none";
      return;
    }
    var rect = target.getBoundingClientRect();
    var selector = getElementSelector(target);
    var text = getElementText(target);
    var attributes = getElementAttributes(target);

    // 更新悬停高亮框位置
    highlightBox.style.display = "block";
    highlightBox.style.left = "".concat(rect.left - 2, "px");
    highlightBox.style.top = "".concat(rect.top - 2, "px");
    highlightBox.style.width = "".concat(rect.width + 4, "px");
    highlightBox.style.height = "".concat(rect.height + 4, "px");

    // 更新标签位置和内容
    tagLabel.style.display = "block";
    tagLabel.textContent = "<".concat(target.tagName.toLowerCase(), ">");

    // 计算标签位置，确保不超出视窗
    var labelTop = rect.top - 22;
    var labelLeft = rect.left;

    // 如果标签会超出顶部，显示在元素下方
    if (labelTop < 0) {
      labelTop = rect.bottom + 5;
    }

    // 如果标签会超出右侧，向左调整
    if (labelLeft + tagLabel.offsetWidth > window.innerWidth) {
      labelLeft = window.innerWidth - tagLabel.offsetWidth - 5;
    }
    tagLabel.style.left = "".concat(Math.max(0, labelLeft), "px");
    tagLabel.style.top = "".concat(labelTop, "px");

    // 发送消息到父窗口
    var elementInfo = {
      tagName: target.tagName.toLowerCase(),
      rect: {
        left: rect.left,
        top: rect.top,
        right: rect.right,
        bottom: rect.bottom,
        width: rect.width,
        height: rect.height,
        x: rect.x,
        y: rect.y
      },
      selector: selector,
      text: text,
      attributes: attributes,
      url: window.location.href,
      path: window.location.pathname,
      timestamp: Date.now()
    };
    try {
      window.parent.postMessage({
        type: "iframe-element-hover",
        data: elementInfo,
        source: "iframe-highlight-injector"
      }, "*");
    } catch (error) {
      console.warn("无法发送消息到父窗口:", error);
    }
  }

  // 鼠标离开事件处理
  function handleMouseOut(e) {
    if (!highlightEnabled) return;
    var relatedTarget = e.relatedTarget;

    // 如果鼠标移动到高亮相关元素上，不隐藏高亮
    if (relatedTarget && (relatedTarget === highlightBox || relatedTarget === tagLabel || relatedTarget === overlay || relatedTarget === selectedBox || relatedTarget === selectedLabel)) {
      return;
    }
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    try {
      window.parent.postMessage({
        type: "iframe-element-hover",
        data: null,
        source: "iframe-highlight-injector"
      }, "*");
    } catch (error) {
      console.warn("无法发送消息到父窗口:", error);
    }
  }

  // 点击事件处理
  function handleClick(e) {
    var target = e.target;
    if (!target || target === overlay || target === highlightBox || target === tagLabel || target === selectedBox || target === selectedLabel) {
      return;
    }

    // 避免处理 html 和 body 元素
    if (target === document.documentElement || target === document.body) {
      return;
    }

    // 检查是否是交互元素，这些元素需要保留默认行为
    var isInteractiveElement = ['input', 'textarea', 'select', 'button', 'a'].includes(target.tagName.toLowerCase());

    // 如果高亮功能启用，对于非交互元素阻止默认行为和事件传播
    if (highlightEnabled) {
      e.preventDefault();
      e.stopPropagation();
    }
    var rect = target.getBoundingClientRect();
    var selector = getElementSelector(target);
    var text = getElementText(target);
    var attributes = getElementAttributes(target);
    console.log("Element clicked:", {
      tagName: target.tagName,
      selector: selector,
      rect: rect
    });

    // 立即更新选中高亮
    updateSelectedHighlight(target);

    // 隐藏悬停高亮，因为现在是选中状态
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    var elementInfo = {
      tagName: target.tagName.toLowerCase(),
      rect: {
        left: rect.left,
        top: rect.top,
        right: rect.right,
        bottom: rect.bottom,
        width: rect.width,
        height: rect.height,
        x: rect.x,
        y: rect.y
      },
      selector: selector,
      text: text,
      attributes: attributes,
      url: window.location.href,
      path: window.location.pathname,
      timestamp: Date.now()
    };
    try {
      window.parent.postMessage({
        type: "iframe-element-click",
        data: elementInfo,
        source: "iframe-highlight-injector"
      }, "*");
    } catch (error) {
      console.warn("无法发送消息到父窗口:", error);
    }
  }

  // 监听来自父窗口的消息
  function handleParentMessage(event) {
    console.log("Received message from parent:", event.data);
    if (event.data.type === "iframe-highlight-toggle") {
      var enabled = event.data.enabled;
      console.log("Highlight toggle:", enabled);
      if (enabled) {
        enableHighlight();
      } else {
        disableHighlight();
      }
    } else if (event.data.type === "enable-iframe-highlight") {
      console.log("Enable iframe highlight");
      enableHighlight();
    } else if (event.data.type === "disable-iframe-highlight") {
      console.log("Disable iframe highlight");
      disableHighlight();
    } else if (event.data.type === "toggle-iframe-highlight") {
      var _enabled = event.data.enabled !== undefined ? event.data.enabled : !highlightEnabled;
      console.log("Toggle iframe highlight to:", _enabled);
      if (_enabled) {
        enableHighlight();
      } else {
        disableHighlight();
      }
    } else if (event.data.type === "update-selected-element") {
      var selector = event.data.selector;
      console.log("Update selected element with selector:", selector);
      if (selector) {
        try {
          var element = document.querySelector(selector);
          console.log("Found element by selector:", element);
          updateSelectedHighlight(element);
        } catch (error) {
          console.warn("Failed to select element:", error);
          updateSelectedHighlight(null);
        }
      } else {
        updateSelectedHighlight(null);
      }
    } else if (event.data.type === "clear-selected-element") {
      console.log("Clear selected element");
      updateSelectedHighlight(null);
    }
  }

  // 启用高亮功能
  function enableHighlight() {
    console.log("Enabling highlight");
    document.addEventListener("mouseover", handleMouseOver, true);
    document.addEventListener("mouseout", handleMouseOut, true);
    document.addEventListener("click", handleClick, true);
    highlightEnabled = true;
    overlay.style.display = "block";
  }

  // 禁用高亮功能
  function disableHighlight() {
    console.log("Disabling highlight");
    highlightEnabled = false;
    // 保持事件监听器，但通过 highlightEnabled 变量控制行为
    // 这样可以保留选中状态的显示
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    // 不隐藏 selectedBox 和 selectedLabel，保留选中状态
  }

  // 完全禁用高亮功能（移除所有监听器）
  function fullyDisableHighlight() {
    console.log("Fully disabling highlight");
    highlightEnabled = false;
    document.removeEventListener("mouseover", handleMouseOver, true);
    document.removeEventListener("mouseout", handleMouseOut, true);
    document.removeEventListener("click", handleClick, true);
    overlay.style.display = "none";
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    selectedBox.style.display = "none";
    selectedLabel.style.display = "none";
  }

  // 添加事件监听
  enableHighlight();
  window.addEventListener("message", handleParentMessage);

  // 暴露全局函数供外部调用
  window.__iframeHighlightControl = {
    enable: enableHighlight,
    disable: disableHighlight,
    fullyDisable: fullyDisableHighlight,
    isEnabled: function isEnabled() {
      return highlightEnabled;
    },
    getSelectedElement: function getSelectedElement() {
      return selectedElement;
    },
    updateSelected: updateSelectedHighlight,
    // 通过消息发送开关控制
    sendToggleMessage: function sendToggleMessage(enabled) {
      window.parent.postMessage({
        type: 'iframe-highlight-status',
        enabled: enabled || highlightEnabled,
        source: 'iframe-highlight-injector'
      }, '*');
    }
  };

  // 通知父窗口脚本已加载
  try {
    window.parent.postMessage({
      type: "iframe-highlight-ready",
      data: {
        url: window.location.href,
        userAgent: navigator.userAgent,
        timestamp: Date.now()
      },
      source: "iframe-highlight-injector"
    }, "*");
  } catch (error) {
    console.warn("无法发送就绪消息到父窗口:", error);
  }

  // 清理函数
  window.__iframeHighlightCleanup = function () {
    fullyDisableHighlight();
    window.removeEventListener("message", handleParentMessage);
    if (overlay.parentElement) {
      overlay.parentElement.removeChild(overlay);
    }
    delete window.__iframeHighlightInitialized;
    delete window.__iframeHighlightCleanup;
  };
})();

</script>

<script>
/**
 * Iframe 元素高亮注入脚本
 * 需要在目标网站中引入此脚本来支持跨域 iframe 高亮功能
 *
 * 使用方法：
 * 1. 将此脚本添加到目标网站的 HTML 中
 * 2. 或通过浏览器扩展、用户脚本等方式注入
 */

(function () {
  "use strict";

  // 检查是否在 iframe 中
  if (window.self === window.top) {
    return; // 不在 iframe 中，不执行
  }

  // 检查是否已经初始化过
  if (window.__iframeHighlightInitialized) {
    return;
  }
  window.__iframeHighlightInitialized = true;
  console.log("Iframe 高亮脚本已加载");

  // 创建高亮覆盖层
  var overlay = document.createElement("div");
  overlay.id = "iframe-highlight-overlay";
  overlay.style.cssText = "\n    position: fixed;\n    top: 0;\n    left: 0;\n    width: 100vw;\n    height: 100vh;\n    pointer-events: none;\n    z-index: 999999;\n    overflow: hidden;\n  ";

  // 创建悬停高亮框（虚线边框）
  var highlightBox = document.createElement("div");
  highlightBox.id = "iframe-highlight-box";
  highlightBox.style.cssText = "\n    position: absolute;\n    border: 2px dashed #007AFF;\n    background: rgba(0, 122, 255, 0.08);\n    pointer-events: none;\n    display: none;\n    transition: all 0.1s ease;\n    box-shadow: 0 0 0 1px rgba(255, 255, 255, 0.8);\n    border-radius: 2px;\n  ";

  // 创建选中节点的常驻高亮框（实线边框）
  var selectedBox = document.createElement("div");
  selectedBox.id = "iframe-selected-box";
  selectedBox.style.cssText = "\n    position: absolute;\n    border: 2px solid #007AFF;\n    pointer-events: none;\n    display: none;\n    box-shadow: 0 0 0 1px rgba(255, 255, 255, 0.9), 0 0 8px rgba(255, 107, 53, 0.4);\n    border-radius: 2px;\n    z-index: 1000000;\n  ";

  // 创建悬停标签显示
  var tagLabel = document.createElement("div");
  tagLabel.id = "iframe-tag-label";
  tagLabel.style.cssText = "\n    position: absolute;\n    background: #007AFF;\n    color: white;\n    padding: 2px 6px;\n    font-size: 11px;\n    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;\n    border-radius: 2px;\n    pointer-events: none;\n    display: none;\n    white-space: nowrap;\n    z-index: 1000001;\n    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);\n    font-weight: 500;\n  ";

  // 创建选中节点标签
  var selectedLabel = document.createElement("div");
  selectedLabel.id = "iframe-selected-label";
  selectedLabel.style.cssText = "\n    position: absolute;\n    background: #007AFF;\n    color: white;\n    padding: 3px 8px;\n    font-size: 11px;\n    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;\n    border-radius: 3px;\n    pointer-events: none;\n    display: none;\n    white-space: nowrap;\n    z-index: 1000002;\n    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.4);\n    font-weight: 600;\n  ";
  overlay.appendChild(highlightBox);
  overlay.appendChild(selectedBox);
  overlay.appendChild(tagLabel);
  overlay.appendChild(selectedLabel);
  document.body.appendChild(overlay);

  // 存储当前选中的元素
  var selectedElement = null;
  var highlightEnabled = false;

  // 更新选中元素的高亮显示
  function updateSelectedHighlight(element) {
    console.log("updateSelectedHighlight called with:", element);
    if (!element) {
      selectedBox.style.display = "none";
      selectedLabel.style.display = "none";
      selectedElement = null;
      console.log("Cleared selected highlight");
      return;
    }
    selectedElement = element;
    var rect = element.getBoundingClientRect();
    console.log("Selected element rect:", rect);

    // 更新选中高亮框位置
    selectedBox.style.display = "block";
    selectedBox.style.left = "".concat(rect.left - 2, "px");
    selectedBox.style.top = "".concat(rect.top - 2, "px");
    selectedBox.style.width = "".concat(rect.width + 4, "px");
    selectedBox.style.height = "".concat(rect.height + 4, "px");

    // 更新选中标签位置和内容
    selectedLabel.style.display = "block";
    selectedLabel.textContent = "\u2713 <".concat(element.tagName.toLowerCase(), ">");

    // 计算标签位置，确保不超出视窗
    var labelTop = rect.top - 28;
    var labelLeft = rect.left;

    // 如果标签会超出顶部，显示在元素下方
    if (labelTop < 5) {
      labelTop = rect.bottom + 5;
    }

    // 如果标签会超出右侧，向左调整
    var labelWidth = selectedLabel.offsetWidth || 100; // 预估宽度
    if (labelLeft + labelWidth > window.innerWidth - 10) {
      labelLeft = window.innerWidth - labelWidth - 10;
    }
    selectedLabel.style.left = "".concat(Math.max(5, labelLeft), "px");
    selectedLabel.style.top = "".concat(labelTop, "px");
    console.log("Selected highlight positioned at:", {
      left: selectedBox.style.left,
      top: selectedBox.style.top,
      width: selectedBox.style.width,
      height: selectedBox.style.height
    });
  }
  function getElementSelector(element) {
    if (!(element instanceof Element)) throw new Error('Argument must be a DOM element');
    var segments = [];
    var current = element;
    while (current !== document.documentElement) {
      var selector = '';
      // 优先检查唯一ID
      if (current.id && document.querySelectorAll("#".concat(current.id)).length === 1) {
        segments.unshift("#".concat(current.id));
        break; // ID唯一，无需继续向上
      }

      // 生成类名选择器（取第一个有效类名）
      var classes = Array.from(current.classList).filter(function (c) {
        return !c.startsWith('js-');
      });
      var className = classes.length > 0 ? ".".concat(classes[0]) : '';

      // 生成位置索引（nth-child）
      var tag = current.tagName.toLowerCase();
      if (!className) {
        var siblings = Array.from(current.parentNode.children);
        var index = siblings.findIndex(function (el) {
          return el === current;
        }) + 1;
        selector = "".concat(tag, ":nth-child(").concat(index, ")");
      } else {
        selector = className;
      }
      segments.unshift(selector);
      current = current.parentElement;
    }

    // 处理根元素
    if (current === document.documentElement) {
      segments.unshift('html');
    }
    return segments.join(' > ');
  }

  // 获取元素文本内容
  function getElementText(element) {
    var _element$textContent;
    if (element.tagName === "INPUT") {
      return element.value || element.placeholder || "";
    }
    if (element.tagName === "TEXTAREA") {
      return element.value || element.placeholder || "";
    }
    var text = ((_element$textContent = element.textContent) === null || _element$textContent === void 0 ? void 0 : _element$textContent.trim()) || "";
    return text.length > 50 ? text.substring(0, 50) + "..." : text;
  }

  // 获取元素属性信息
  function getElementAttributes(element) {
    var attrs = {};
    for (var i = 0; i < element.attributes.length; i++) {
      var attr = element.attributes[i];
      attrs[attr.name] = attr.value;
    }
    return attrs;
  }

  // 鼠标悬停事件处理
  function handleMouseOver(e) {
    if (!highlightEnabled) return;
    var target = e.target;
    if (!target || target === overlay || target === highlightBox || target === tagLabel || target === selectedBox || target === selectedLabel) {
      return;
    }

    // 避免高亮 html 和 body 元素
    if (target === document.documentElement || target === document.body) {
      return;
    }

    // 如果是已选中的元素，不显示悬停高亮
    if (target === selectedElement) {
      highlightBox.style.display = "none";
      tagLabel.style.display = "none";
      return;
    }
    var rect = target.getBoundingClientRect();
    var selector = getElementSelector(target);
    var text = getElementText(target);
    var attributes = getElementAttributes(target);

    // 更新悬停高亮框位置
    highlightBox.style.display = "block";
    highlightBox.style.left = "".concat(rect.left - 2, "px");
    highlightBox.style.top = "".concat(rect.top - 2, "px");
    highlightBox.style.width = "".concat(rect.width + 4, "px");
    highlightBox.style.height = "".concat(rect.height + 4, "px");

    // 更新标签位置和内容
    tagLabel.style.display = "block";
    tagLabel.textContent = "<".concat(target.tagName.toLowerCase(), ">");

    // 计算标签位置，确保不超出视窗
    var labelTop = rect.top - 22;
    var labelLeft = rect.left;

    // 如果标签会超出顶部，显示在元素下方
    if (labelTop < 0) {
      labelTop = rect.bottom + 5;
    }

    // 如果标签会超出右侧，向左调整
    if (labelLeft + tagLabel.offsetWidth > window.innerWidth) {
      labelLeft = window.innerWidth - tagLabel.offsetWidth - 5;
    }
    tagLabel.style.left = "".concat(Math.max(0, labelLeft), "px");
    tagLabel.style.top = "".concat(labelTop, "px");

    // 发送消息到父窗口
    var elementInfo = {
      tagName: target.tagName.toLowerCase(),
      rect: {
        left: rect.left,
        top: rect.top,
        right: rect.right,
        bottom: rect.bottom,
        width: rect.width,
        height: rect.height,
        x: rect.x,
        y: rect.y
      },
      selector: selector,
      text: text,
      attributes: attributes,
      url: window.location.href,
      path: window.location.pathname,
      timestamp: Date.now()
    };
    try {
      window.parent.postMessage({
        type: "iframe-element-hover",
        data: elementInfo,
        source: "iframe-highlight-injector"
      }, "*");
    } catch (error) {
      console.warn("无法发送消息到父窗口:", error);
    }
  }

  // 鼠标离开事件处理
  function handleMouseOut(e) {
    if (!highlightEnabled) return;
    var relatedTarget = e.relatedTarget;

    // 如果鼠标移动到高亮相关元素上，不隐藏高亮
    if (relatedTarget && (relatedTarget === highlightBox || relatedTarget === tagLabel || relatedTarget === overlay || relatedTarget === selectedBox || relatedTarget === selectedLabel)) {
      return;
    }
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    try {
      window.parent.postMessage({
        type: "iframe-element-hover",
        data: null,
        source: "iframe-highlight-injector"
      }, "*");
    } catch (error) {
      console.warn("无法发送消息到父窗口:", error);
    }
  }

  // 点击事件处理
  function handleClick(e) {
    var target = e.target;
    if (!target || target === overlay || target === highlightBox || target === tagLabel || target === selectedBox || target === selectedLabel) {
      return;
    }

    // 避免处理 html 和 body 元素
    if (target === document.documentElement || target === document.body) {
      return;
    }

    // 检查是否是交互元素，这些元素需要保留默认行为
    var isInteractiveElement = ['input', 'textarea', 'select', 'button', 'a'].includes(target.tagName.toLowerCase());

    // 如果高亮功能启用，对于非交互元素阻止默认行为和事件传播
    if (highlightEnabled) {
      e.preventDefault();
      e.stopPropagation();
    }
    var rect = target.getBoundingClientRect();
    var selector = getElementSelector(target);
    var text = getElementText(target);
    var attributes = getElementAttributes(target);
    console.log("Element clicked:", {
      tagName: target.tagName,
      selector: selector,
      rect: rect
    });

    // 立即更新选中高亮
    updateSelectedHighlight(target);

    // 隐藏悬停高亮，因为现在是选中状态
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    var elementInfo = {
      tagName: target.tagName.toLowerCase(),
      rect: {
        left: rect.left,
        top: rect.top,
        right: rect.right,
        bottom: rect.bottom,
        width: rect.width,
        height: rect.height,
        x: rect.x,
        y: rect.y
      },
      selector: selector,
      text: text,
      attributes: attributes,
      url: window.location.href,
      path: window.location.pathname,
      timestamp: Date.now()
    };
    try {
      window.parent.postMessage({
        type: "iframe-element-click",
        data: elementInfo,
        source: "iframe-highlight-injector"
      }, "*");
    } catch (error) {
      console.warn("无法发送消息到父窗口:", error);
    }
  }

  // 监听来自父窗口的消息
  function handleParentMessage(event) {
    console.log("Received message from parent:", event.data);
    if (event.data.type === "iframe-highlight-toggle") {
      var enabled = event.data.enabled;
      console.log("Highlight toggle:", enabled);
      if (enabled) {
        enableHighlight();
      } else {
        disableHighlight();
      }
    } else if (event.data.type === "enable-iframe-highlight") {
      console.log("Enable iframe highlight");
      enableHighlight();
    } else if (event.data.type === "disable-iframe-highlight") {
      console.log("Disable iframe highlight");
      disableHighlight();
    } else if (event.data.type === "toggle-iframe-highlight") {
      var _enabled = event.data.enabled !== undefined ? event.data.enabled : !highlightEnabled;
      console.log("Toggle iframe highlight to:", _enabled);
      if (_enabled) {
        enableHighlight();
      } else {
        disableHighlight();
      }
    } else if (event.data.type === "update-selected-element") {
      var selector = event.data.selector;
      console.log("Update selected element with selector:", selector);
      if (selector) {
        try {
          var element = document.querySelector(selector);
          console.log("Found element by selector:", element);
          updateSelectedHighlight(element);
        } catch (error) {
          console.warn("Failed to select element:", error);
          updateSelectedHighlight(null);
        }
      } else {
        updateSelectedHighlight(null);
      }
    } else if (event.data.type === "clear-selected-element") {
      console.log("Clear selected element");
      updateSelectedHighlight(null);
    }
  }

  // 启用高亮功能
  function enableHighlight() {
    console.log("Enabling highlight");
    document.addEventListener("mouseover", handleMouseOver, true);
    document.addEventListener("mouseout", handleMouseOut, true);
    document.addEventListener("click", handleClick, true);
    highlightEnabled = true;
    overlay.style.display = "block";
  }

  // 禁用高亮功能
  function disableHighlight() {
    console.log("Disabling highlight");
    highlightEnabled = false;
    // 保持事件监听器，但通过 highlightEnabled 变量控制行为
    // 这样可以保留选中状态的显示
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    // 不隐藏 selectedBox 和 selectedLabel，保留选中状态
  }

  // 完全禁用高亮功能（移除所有监听器）
  function fullyDisableHighlight() {
    console.log("Fully disabling highlight");
    highlightEnabled = false;
    document.removeEventListener("mouseover", handleMouseOver, true);
    document.removeEventListener("mouseout", handleMouseOut, true);
    document.removeEventListener("click", handleClick, true);
    overlay.style.display = "none";
    highlightBox.style.display = "none";
    tagLabel.style.display = "none";
    selectedBox.style.display = "none";
    selectedLabel.style.display = "none";
  }

  // 添加事件监听
  enableHighlight();
  window.addEventListener("message", handleParentMessage);

  // 暴露全局函数供外部调用
  window.__iframeHighlightControl = {
    enable: enableHighlight,
    disable: disableHighlight,
    fullyDisable: fullyDisableHighlight,
    isEnabled: function isEnabled() {
      return highlightEnabled;
    },
    getSelectedElement: function getSelectedElement() {
      return selectedElement;
    },
    updateSelected: updateSelectedHighlight,
    // 通过消息发送开关控制
    sendToggleMessage: function sendToggleMessage(enabled) {
      window.parent.postMessage({
        type: 'iframe-highlight-status',
        enabled: enabled || highlightEnabled,
        source: 'iframe-highlight-injector'
      }, '*');
    }
  };

  // 通知父窗口脚本已加载
  try {
    window.parent.postMessage({
      type: "iframe-highlight-ready",
      data: {
        url: window.location.href,
        userAgent: navigator.userAgent,
        timestamp: Date.now()
      },
      source: "iframe-highlight-injector"
    }, "*");
  } catch (error) {
    console.warn("无法发送就绪消息到父窗口:", error);
  }

  // 清理函数
  window.__iframeHighlightCleanup = function () {
    fullyDisableHighlight();
    window.removeEventListener("message", handleParentMessage);
    if (overlay.parentElement) {
      overlay.parentElement.removeChild(overlay);
    }
    delete window.__iframeHighlightInitialized;
    delete window.__iframeHighlightCleanup;
  };
})();

</script>
<style>
#minimax-floating-ball {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 10px 12px;
  background: #222222;
  border-radius: 12px;
  display: flex;
  align-items: center;
  color: #F8F8F8;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  z-index: 9999;
  transition: all 0.3s ease;
  overflow: hidden;
  cursor: pointer;
}

#minimax-floating-ball:hover {
  transform: translateY(-2px);
  background: #383838;
}
.minimax-ball-content {
  display: flex;
  align-items: center;
  gap: 8px;
}

.minimax-logo-wave {
  width: 20px;
  height: 20px;
  background-image: url("data:image/svg+xml,%3Csvg%20preserveAspectRatio%3D%27none%27%20width%3D%27100%25%27%20height%3D%27100%25%27%20overflow%3D%27visible%27%20style%3D%27display%3A%20block%3B%27%20viewBox%3D%270%200%20170.136%20138.225%27%20fill%3D%27none%27%20xmlns%3D%27http%3A//www.w3.org/2000/svg%27%3E%3Cg%20id%3D%27Frame%202116748449%27%3E%3Cpath%20id%3D%27Subtract%27%20d%3D%27M170%20101.783C170%20105.144%20168.49%20108.327%20165.886%20110.453L134.963%20135.702C132.964%20137.334%20130.463%20138.225%20127.883%20138.225H10.4938C4.69824%20138.225%200%20133.527%200%20127.732V39.2289C0%2035.8597%201.51758%2032.6698%204.13162%2030.5442L38.5402%202.56547C40.536%200.942662%2043.0298%200.0567377%2045.602%200.0567377H159.506C165.302%200.0567377%20170%204.75498%20170%2010.5506V101.783Z%27%20fill%3D%27black%27%20style%3D%27fill%3Ablack%3Bfill-opacity%3A1%3B%27/%3E%3Cpath%20id%3D%27Subtract_2%27%20d%3D%27M149.011%2094.4632C149.011%2096.1471%20148.253%2097.7415%20146.946%2098.8043L125.893%20115.936C124.895%20116.748%20123.648%20117.191%20122.361%20117.191H24.6479C22.716%20117.191%2021.15%20115.625%2021.15%20113.693V46.1166C21.15%2044.4267%2021.9135%2042.8274%2023.2274%2041.7648L47.367%2022.2437C48.3638%2021.4376%2049.607%2020.9982%2050.8888%2020.9988L145.514%2021.0427C147.446%2021.0436%20149.011%2022.6094%20149.011%2024.5406V94.4632Z%27%20fill%3D%27white%27%20style%3D%27fill%3Awhite%3Bfill-opacity%3A1%3B%27/%3E%3Cpath%20id%3D%27Rectangle%20111142564%27%20d%3D%27M42.111%2080.8025C42.111%2077.7115%2044.6167%2075.2057%2047.7077%2075.2057H60.9999C64.0908%2075.2057%2066.5966%2077.7115%2066.5966%2080.8025V121.029H42.111V80.8025Z%27%20fill%3D%27black%27%20style%3D%27fill%3Ablack%3Bfill-opacity%3A1%3B%27/%3E%3Cpath%20id%3D%27Rectangle%20111142567%27%20d%3D%27M79.1894%2080.8025C79.1894%2077.7115%2081.6952%2075.2057%2084.7861%2075.2057H98.0783C101.169%2075.2057%20103.675%2077.7115%20103.675%2080.8025V121.029H79.1894V80.8025Z%27%20fill%3D%27black%27%20style%3D%27fill%3Ablack%3Bfill-opacity%3A1%3B%27/%3E%3C/g%3E%3C/svg%3E");
  background-repeat: no-repeat;
  background-position: center;
  background-size: 14px 11px;
  background-color: #8FD1FF;
  border-radius: 4px;
}

.minimax-ball-text {
  font-size: 12px;
  font-weight: 500;
  white-space: nowrap;
}

.minimax-close-icon {
  margin-left: 8px;
  font-size: 16px;
  width: 18px;
  height: 18px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  cursor: pointer;
  opacity: 0.7;
  transition: opacity 0.2s ease;
}

.minimax-close-icon:hover {
  opacity: 1;
}
</style>
<div id="minimax-floating-ball">
  <div class="minimax-ball-content">
    <div class="minimax-logo-wave"></div>
    <span class="minimax-ball-text">Created by MiniMax Agent</span>
  </div>
  <div class="minimax-close-icon">×</div>
</div>
<script>
// Initialize floating ball functionality
function initFloatingBall() {
  const ball = document.getElementById('minimax-floating-ball');
  if (!ball) return;

  // Initial animation
  ball.style.opacity = '0';
  ball.style.transform = 'translateY(20px)';

  setTimeout(() => {
    ball.style.opacity = '1';
    ball.style.transform = 'translateY(0)';
  }, 500);

  // Handle logo click
  const ballContent = ball.querySelector('.minimax-ball-content');
  ballContent.addEventListener('click', function (e) {
    e.stopPropagation();
    window.open('https://agent.minimax.io/', '_blank');
    ball.style.transform = 'scale(0.95)';
    setTimeout(() => {
      ball.style.transform = 'scale(1)';
    }, 100);
  });

  // Handle close button click
  const closeIcon = ball.querySelector('.minimax-close-icon');
  closeIcon.addEventListener('click', function (e) {
    e.stopPropagation();
    ball.style.opacity = '0';
    ball.style.transform = 'translateY(20px)';

    setTimeout(() => {
      ball.style.display = 'none';
    }, 300);
  });
}

// Initialize when DOM is ready
document.addEventListener('DOMContentLoaded', initFloatingBall); 
</script>
</body>
</html>
