<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title data-i18n="pageTitle">Altea Bank - Le crédit transparent, rapide et sécurisé</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    
    <style>
        /* Importation d'une police professionnelle de Google Fonts */
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');

        :root {
            /* Définition des couleurs principales du site */
            --color-dark-blue: #0A192F;
            --color-gold: #FFD700;
            --color-black-mat: #121212;
            --color-white: #FFFFFF;
            --color-light-gray: #EFEFEF;
        }

        /* Styles généraux pour le corps de la page */
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--color-black-mat);
            color: var(--color-white);
            line-height: 1.6;
            transition: background-color 0.5s ease-in-out;
        }

        /* Styles pour les titres (h1, h2, etc.) */
        h1, h2 {
            color: var(--color-gold);
            font-weight: 600;
        }

        /* Styles pour les liens */
        a {
            text-decoration: none;
            color: var(--color-white);
            transition: color 0.3s ease;
        }

        a:hover {
            color: var(--color-gold);
        }

        /* Styles pour l'en-tête (Header) */
        header {
            background-color: var(--color-dark-blue);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
        }

        .logo h1 {
            margin: 0;
            font-size: 1.5rem;
            color: var(--color-white);
        }

        .main-nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            gap: 2rem;
        }

        .language-selector button {
            background: none;
            border: 1px solid var(--color-white);
            color: var(--color-white);
            padding: 0.5rem 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .language-selector button:hover {
            background-color: var(--color-gold);
            border-color: var(--color-gold);
        }

        /* Styles pour la section principale (Hero) */
        .hero {
            background-color: var(--color-black-mat);
            color: var(--color-white);
            text-align: center;
            padding: 10rem 2rem;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero-content p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 2rem;
        }

        .cta-buttons .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
            border-radius: 5px;
            font-weight: 600;
            transition: transform 0.3s ease;
        }

        .cta-buttons .btn:hover {
            transform: translateY(-5px);
        }

        .btn-primary {
            background-color: var(--color-gold);
            color: var(--color-dark-blue);
            margin-right: 1rem;
        }

        .btn-secondary {
            background-color: transparent;
            border: 2px solid var(--color-white);
            color: var(--color-white);
        }

        /* Styles pour la section du simulateur */
        .simulator-section {
            background-color: var(--color-dark-blue);
            padding: 4rem 2rem;
            text-align: center;
        }

        .simulator-section h2 {
            margin-bottom: 2rem;
        }

        .simulator-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--color-black-mat);
            padding: 2rem;
            border-radius: 10px;
        }

        .form-group {
            margin-bottom: 1.5rem;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        input[type="range"] {
            width: 100%;
            -webkit-appearance: none;
            appearance: none;
            background: var(--color-light-gray);
            height: 8px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            background: var(--color-gold);
            border-radius: 50%;
            cursor: pointer;
        }

        .form-group span {
            font-weight: 600;
            color: var(--color-gold);
        }

        .result {
            margin-top: 2rem;
            padding: 1rem;
            border: 2px solid var(--color-gold);
            border-radius: 5px;
        }

        .result p {
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0;
        }

        .result .rate {
            font-size: 0.9rem;
            color: var(--color-light-gray);
            margin-top: 0.5rem;
        }

        /* Styles pour la section des services */
        .services-section {
            background-color: var(--color-black-mat);
            padding: 4rem 2rem;
            text-align: center;
        }

        .section-description {
            font-size: 1.1rem;
            color: var(--color-light-gray);
            max-width: 800px;
            margin: 0 auto 3rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .service-card {
            background-color: var(--color-dark-blue);
            padding: 2rem;
            border-radius: 10px;
            text-align: left;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid transparent;
        }

        .service-card:hover {
            transform: translateY(-10px);
            border-color: var(--color-gold);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .service-card h3 {
            margin-top: 0;
            font-size: 1.5rem;
            color: var(--color-gold);
        }

        .service-card p {
            color: var(--color-light-gray);
        }

        .conditions-note {
            margin-top: 4rem;
            font-style: italic;
            color: var(--color-gold);
        }

        /* Styles pour la section des conditions */
        .conditions-section {
            background-color: var(--color-dark-blue);
            padding: 4rem 2rem;
            text-align: center;
        }

        .conditions-grid {
            display: flex;
            justify-content: center;
            gap: 3rem;
            flex-wrap: wrap; /* Pour que les éléments aillent à la ligne sur les petits écrans */
            margin-top: 3rem;
        }

        .condition-item {
            background-color: var(--color-black-mat);
            padding: 2rem;
            border-radius: 10px;
            text-align: left;
            max-width: 450px;
        }

        .condition-item h3 {
            margin-top: 0;
            color: var(--color-gold);
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
        }

        .condition-item ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .condition-item li {
            margin-bottom: 1rem;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            color: var(--color-light-gray);
        }

        .condition-item i {
            color: var(--color-gold);
            margin-right: 1rem;
            font-size: 1.2rem;
        }

        .cta-conditions {
            margin-top: 3rem;
            font-size: 1.2rem;
        }

        .cta-conditions a {
            color: var(--color-gold);
            border-bottom: 2px solid var(--color-gold);
            transition: border-bottom-color 0.3s ease;
        }

        .cta-conditions a:hover {
            border-bottom-color: transparent;
        }

        /* Styles pour la section du formulaire */
        .form-section {
            background-color: var(--color-black-mat);
            padding: 4rem 2rem;
            text-align: center;
        }

        .loan-application-form {
            max-width: 800px;
            margin: 0 auto;
            background-color: var(--color-dark-blue);
            padding: 2rem;
            border-radius: 10px;
        }

        .form-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .form-group {
            text-align: left;
        }

        .form-group.full-width {
            grid-column: span 2;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--color-white);
            font-weight: 600;
        }

        .form-group input {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid var(--color-white);
            background-color: transparent;
            color: var(--color-white);
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group input:focus {
            outline: none;
            border-color: var(--color-gold);
            box-shadow: 0 0 5px rgba(255, 215, 0, 0.5);
        }

        .form-group small {
            color: var(--color-light-gray);
            font-size: 0.8rem;
            display: block;
            margin-top: 0.5rem;
        }

        .loan-application-form .btn-primary {
            width: auto;
            padding: 1rem 3rem;
            font-size: 1.1rem;
        }

        /* Styles pour la section des témoignages */
        .testimonials-section {
            background-color: var(--color-dark-blue);
            padding: 4rem 2rem;
            text-align: center;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .testimonial-card {
            background-color: var(--color-black-mat);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
        }

        .testimonial-card .rating {
            color: var(--color-gold);
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        .testimonial-card .quote {
            font-style: italic;
            color: var(--color-light-gray);
            margin-bottom: 1.5rem;
        }

        .testimonial-card .author {
            font-weight: 600;
            color: var(--color-white);
            margin: 0;
        }

        /* Styles pour la section "À propos" */
        .about-section {
            background-color: var(--color-black-mat);
            padding: 4rem 2rem;
            text-align: center;
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            color: var(--color-light-gray);
            font-size: 1.1rem;
        }

        .about-content p {
            margin-bottom: 1.5rem;
        }
        
        /* Styles pour le pied de page */
        footer {
            background-color: var(--color-dark-blue);
            padding: 4rem 2rem 2rem;
            color: var(--color-light-gray);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            border-bottom: 1px solid var(--color-black-mat);
            padding-bottom: 2rem;
        }

        .footer-about h3, .footer-links h3, .footer-legal h3 {
            color: var(--color-white);
            margin-top: 0;
        }

        .footer-about p {
            font-size: 0.9rem;
            line-height: 1.5;
        }

        .footer-links ul, .footer-legal ul {
            list-style: none;
            padding: 0;
        }

        .footer-links li, .footer-legal li {
            margin-bottom: 0.8rem;
        }

        .footer-links a, .footer-legal a {
            color: var(--color-light-gray);
            transition: color 0.3s ease;
        }

        .footer-links a:hover, .footer-legal a:hover {
            color: var(--color-gold);
        }

        .footer-bottom {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.8rem;
            color: var(--color-light-gray);
        }

        /* Media Queries pour le responsive design */
        @media (max-width: 768px) {
            .main-nav {
                display: none; /* Le menu sera caché sur les petits écrans */
            }

            .hero-content h1 {
                font-size: 2rem;
            }

            .cta-buttons {
                display: flex;
                flex-direction: column;
                gap: 1rem;
                align-items: center;
            }

            .cta-buttons .btn {
                width: 80%; /* Les boutons s'étendent sur toute la largeur */
            }

            .btn-primary {
                margin-right: 0;
            }

            .form-grid {
                grid-template-columns: 1fr;
            }

            .form-group.full-width {
                grid-column: span 1;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">
            <h1 aria-label="Altea Bank, retour à la page d'accueil">Altea Bank</h1>
        </div>
        <nav class="main-nav" aria-label="Menu de navigation principal">
            <ul>
                <li><a href="#services" data-i18n="navServices">Nos services</a></li>
                <li><a href="#simulator" data-i18n="navSimulator">Simulateur</a></li>
                <li><a href="#form" data-i18n="navContact">Faire une demande</a></li>
                <li><a href="#" data-i18n="navLogin">Espace client</a></li>
            </ul>
        </nav>
        <div class="language-selector">
            <button class="lang-btn" data-lang="fr" aria-label="Changer la langue en français">FR 🇫🇷</button>
            <button class="lang-btn" data-lang="en" aria-label="Change language to English">EN 🇬🇧</button>
            <button class="lang-btn" data-lang="es" aria-label="Cambiar idioma a español">ES 🇪🇸</button>
        </div>
    </header>

    <main class="hero">
        <div class="hero-content">
            <h1 data-i18n="heroSlogan">Le crédit transparent, rapide et sécurisé</h1>
            <p data-i18n="heroSubtitle">Simplifiez vos projets de vie avec des solutions de financement adaptées à vos besoins.</p>
            <div class="cta-buttons">
                <a href="#simulator" class="btn btn-primary" data-i18n="ctaSimulate">Simuler mon crédit</a>
                <a href="#form" class="btn btn-secondary" data-i18n="ctaRequest">Faire une demande</a>
            </div>
        </div>
    </main>
    
    <section class="simulator-section" id="simulator">
        <div class="container">
            <h2 data-i18n="simulatorTitle">Simuler votre crédit</h2>
            <div class="simulator-form">
                <div class="form-group">
                    <label for="amount" data-i18n="labelAmount">Montant souhaité (€)</label>
                    <input type="range" id="amount" min="1000" max="50000" step="500" value="10000">
                    <span id="amount-value">10 000 €</span>
                </div>
                <div class="form-group">
                    <label for="duration" data-i18n="labelDuration">Durée de remboursement (mois)</label>
                    <input type="range" id="duration" min="12" max="120" step="6" value="36">
                    <span id="duration-value">36 mois</span>
                </div>
                <div class="result">
                    <h3 data-i18n="monthlyPaymentTitle">Mensualité estimée</h3>
                    <p id="monthly-payment">0,00 €</p>
                    <p class="rate" data-i18n="rateInfo">Taux d'intérêt fixe : 3% par an</p>
                </div>
            </div>
        </div>
    </section>

    <section class="services-section" id="services">
        <div class="container">
            <h2 data-i18n="servicesTitle">Nos services de crédit</h2>
            <p class="section-description" data-i18n="servicesDescription">Découvrez nos solutions de financement transparentes et adaptées à chaque projet.</p>
            <div class="services-grid">
                <div class="service-card">
                    <h3 data-i18n="servicePersonal">Crédit personnel</h3>
                    <p data-i18n="servicePersonalDesc">Pour financer vos projets de vie sans avoir à justifier de leur utilisation.</p>
                </div>
                <div class="service-card">
                    <h3 data-i18n="serviceAuto">Prêt automobile</h3>
                    <p data-i18n="serviceAutoDesc">Réalisez l'achat de la voiture de vos rêves avec un financement sur mesure.</p>
                </div>
                <div class="service-card">
                    <h3 data-i18n="serviceMortgage">Prêt hypothécaire</h3>
                    <p data-i18n="serviceMortgageDesc">Accédez à la propriété en toute sérénité avec nos prêts immobiliers à taux compétitifs.</p>
                </div>
                <div class="service-card">
                    <h3 data-i18n="servicePro">Prêt professionnel</h3>
                    <p data-i18n="serviceProDesc">Développez votre entreprise avec un financement flexible, adapté à vos ambitions.</p>
                </div>
                <div class="service-card">
                    <h3 data-i18n="serviceStudent">Prêt étudiant</h3>
                    <p data-i18n="serviceStudentDesc">Financez vos études supérieures sans stress et commencez votre carrière sans soucis.</p>
                </div>
                <div class="service-card">
                    <h3 data-i18n="serviceProject">Crédit projet</h3>
                    <p data-i18n="serviceProjectDesc">Transformez vos idées en réalité, qu'il s'agisse de travaux, de voyages ou d'événements.</p>
                </div>
                <div class="service-card">
                    <h3 data-i18n="serviceRevolving">Crédit renouvelable</h3>
                    <p data-i18n="serviceRevolvingDesc">Profitez d'une réserve d'argent disponible à tout moment pour faire face aux imprévus.</p>
                </div>
            </div>
            <p class="conditions-note" data-i18n="servicesNote">Taux fixe de 3% par an et remboursements souples pour tous nos services.</p>
        </div>
    </section>

    <section class="conditions-section">
        <div class="container">
            <h2 data-i18n="conditionsTitle">Conditions d'obtention</h2>
            <p class="section-description" data-i18n="conditionsDescription">Nos critères de sélection sont simples et transparents, pour vous permettre d'obtenir un crédit rapidement et sans complication.</p>
            
            <div class="conditions-grid">
                <div class="condition-item">
                    <h3 data-i18n="criteriaTitle">Critères de base</h3>
                    <ul>
                        <li><i class="fas fa-check-circle"></i> <span data-i18n="criteria1">Être âgé de 18 ans ou plus.</span></li>
                        <li><i class="fas fa-check-cir
