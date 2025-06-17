<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Miloslav Hesek - Profesionální profil</title>
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
            background-color: #ffffff;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 80px 0;
            text-align: center;
        }

        .header h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            animation: fadeInUp 1s ease;
        }

        .header .subtitle {
            font-size: 1.3rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s both;
        }

        /* Navigation */
        .nav {
            background: #333;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }

        .nav li {
            margin: 0 20px;
        }

        .nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav a:hover {
            color: #667eea;
        }

        /* Sections */
        .section {
            padding: 60px 0;
        }

        .section:nth-child(even) {
            background-color: #f8f9fa;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 50px;
            color: #333;
        }

        /* About section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 40px;
            align-items: center;
        }

        .profile-image {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 80px;
            margin: 0 auto;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* Skills section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .skill-category {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .skill-category:hover {
            transform: translateY(-5px);
        }

        .skill-category h3 {
            color: #667eea;
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
        }

        .skill-list li:last-child {
            border-bottom: none;
        }

        /* Experience section */
        .experience-timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline-item {
            background: white;
            padding: 30px;
            margin: 20px 0;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-left: 5px solid #667eea;
        }

        .timeline-item h3 {
            color: #667eea;
            margin-bottom: 10px;
        }

        .timeline-item .date {
            color: #666;
            font-style: italic;
            margin-bottom: 15px;
        }

        /* Projects section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-image {
            height: 200px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .project-content {
            padding: 25px;
        }

        .project-content h3 {
            color: #333;
            margin-bottom: 15px;
        }

        .project-content p {
            color: #666;
            line-height: 1.6;
        }

        /* Contact section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            max-width: 800px;
            margin: 0 auto;
        }

        .contact-item {
            text-align: center;
            padding: 30px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .contact-item h3 {
            color: #667eea;
            margin-bottom: 15px;
        }

        .contact-icon {
            font-size: 3rem;
            color: #667eea;
            margin-bottom: 20px;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 30px 0;
        }

        /* Animations */
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

        /* Responsive design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .about-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .nav ul {
                flex-direction: column;
                align-items: center;
            }

            .nav li {
                margin: 5px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <h1>Miloslav Hesek</h1>
            <p class="subtitle">Profesionální profil & Portfolio</p>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="nav">
        <div class="container">
            <ul>
                <li><a href="#about">O mně</a></li>
                <li><a href="#skills">Dovednosti</a></li>
                <li><a href="#experience">Zkušenosti</a></li>
                <li><a href="#projects">Projekty</a></li>
                <li><a href="#contact">Kontakt</a></li>
            </ul>
        </div>
    </nav>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">O mně</h2>
            <div class="about-content">
                <div class="profile-image">MH</div>
                <div class="about-text">
                    <p>Vítejte na mém profesionálním profilu! Jsem Miloslav Hesek a specializuji se na moderní technologie a inovativní řešení. S dlouholetými zkušenostmi v oboru se věnuji projektům, které přinášejí skutečnou hodnotu.</p>
                    
                    <p>Moje práce se zaměřuje na kvalitu, efektivitu a inovace. Věřím v sílu týmové spolupráce a neustálého vzdělávání. Každý projekt vnímám jako příležitost k růstu a zdokonalování.</p>
                    
                    <p>Pokud hledáte spolehlivého partnera pro vaše projekty nebo máte zájem o spolupráci, jsem zde připraven pomoci s realizací vašich cílů.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
        <div class="container">
            <h2 class="section-title">Moje dovednosti</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>🛠️ Technické dovednosti</h3>
                    <ul class="skill-list">
                        <li>Projektové řízení</li>
                        <li>Analytické myšlení</li>
                        <li>Řešení problémů</li>
                        <li>Technická dokumentace</li>
                        <li>Kvalitní komunikace</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>💼 Manažerské dovednosti</h3>
                    <ul class="skill-list">
                        <li>Vedení týmů</li>
                        <li>Strategické plánování</li>
                        <li>Koordinace projektů</li>
                        <li>Časové řízení</li>
                        <li>Prezentační dovednosti</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>🌐 Komunikační dovednosti</h3>
                    <ul class="skill-list">
                        <li>Efektivní komunikace</li>
                        <li>Aktivní naslouchání</li>
                        <li>Vyjednávání</li>
                        <li>Multikulturní prostředí</li>
                        <li>Zákaznický přístup</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="section">
        <div class="container">
            <h2 class="section-title">Profesionální zkušenosti</h2>
            <div class="experience-timeline">
                <div class="timeline-item">
                    <h3>Senior specialista</h3>
                    <div class="date">2020 - současnost</div>
                    <p>Vedení klíčových projektů a koordinace týmových aktivit. Odpovědnost za strategické plánování a implementaci inovativních řešení.</p>
                </div>
                <div class="timeline-item">
                    <h3>Projektový koordinátor</h3>
                    <div class="date">2017 - 2020</div>
                    <p>Řízení střednědobých projektů, koordinace mezi odděleními a zajištění splnění stanovených cílů v termínu a rozpočtu.</p>
                </div>
                <div class="timeline-item">
                    <h3>Analytik</h3>
                    <div class="date">2014 - 2017</div>
                    <p>Analýza obchodních procesů, příprava doporučení pro optimalizaci a podporu rozhodovacích procesů managementu.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <div class="container">
            <h2 class="section-title">Vybrané projekty</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image">🚀</div>
                    <div class="project-content">
                        <h3>Inovativní řešení</h3>
                        <p>Komplexní projekt zaměřený na modernizaci a optimalizaci klíčových procesů s významným dopadem na efektivitu organizace.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">📊</div>
                    <div class="project-content">
                        <h3>Analytický systém</h3>
                        <p>Vývoj a implementace pokročilého analytického nástroje pro podporu strategického rozhodování a business intelligence.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">🎯</div>
                    <div class="project-content">
                        <h3>Strategická iniciativa</h3>
                        <p>Dlouhodobý projekt koordinace a implementace strategických změn s pozitivním dopadem na celkovou výkonnost.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Kontakt</h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <div class="contact-icon">📧</div>
                    <h3>Email</h3>
                    <p>miloslav.hesek@email.cz</p>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">📱</div>
                    <h3>Telefon</h3>
                    <p>+420 xxx xxx xxx</p>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">📍</div>
                    <h3>Lokace</h3>
                    <p>Ostrava, 735 41<br>Moravskoslezský kraj, ČR</p>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">💼</div>
                    <h3>Dostupnost</h3>
                    <p>Otevřen zajímavým<br>organizačním procesům</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2025 Miloslav Hesek. Všechna práva vyhrazena.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
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
    </script>
</body>
</html>
