<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Digital Future — Дизайнер цифровых пространств</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display",
                   "Segoe UI", Arial, sans-serif;
      background: #ffffff;
      color: #111111;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      width: min(1180px, 92%);
      margin: auto;
    }

    /* ================= HEADER ================= */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;

      background: rgba(255,255,255,0.82);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);

      border-bottom: 1px solid #eeeeee;
    }

    nav {
      height: 72px;

      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 18px;
      font-weight: 700;
      letter-spacing: -0.5px;
    }

    .logo span {
      color: #0757ff;
    }

    .menu {
      display: flex;
      gap: 32px;

      font-size: 14px;
      color: #555;
    }

    .menu a {
      transition: 0.2s;
    }

    .menu a:hover {
      color: #0757ff;
    }

    .nav-button {
      background: #0757ff;
      color: white;

      padding: 11px 18px;

      border-radius: 999px;

      font-size: 14px;
      font-weight: 600;

      transition: 0.2s;
    }

    .nav-button:hover {
      background: #0047df;
      transform: translateY(-1px);
    }

    /* ================= HERO ================= */

    .hero {
      min-height: 100vh;

      display: flex;
      align-items: center;

      padding-top: 100px;
      padding-bottom: 80px;
    }

    .hero-content {
      max-width: 1000px;
    }

    .label {
      display: inline-block;

      padding: 8px 14px;

      border-radius: 999px;

      background: #f3f6ff;
      color: #0757ff;

      font-size: 13px;
      font-weight: 600;

      margin-bottom: 28px;
    }

    h1 {
      font-size: clamp(55px, 9vw, 110px);

      line-height: 0.95;

      letter-spacing: -7px;

      font-weight: 700;

      margin-bottom: 35px;
    }

    h1 span {
      color: #0757ff;
    }

    .hero-text {
      max-width: 650px;

      font-size: 20px;
      line-height: 1.6;

      color: #666;

      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      gap: 12px;

      flex-wrap: wrap;
    }

    .button {
      display: inline-flex;

      align-items: center;
      justify-content: center;

      padding: 15px 24px;

      border-radius: 999px;

      font-size: 15px;
      font-weight: 600;

      transition: 0.25s;
    }

    .button-blue {
      background: #0757ff;
      color: white;

      box-shadow: 0 10px 30px rgba(7,87,255,0.18);
    }

    .button-blue:hover {
      background: #0047df;
      transform: translateY(-2px);
    }

    .button-light {
      background: #f3f3f3;
      color: #111;
    }

    .button-light:hover {
      background: #e9e9e9;
    }

    /* ================= STATS ================= */

    .stats {
      display: grid;

      grid-template-columns: repeat(3, 1fr);

      gap: 16px;

      margin-top: 90px;
    }

    .stat {
      padding: 30px;

      border-radius: 24px;

      background: #f7f7f7;
    }

    .stat-number {
      font-size: 38px;
      font-weight: 700;

      letter-spacing: -2px;

      margin-bottom: 8px;
    }

    .stat-text {
      color: #777;
      font-size: 14px;
    }

    /* ================= SECTIONS ================= */

    section {
      padding: 130px 0;
    }

    .section-title {
      font-size: clamp(40px, 6vw, 70px);

      line-height: 1;

      letter-spacing: -4px;

      max-width: 800px;

      margin-bottom: 25px;
    }

    .section-description {
      max-width: 600px;

      color: #777;

      font-size: 18px;
      line-height: 1.6;

      margin-bottom: 60px;
    }

    /* ================= CARDS ================= */

    .cards {
      display: grid;

      grid-template-columns: repeat(3, 1fr);

      gap: 18px;
    }

    .card {
      min-height: 300px;

      padding: 30px;

      border-radius: 28px;

      background: #f7f7f7;

      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-6px);

      box-shadow:
        0 20px 50px rgba(0,0,0,0.08);
    }

    .card-number {
      color: #0757ff;

      font-size: 13px;
      font-weight: 700;

      margin-bottom: 100px;
    }

    .card h3 {
      font-size: 27px;

      letter-spacing: -1px;

      margin-bottom: 12px;
    }

    .card p {
      color: #777;

      line-height: 1.5;

      font-size: 15px;
    }

    /* ================= BLUE BLOCK ================= */

    .blue-section {
      background: #0757ff;

      color: white;
    }

    .blue-section .section-description {
      color: rgba(255,255,255,0.72);
    }

    .world-box {
      display: grid;

      grid-template-columns: 1fr 1fr;

      gap: 20px;
    }

    .world-card {
      min-height: 350px;

      padding: 40px;

      border-radius: 30px;

      background: rgba(255,255,255,0.1);

      border: 1px solid rgba(255,255,255,0.15);
    }

    .world-card h3 {
      font-size: 50px;

      line-height: 1;

      letter-spacing: -3px;

      margin-bottom: 25px;
    }

    .world-card p {
      color: rgba(255,255,255,0.75);

      font-size: 17px;
      line-height: 1.6;
    }

    .countries {
      display: flex;

      flex-direction: column;

      gap: 0;
    }

    .country {
      display: flex;

      justify-content: space-between;

      padding: 22px 0;

      border-bottom: 1px solid rgba(255,255,255,0.2);

      font-size: 16px;
    }

    .country:last-child {
      border-bottom: none;
    }

    /* ================= CONTACT ================= */

    .contact {
      text-align: center;
    }

    .contact .section-title {
      margin-left: auto;
      margin-right: auto;
    }

    .contact .section-description {
      margin-left: auto;
      margin-right: auto;
    }

    .contact-buttons {
      display: flex;

      justify-content: center;

      gap: 14px;

      flex-wrap: wrap;
    }

    /* ================= FOOTER ================= */

    footer {
      border-top: 1px solid #eeeeee;

      padding: 30px 0;

      color: #888;

      font-size: 13px;
    }

    .footer-content {
      display: flex;

      justify-content: space-between;

      gap: 20px;
    }

    /* ================= MOBILE ================= */

    @media (max-width: 800px) {

      .menu {
        display: none;
      }

      h1 {
        letter-spacing: -4px;
      }

      .stats {
        grid-template-columns: 1fr;
        margin-top: 55px;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      .world-box {
        grid-template-columns: 1fr;
      }

      .world-card h3 {
        font-size: 38px;
      }

      section {
        padding: 90px 0;
      }

      .footer-content {
        flex-direction: column;
      }
    }
  </style>
</head>


<body>

<!-- ================= HEADER ================= -->

<header>

  <div class="container">

    <nav>

      <a href="#" class="logo">
        DIGITAL<span>FUTURE</span>
      </a>

      <div class="menu">

        <a href="#about">О нас</a>

        <a href="#directions">Направления</a>

        <a href="#world">География</a>

        <a href="#contact">Контакты</a>

      </div>

      <a href="#contact" class="nav-button">
        Связаться
      </a>

    </nav>

  </div>

</header>


<!-- ================= HERO ================= -->

<section class="hero">

  <div class="container">

    <div class="hero-content">

      <div class="label">
        DIGITAL SPACE OF THE FUTURE
      </div>

      <h1>
        Дизайнер<br>
        цифровых <span>пространств.</span>
      </h1>

      <p class="hero-text">

        Создаём современные цифровые пространства,
        бренды и интерфейсы, которые помогают
        компаниям и людям двигаться в будущее.

      </p>

      <div class="buttons">

        <a href="#contact" class="button button-blue">
          Обсудить проект →
        </a>

        <a href="#directions" class="button button-light">
          Наши направления
        </a>

      </div>

      <!-- STATS -->

      <div class="stats">

        <div class="stat">

          <div class="stat-number">
            50 000+
          </div>

          <div class="stat-text">
            учеников и участников
          </div>

        </div>


        <div class="stat">

          <div class="stat-number">
            Россия
          </div>

          <div class="stat-text">
            работаем по всей стране
          </div>

        </div>


        <div class="stat">

          <div class="stat-number">
            Global
          </div>

          <div class="stat-text">
            открыты для международных проектов
          </div>

        </div>

      </div>

    </div>

  </div>

</section>


<!-- ================= ABOUT ================= -->

<section id="about">

  <div class="container">

    <h2 class="section-title">
      Цифровой дизайн —
      это новый язык бизнеса.
    </h2>

    <p class="section-description">

      Мы объединяем дизайн, технологии и стратегию,
      чтобы создавать цифровые продукты, которыми
      хочется пользоваться.

    </p>

  </div>

</section>


<!-- ================= DIRECTIONS ================= -->

<section id="directions">

  <div class="container">

    <h2 class="section-title">
      Что мы создаём.
    </h2>

    <p class="section-description">

      От идеи до готового цифрового пространства.

    </p>


    <div class="cards">


      <div class="card">

        <div class="card-number">
          01 / WEB
        </div>

        <h3>
          Web & UI
        </h3>

        <p>

          Современные сайты, интерфейсы
          и цифровые продукты с сильным
          пользовательским опытом.

        </p>

      </div>


      <div class="card">

        <div class="card-number">
          02 / BRAND
        </div>

        <h3>
          Digital Branding
        </h3>

        <p>

          Создаём визуальные системы,
          которые делают бренд узнаваемым
          в цифровой среде.

        </p>

      </div>


      <div class="card">

        <div class="card-number">
          03 / EDUCATION
        </div>

        <h3>
          Обучение
        </h3>

        <p>

          Практические знания для тех,
          кто хочет создавать цифровые
          продукты будущего.

        </p>

      </div>


    </div>

  </div>

</section>


<!-- ================= WORLD ================= -->

<section id="world" class="blue-section">

  <div class="container">

    <h2 class="section-title">
      Из России —
      в весь мир.
    </h2>

    <p class="section-description">

      Работаем с проектами по всей России
      и открыты к сотрудничеству
      с компаниями из других стран.

    </p>


    <div class="world-box">


      <div class="world-card">

        <h3>
          50 000+
        </h3>

        <p>

          учеников уже получили знания
          и инструменты для развития
          в цифровой среде.

        </p>

      </div>


      <div class="world-card">

        <div class="countries">

          <div class="country">

            <span>Россия</span>

            <strong>01</strong>

          </div>


          <div class="country">

            <span>СНГ</span>

            <strong>02</strong>

          </div>


          <div class="country">

            <span>Европа</span>

            <strong>03</strong>

          </div>


          <div class="country">

            <span>Другие страны</span>

            <strong>04</strong>

          </div>


          <div class="country">

            <span>Worldwide</span>

            <strong>∞</strong>

          </div>

        </div>

      </div>


    </div>

  </div>

</section>


<!-- ================= CONTACT ================= -->

<section id="contact" class="contact">

  <div class="container">

    <h2 class="section-title">
      Давайте создадим
      что-то большое.
    </h2>

    <p class="section-description">

      Расскажите о своей задаче.
      Обсудим идею, формат сотрудничества
      и следующий шаг.

    </p>


    <div class="contact-buttons">

      <a
        href="tel:+79895759929"
        class="button button-blue"
      >
        📞 +7 989 575-99-29
      </a>


      <a
        href="mailto:wlly670777@gmail.com"
        class="button button-light"
      >
        ✉️ wlly670777@gmail.com
      </a>

    </div>

  </div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

  <div class="container">

    <div class="footer-content">

      <div>
        © 2026 Digital Future
      </div>

      <div>
        Дизайнер цифровых пространств будущего
      </div>

    </div>

  </div>

</footer>


</body>
</html>
