# unity-forge-services
Site officiel de Unity Forge Services

<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Unity Forge Services | Pointe-Noire</title>
  <meta name="description" content="Unity Forge Services : électricité, décoration, infographie, impression, photo, vidéo et communication digitale à Pointe-Noire, Congo.">
  <meta name="theme-color" content="#102b50">

  <style>
    :root {
      --bleu: #102b50;
      --bleu-clair: #2463a6;
      --blanc: #ffffff;
      --fond: #f4f7fb;
      --texte: #26364b;
      --orange: #f4a62a;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: var(--blanc);
      color: var(--texte);
      line-height: 1.7;
    }

    a {
      text-decoration: none;
    }

    .container {
      width: min(1120px, 90%);
      margin: auto;
    }

    header {
      background: var(--blanc);
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 15px #102b5010;
    }

    nav {
      min-height: 78px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      color: var(--bleu);
      font-size: 25px;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .logo span {
      color: var(--bleu-clair);
    }

    .logo small {
      display: block;
      font-size: 10px;
      letter-spacing: 3px;
      text-transform: uppercase;
      line-height: 1.2;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 24px;
    }

    .nav-links a {
      color: var(--bleu);
      font-size: 14px;
      font-weight: 700;
    }

    .nav-links a:hover {
      color: var(--bleu-clair);
    }

    .btn {
      display: inline-block;
      padding: 13px 22px;
      border-radius: 6px;
      font-weight: 700;
      transition: 0.2s;
      cursor: pointer;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      background: var(--bleu-clair);
      color: white;
    }

    .btn-light {
      background: white;
      color: var(--bleu);
      border: 1px solid #dce5f0;
    }

    .hero {
      background:
        radial-gradient(ellipse at 90% 10%, #2463a655, transparent 38%),
        linear-gradient(135deg, #102b50, #174777);
      color: white;
      padding: 100px 0 95px;
      overflow: hidden;
    }

    .hero-content {
      max-width: 760px;
    }

    .eyebrow {
      display: inline-block;
      color: var(--orange);
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-bottom: 18px;
    }

    .hero h1 {
      font-size: clamp(36px, 6vw, 65px);
      line-height: 1.12;
      margin-bottom: 22px;
      letter-spacing: -1.5px;
    }

    .hero h1 span {
      color: #82baff;
    }

    .hero p {
      max-width: 620px;
      font-size: 17px;
      color: #e1eaf5;
      margin-bottom: 30px;
    }

    .hero-buttons {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    .hero-note {
      margin-top: 40px;
      color: #d4e1f0;
      font-size: 13px;
    }

    section {
      padding: 78px 0;
    }

    .section-heading {
      max-width: 700px;
      margin-bottom: 36px;
    }

    .section-heading .eyebrow {
      color: var(--bleu-clair);
      margin-bottom: 8px;
    }

    .section-heading h2 {
      color: var(--bleu);
      font-size: clamp(28px, 4vw, 40px);
      line-height: 1.25;
      margin-bottom: 14px;
    }

    .section-heading p {
      color: #64748b;
    }

    .about {
      background: var(--fond);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1.2fr 1fr;
      gap: 45px;
      align-items: center;
    }

    .about-text h3 {
      font-size: 24px;
      color: var(--bleu);
      margin-bottom: 14px;
    }

    .about-text p {
      margin-bottom: 15px;
    }

    .values {
      display: grid;
      gap: 14px;
    }

    .value {
      background: white;
      padding: 20px;
      border-radius: 10px;
      border: 1px solid #e5ebf3;
    }

    .value strong {
      display: block;
      color: var(--bleu);
      margin-bottom: 5px;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .service-card {
      border: 1px solid #e5ebf3;
      padding: 26px;
      border-radius: 12px;
      background: white;
      transition: 0.2s;
    }

    .service-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 35px #102b5010;
      border-color: #b5cce8;
    }

    .service-icon {
      width: 52px;
      height: 52px;
      display: grid;
      place-items: center;
      background: #eaf2fc;
      border-radius: 10px;
      font-size: 25px;
      margin-bottom: 17px;
    }

    .service-card h3 {
      color: var(--bleu);
      font-size: 19px;
      margin-bottom: 10px;
    }

    .service-card p {
      color: #64748b;
      font-size: 14px;
    }

    .service-card ul {
      list-style: none;
      margin-top: 15px;
      font-size: 13px;
    }

    .service-card li {
      margin-top: 6px;
    }

    .service-card li::before {
      content: "✓ ";
      color: var(--bleu-clair);
      font-weight: 900;
    }

    .engagement {
      background: var(--bleu);
      color: white;
      text-align: center;
    }

    .engagement h2 {
      font-size: clamp(28px, 4vw, 42px);
      margin-bottom: 14px;
    }

    .engagement p {
      color: #dbe7f5;
      max-width: 700px;
      margin: 0 auto 25px;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 35px;
    }

    .contact-info {
      background: var(--fond);
      border-radius: 12px;
      padding: 28px;
    }

    .contact-info h3,
    .contact-form h3 {
      color: var(--bleu);
      margin-bottom: 15px;
    }

    .contact-item {
      margin-top: 18px;
      overflow-wrap: anywhere;
    }

    .contact-item strong {
      display: block;
      color: var(--bleu);
    }

    .contact-item a {
      color: var(--bleu-clair);
    }

    .contact-form {
      border: 1px solid #e5ebf3;
      border-radius: 12px;
      padding: 28px;
    }

    .field {
      margin-bottom: 15px;
    }

    .field label {
      display: block;
      margin-bottom: 6px;
      font-size: 14px;
      font-weight: 700;
    }

    .field input,
    .field textarea,
    .field select {
      width: 100%;
      padding: 12px;
      border: 1px solid #d6dfeb;
      border-radius: 6px;
      font: inherit;
      background: white;
      color: var(--texte);
    }

    .field textarea {
      min-height: 120px;
      resize: vertical;
    }

    .contact-form button {
      border: none;
      font: inherit;
    }

    footer {
      background: #091c34;
      color: #dbe7f5;
      padding: 28px 0;
      text-align: center;
      font-size: 13px;
    }

    footer strong {
      color: white;
    }

    .footer-slogan {
      margin-top: 5px;
      color: #9eb8d8;
    }

    .whatsapp-float {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 99;
      background: #1eae65;
      color: white;
      padding: 13px 17px;
      border-radius: 40px;
      font-weight: 700;
      box-shadow: 0 5px 20px #0002;
    }

    @media (max-width: 800px) {
      nav {
        padding: 14px 0;
        align-items: flex-start;
        flex-direction: column;
      }

      .nav-links {
        width: 100%;
        gap: 15px;
        flex-wrap: wrap;
      }

      .nav-links a {
        font-size: 12px;
      }

      .hero {
        padding: 70px 0;
      }

      .about-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .services-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 520px) {
      .services-grid {
        grid-template-columns: 1fr;
      }

      section {
        padding: 55px 0;
      }

      .hero h1 {
        font-size: 39px;
      }

      .btn {
        padding: 12px 16px;
      }

      .whatsapp-float {
        right: 12px;
        bottom: 12px;
        font-size: 13px;
      }
    }
  </style>
</head>

<body>

  <header>
    <nav class="container">
      <a class="logo" href="#accueil">
        UNITY <span>FORGE</span>
        <small>Services</small>
      </a>

      <div class="nav-links">
        <a href="#accueil">Accueil</a>
        <a href="#apropos">À propos</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero" id="accueil">
      <div class="container hero-content">
        <span class="eyebrow">Votre partenaire multiservices</span>

        <h1>
          Des idées aux réalisations,
          <span>construisons ensemble.</span>
        </h1>

        <p>
          Unity Forge Services accompagne les particuliers,
          les entreprises et les organisateurs d'événements
          avec des solutions pratiques, créatives et adaptées
          à leurs besoins à Pointe-Noire.
        </p>

        <div class="hero-buttons">
          <a class="btn btn-primary" href="#services">
            Découvrir nos services
          </a>
          <a class="btn btn-light" href="#contact">
            Nous contacter
          </a>
        </div>

        <div class="hero-note">
          Pointe-Noire, République du Congo
        </div>
      </div>
    </section>

    <section class="about" id="apropos">
      <div class="container about-grid">
        <div class="about-text">
          <span class="eyebrow">Qui sommes-nous ?</span>
          <h3>Une équipe, plusieurs compétences, une même ambition.</h3>

          <p>
            Unity Forge Services est une initiative entrepreneuriale
            congolaise qui rassemble plusieurs compétences autour
            d'un objectif commun : transformer les idées en réalisations
            concrètes.
          </p>

          <p>
            Nous privilégions la collaboration, le travail bien fait,
            l'écoute des clients et la recherche de solutions adaptées
            aux réalités locales.
          </p>

          <p>
            Notre ambition est de contribuer au développement
            entrepreneurial local et à la valorisation des compétences
            de la jeunesse congolaise.
          </p>
        </div>

        <div class="values">
          <div class="value">
            <strong>Notre vision</strong>
            Construire ensemble une force entrepreneuriale locale,
            durable et impactante pour la jeunesse congolaise.
          </div>

          <div class="value">
            <strong>Notre approche</strong>
            Écouter, proposer des solutions adaptées et travailler
            avec sérieux à chaque étape du projet.
          </div>

          <div class="value">
            <strong>Notre devise</strong>
            Unir pour bâtir, bâtir pour grandir.
          </div>
        </div>
      </div>
    </section>

    <section id="services">
      <div class="container">
        <div class="section-heading">
          <span class="eyebrow">Nos domaines d'activité</span>
          <h2>Des services pensés pour vos projets.</h2>
          <p>
            Une offre multiservices qui associe compétences techniques,
            créativité et solutions de proximité.
          </p>
        </div>

        <div class="services-grid">

          <article class="service-card">
            <div class="service-icon">⚡</div>
            <h3>Électricité</h3>
            <p>Des solutions électriques adaptées aux besoins du client.</p>
            <ul>
              <li>Installations électriques</li>
              <li>Éclairage et maintenance</li>
              <li>Dépannage et réparations</li>
            </ul>
          </article>

          <article class="service-card">
            <div class="service-icon">🏠</div>
            <h3>Décoration et peinture</h3>
            <p>Des idées pour valoriser vos espaces intérieurs et extérieurs.</p>
            <ul>
              <li>Décoration intérieure</li>
              <li>Peinture et finitions</li>
              <li>Décoration événementielle</li>
            </ul>
          </article>

          <article class="service-card">
            <div class="service-icon">🎨</div>
            <h3>Infographie et impression</h3>
            <p>Des supports visuels pour présenter votre activité.</p>
            <ul>
              <li>Affiches et flyers</li>
              <li>Logos et visuels publicitaires</li>
              <li>Supports imprimés</li>
            </ul>
          </article>

          <article class="service-card">
            <div class="service-icon">📸</div>
            <h3>Photo et vidéo</h3>
            <p>Des contenus visuels pour vos projets et événements.</p>
            <ul>
              <li>Création de contenus</li>
              <li>Montage vidéo</li>
              <li>Design visuel</li>
            </ul>
          </article>

          <article class="service-card">
            <div class="service-icon">📱</div>
            <h3>Communication digitale</h3>
            <p>Une présence en ligne pensée pour votre activité.</p>
            <ul>
              <li>Visuels pour les réseaux sociaux</li>
              <li>Communication locale</li>
              <li>Marketing digital</li>
            </ul>
          </article>

          <article class="service-card">
            <div class="service-icon">🥤</div>
            <h3>Boissons et services de proximité</h3>
            <p>Des solutions pratiques pour les besoins du quotidien.</p>
            <ul>
              <li>Yaourts et boissons fraîches</li>
              <li>Petits travaux et réparations</li>
              <li>Services liés aux événements</li>
            </ul>
          </article>

        </div>
      </div>
    </section>

    <section class="engagement">
      <div class="container">
        <span class="eyebrow">Notre engagement</span>
        <h2>Unir pour bâtir, bâtir pour grandir.</h2>
        <p>
          Chaque projet est une occasion de mettre les compétences
          en commun, de créer de la valeur et de contribuer
          à une dynamique entrepreneuriale locale.
        </p>
        <a class="btn btn-light" href="#contact">
          Parlons de votre projet
        </a>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="section-heading">
          <span class="eyebrow">Contact</span>
          <h2>Parlons de votre prochain projet.</h2>
          <p>
            Présentez-nous votre besoin pour que nous puissions
            échanger sur les solutions possibles.
          </p>
        </div>

        <div class="contact-grid">
          <div class="contact-info">
            <h3>Nos coordonnées</h3>
            <p>Retrouvez-nous à Pointe-Noire, République du Congo.</p>

            <div class="contact-item">
              <strong>Entreprise</strong>
              Unity Forge Services
            </div>

            <div class="contact-item">
              <strong>Localisation</strong>
              Pointe-Noire, Congo-Brazzaville
            </div>

            <div class="contact-item">
              <strong>Courriel</strong>
              <a href="mailto:brunelmbama3@gmail.com">
                brunelmbama3@gmail.com
              </a>
            </div>

            <div class="contact-item">
              <strong>WhatsApp</strong>
              <a href="https://wa.me/242XXXXXXXX" target="_blank"
                 rel="noopener noreferrer">
                Nous écrire sur WhatsApp
              </a>
            </div>
          </div>

          <div class="contact-form">
            <h3>Envoyer une demande</h3>

            <form id="contactForm">
              <div class="field">
                <label for="nom">Votre nom</label>
                <input id="nom" name="nom" type="text"
                       placeholder="Nom et prénom" required>
              </div>

              <div class="field">
                <label for="email">Votre adresse e-mail</label>
                <input id="email" name="email" type="email"
                       placeholder="exemple@email.com" required>
              </div>

              <div class="field">
                <label for="service">Service recherché</label>
                <select id="service" name="service" required>
                  <option value="">Choisir un service</option>
                  <option>Électricité</option>
                  <option>Décoration et peinture</option>
                  <option>Infographie et impression</option>
                  <option>Photo et vidéo</option>
                  <option>Communication digitale</option>
                  <option>Boissons et services de proximité</option>
                  <option>Autre demande</option>
                </select>
              </div>

              <div class="field">
                <label for="message">Votre message</label>
                <textarea id="message" name="message"
                          placeholder="Décrivez votre projet..."
                          required></textarea>
              </div>

              <button class="btn btn-primary" type="submit">
                Préparer ma demande
              </button>
            </form>

            <p style="font-size:12px;color:#64748b;margin-top:12px">
              Votre demande sera préparée dans votre application
              de messagerie électronique.
            </p>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <strong>UNITY FORGE SERVICES</strong>
      <p>© <span id="year"></span> Unity Forge Services. Tous droits réservés.</p>
      <p class="footer-slogan">Unir pour bâtir, bâtir pour grandir.</p>
    </div>
  </footer>

  <a class="whatsapp-float"
     href="https://wa.me/242XXXXXXXX"
     target="_blank"
     rel="noopener noreferrer"
     aria-label="Contacter Unity Forge Services sur WhatsApp">
    WhatsApp
  </a>

  <script>
    document.getElementById("year").textContent =
      new Date().getFullYear();

    document.getElementById("contactForm").addEventListener(
      "submit",
      function (event) {
        event.preventDefault();

        const nom = document.getElementById("nom").value.trim();
        const email = document.getElementById("email").value.trim();
        const service = document.getElementById("service").value;
        const message = document.getElementById("message").value.trim();

        const sujet = encodeURIComponent(
          "Demande de renseignements - Unity Forge Services"
        );

        const corps = encodeURIComponent(
          "Bonjour Unity Forge Services,\n\n" +
          "Nom : " + nom + "\n" +
          "E-mail : " + email + "\n" +
          "Service : " + service + "\n\n" +
          "Message :\n" + message
        );

        window.location.href =
          "mailto:brunelmbama3@gmail.com?subject=" +
          sujet + "&body=" + corps;
      }
    );
  </script>

</body>
</html>

