<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <title>Возврат навязанных услуг при покупке автомобиля</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta
    name="description"
    content="Юридическая помощь по возврату навязанных услуг при покупке автомобиля в автосалоне."
  />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap"
    rel="stylesheet"
  />
  <style>
    :root {
      --blue-dark: #0d47a1;
      --blue: #1565c0;
      --blue-light: #e3f2fd;
      --white: #ffffff;
      --text-main: #0f172a;
      --text-muted: #64748b;
      --danger: #ef4444;
      --border-radius-lg: 18px;
      --border-radius-md: 12px;
      --shadow-soft: 0 18px 50px rgba(15, 23, 42, 0.15);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Inter", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: #f1f5f9;
      color: var(--text-main);
      line-height: 1.5;
    }

    img {
      max-width: 100%;
      display: block;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* Layout */

    .page {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(16px);
      background: rgba(15, 23, 42, 0.75);
      color: var(--white);
    }

    .header-inner {
      max-width: 1120px;
      margin: 0 auto;
      padding: 14px 16px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .logo-mark {
      width: 32px;
      height: 32px;
      border-radius: 10px;
      background: linear-gradient(135deg, var(--blue-dark), var(--blue));
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      font-size: 18px;
    }

    .logo-text-main {
      font-weight: 600;
      font-size: 17px;
    }

    .logo-text-sub {
      font-size: 12px;
      opacity: 0.8;
    }

    nav {
      display: flex;
      gap: 18px;
      font-size: 14px;
      align-items: center;
    }

    nav a {
      opacity: 0.85;
      transition: opacity 0.2s ease, transform 0.2s ease;
    }

    nav a:hover {
      opacity: 1;
      transform: translateY(-1px);
    }

    .nav-cta {
      padding: 8px 16px;
      border-radius: 999px;
      background: var(--white);
      color: var(--blue-dark);
      font-weight: 500;
      box-shadow: 0 10px 25px rgba(15, 23, 42, 0.45);
    }

    main {
      flex: 1;
    }

    .section {
      padding: 56px 16px;
    }

    .container {
      max-width: 1120px;
      margin: 0 auto;
    }

    /* Hero */

    .hero {
      background: radial-gradient(circle at top left, var(--blue-light), #eff6ff);
      padding-top: 40px;
      padding-bottom: 56px;
    }

    .hero-inner {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 32px;
      align-items: center;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 12px;
      border-radius: 999px;
      background: rgba(21, 101, 192, 0.09);
      color: var(--blue-dark);
      font-size: 13px;
      margin-bottom: 16px;
    }

    .badge-dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: #22c55e;
    }

    .hero-title {
      font-size: clamp(26px, 4vw, 34px);
      font-weight: 700;
      margin-bottom: 12px;
      color: #020617;
    }

    .hero-title span {
      color: var(--blue-dark);
    }

    .hero-subtitle {
      font-size: 15px;
      color: var(--text-muted);
      margin-bottom: 24px;
      max-width: 480px;
    }

    .hero-stats {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin-bottom: 24px;
    }

    .hero-stat {
      padding: 10px 16px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.9);
      box-shadow: 0 10px 35px rgba(15, 23, 42, 0.08);
      font-size: 13px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 18px;
    }

    .btn-primary {
      padding: 12px 22px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--blue-dark), var(--blue));
      color: var(--white);
      font-weight: 600;
      border: none;
      cursor: pointer;
      font-size: 14px;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      box-shadow: 0 18px 40px rgba(15, 23, 42, 0.35);
      transition: transform 0.15s ease, box-shadow 0.15s ease, opacity 0.2s ease;
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 24px 50px rgba(15, 23, 42, 0.35);
      opacity: 0.95;
    }

    .btn-outline {
      padding: 11px 20px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.7);
      background: rgba(255, 255, 255, 0.8);
      font-size: 14px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: background 0.15s ease, transform 0.15s ease, box-shadow 0.15s ease;
    }

    .btn-outline:hover {
      background: #f9fafb;
      transform: translateY(-1px);
      box-shadow: 0 14px 35px rgba(15, 23, 42, 0.12);
    }

    .hero-note {
      font-size: 12px;
      color: var(--text-muted);
    }

    .hero-note strong {
      color: var(--blue-dark);
    }

    .hero-media {
      position: relative;
    }

    .hero-card {
      background: linear-gradient(135deg, #0f172a, #1e293b);
      border-radius: 28px;
      padding: 18px 18px 20px;
      color: var(--white);
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: -40%;
      background: radial-gradient(circle at 10% 10%, rgba(59, 130, 246, 0.26), transparent 50%);
      opacity: 0.9;
      pointer-events: none;
    }

    .hero-card-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 12px;
      position: relative;
      z-index: 1;
    }

    .hero-card-title {
      font-size: 13px;
      opacity: 0.9;
    }

    .hero-card-tag {
      padding: 4px 9px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.7);
      font-size: 11px;
    }

    .hero-car-image-wrap {
      position: relative;
      border-radius: 18px;
      overflow: hidden;
      margin-bottom: 12px;
      border: 1px solid rgba(148, 163, 184, 0.45);
    }

    .hero-car-image {
      width: 100%;
      height: 190px;
      object-fit: cover;
      /* Замените URL на свои изображения авто */
      background-image: url("https://images.pexels.com/photos/210019/pexels-photo-210019.jpeg?auto=compress&cs=tinysrgb&w=1200");
      background-size: cover;
      background-position: center;
    }

    .hero-car-overlay {
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(15, 23, 42, 0.85), transparent 45%);
    }

    .hero-car-text {
      position: absolute;
      left: 14px;
      bottom: 12px;
      right: 14px;
      font-size: 13px;
    }

    .hero-car-text strong {
      display: block;
      margin-bottom: 4px;
    }

    .hero-card-footer {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 8px;
      font-size: 11px;
      position: relative;
      z-index: 1;
    }

    .hero-card-pill {
      padding: 8px 10px;
      border-radius: 12px;
      background: rgba(15, 23, 42, 0.85);
      border: 1px solid rgba(148, 163, 184, 0.5);
    }

    .hero-card-pill span {
      display: block;
      font-size: 10px;
      opacity: 0.7;
      margin-bottom: 2px;
    }

    .hero-floating {
      position: absolute;
      right: -4px;
      bottom: -8px;
      transform: translateY(0);
      animation: float 5s ease-in-out infinite;
    }

    .hero-floating-card {
      background: var(--white);
      color: var(--text-main);
      padding: 10px 12px;
      border-radius: 14px;
      font-size: 11px;
      box-shadow: var(--shadow-soft);
      max-width: 190px;
    }

    .hero-floating-card strong {
      display: block;
      margin-bottom: 4px;
      color: var(--blue-dark);
    }

    @keyframes float {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-8px);
      }
    }

    /* Section titles */

    .section-title {
      font-size: 22px;
      font-weight: 700;
      margin-bottom: 10px;
      text-align: left;
      color: #020617;
    }

    .section-subtitle {
      font-size: 14px;
      color: var(--text-muted);
      margin-bottom: 24px;
      max-width: 540px;
    }

    /* Benefits */

    .benefits-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 16px;
    }

    .benefit-card {
      background: var(--white);
      border-radius: var(--border-radius-md);
      padding: 16px 14px;
      box-shadow: 0 12px 35px rgba(15, 23, 42, 0.08);
      border: 1px solid rgba(148, 163, 184, 0.2);
    }

    .benefit-icon {
      width: 30px;
      height: 30px;
      border-radius: 999px;
      background: var(--blue-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 16px;
      margin-bottom: 10px;
    }

    .benefit-title {
      font-weight: 600;
      font-size: 14px;
      margin-bottom: 6px;
    }

    .benefit-text {
      font-size: 13px;
      color: var(--text-muted);
    }

    /* Steps */

    .steps {
      background: #0b1120;
      color: var(--white);
    }

    .steps .section-title {
      color: var(--white);
    }

    .steps .section-subtitle {
      color: rgba(148, 163, 184, 0.9);
    }

    .steps-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 14px;
    }

    .step-card {
      background: rgba(15, 23, 42, 0.9);
      border-radius: var(--border-radius-md);
      padding: 14px 12px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      position: relative;
      overflow: hidden;
    }

    .step-card::before {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at top right, rgba(37, 99, 235, 0.3), transparent 45%);
      opacity: 0.6;
      pointer-events: none;
    }

    .step-number {
      width: 22px;
      height: 22px;
      border-radius: 999px;
      border: 1px solid rgba(129, 140, 248, 0.9);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 11px;
      margin-bottom: 8px;
      background: rgba(15, 23, 42, 0.8);
    }

    .step-title {
      font-size: 13px;
      font-weight: 600;
      margin-bottom: 6px;
    }

    .step-text {
      font-size: 12px;
      color: rgba(148, 163, 184, 0.95);
    }

    /* Cases */

    .cases-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 14px;
    }

    .case-card {
      background: var(--white);
      border-radius: var(--border-radius-md);
      overflow: hidden;
      box-shadow: 0 12px 35px rgba(15, 23, 42, 0.08);
      border: 1px solid rgba(148, 163, 184, 0.25);
      display: flex;
      flex-direction: column;
    }

    .case-image {
      height: 130px;
      background-size: cover;
      background-position: center;
    }

    .case-image--1 {
      background-image: url("https://images.pexels.com/photos/210019/pexels-photo-210019.jpeg?auto=compress&cs=tinysrgb&w=900");
    }

    .case-image--2 {
      background-image: url("https://images.pexels.com/photos/210019/pexels-photo-210019.jpeg?auto=compress&cs=tinysrgb&w=900");
    }

    .case-image--3 {
      background-image: url("https://images.pexels.com/photos/971435/pexels-photo-971435.jpeg?auto=compress&cs=tinysrgb&w=900");
    }

    .case-body {
      padding: 12px 14px 14px;
      font-size: 12px;
    }

    .case-badge {
      display: inline-flex;
      padding: 4px 8px;
      border-radius: 999px;
      font-size: 10px;
      background: rgba(21, 101, 192, 0.08);
      color: var(--blue-dark);
      margin-bottom: 6px;
    }

    .case-title {
      font-weight: 600;
      font-size: 13px;
      margin-bottom: 4px;
    }

    .case-meta {
      display: flex;
      justify-content: space-between;
      gap: 6px;
      font-size: 11px;
      color: var(--text-muted);
      margin-top: 6px;
    }

    /* Contact form */

    .contact {
      background: linear-gradient(135deg, #0b1120, #020617);
      color: var(--white);
    }

    .contact-inner {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 30px;
      align-items: flex-start;
    }

    .contact-info {
      font-size: 14px;
      color: rgba(203, 213, 225, 0.95);
    }

    .contact-info p + p {
      margin-top: 10px;
    }

    .contact-points {
      margin-top: 16px;
      display: grid;
      gap: 10px;
    }

    .contact-point {
      display: flex;
      gap: 8px;
      align-items: flex-start;
      font-size: 13px;
    }

    .contact-dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: #38bdf8;
      margin-top: 5px;
    }

    .contact-form-wrap {
      background: rgba(15, 23, 42, 0.95);
      padding: 18px 16px 18px;
      border-radius: var(--border-radius-lg);
      border: 1px solid rgba(148, 163, 184, 0.45);
      box-shadow: 0 18px 45px rgba(15, 23, 42, 0.9);
    }

    .contact-form-title {
      font-size: 16px;
      font-weight: 600;
      margin-bottom: 6px;
    }

    .contact-form-subtitle {
      font-size: 12px;
      color: rgba(148, 163, 184, 0.9);
      margin-bottom: 14px;
    }

    .form-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px 12px;
      margin-bottom: 10px;
    }

    .form-field {
      display: flex;
      flex-direction: column;
      gap: 4px;
      font-size: 12px;
      color: rgba(226, 232, 240, 0.95);
    }

    .form-field--full {
      grid-column: 1 / -1;
    }

    label span {
      color: #f97316;
    }

    input,
    textarea,
    select {
      border-radius: 10px;
      border: 1px solid rgba(148, 163, 184, 0.7);
      background: rgba(15, 23, 42, 0.9);
      padding: 9px 10px;
      font-size: 13px;
      color: var(--white);
      outline: none;
      transition: border 0.15s ease, box-shadow 0.15s ease, background 0.15s ease;
      font-family: inherit;
      resize: vertical;
    }

    input::placeholder,
    textarea::placeholder {
      color: rgba(148, 163, 184, 0.9);
    }

    input:focus,
    textarea:focus,
    select:focus {
      border-color: #38bdf8;
      box-shadow: 0 0 0 1px #38bdf8;
      background: #020617;
    }

    .form-row-inline {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 12px;
      font-size: 11px;
      color: rgba(148, 163, 184, 0.95);
    }

    .form-row-inline input[type="checkbox"] {
      width: 14px;
      height: 14px;
      border-radius: 4px;
      margin: 0;
    }

    .form-footer {
      display: flex;
      flex-direction: column;
      gap: 6px;
      align-items: flex-start;
    }

    .form-hint {
      font-size: 11px;
      color: rgba(148, 163, 184, 0.9);
    }

    .error-text {
      font-size: 11px;
      color: var(--danger);
      margin-top: 4px;
      display: none;
    }

    .error input,
    .error textarea {
      border-color: var(--danger);
      box-shadow: 0 0 0 1px var(--danger);
    }

    .error .error-text {
      display: block;
    }

    /* Footer */

    footer {
      background: #020617;
      color: rgba(148, 163, 184, 0.9);
      padding: 14px 16px 18px;
      font-size: 11px;
    }

    .footer-inner {
      max-width: 1120px;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 8px;
      align-items: center;
    }

    .footer-links {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .footer-links a {
      text-decoration: underline;
      text-decoration-style: dotted;
      text-underline-offset: 3px;
    }

    /* Responsive */

    @media (max-width: 900px) {
      .hero-inner {
        grid-template-columns: minmax(0, 1fr);
      }
      .hero-media {
        order: -1;
      }
      .contact-inner {
        grid-template-columns: minmax(0, 1fr);
      }
      .contact-form-wrap {
        order: -1;
      }
      .steps-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
      .benefits-grid,
      .cases-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
      nav {
        display: none;
      }
    }

    @media (max-width: 640px) {
      .section {
        padding: 40px 14px;
      }
      .hero {
        padding-top: 26px;
        padding-bottom: 36px;
      }
      .hero-car-image {
        height: 160px;
      }
      .steps-grid,
      .benefits-grid,
      .cases-grid {
        grid-template-columns: minmax(0, 1fr);
      }
      .form-grid {
        grid-template-columns: minmax(0, 1fr);
      }
      .contact-form-wrap {
        padding: 16px 14px;
      }
    }
  </style>
</head>
<body>
  <div class="page">
    <header>
      <div class="header-inner">
        <div class="logo">
          <div class="logo-mark">L</div>
          <div>
            <div class="logo-text-main">LEX AUTO</div>
            <div class="logo-text-sub">Юристы по автосделкам</div>
          </div>
        </div>
        <nav>
          <a href="#benefits">Почему это законно</a>
          <a href="#steps">Как мы работаем</a>
          <a href="#cases">Наши кейсы</a>
          <a href="#contact" class="nav-cta">Оставить заявку</a>
        </nav>
      </div>
    </header>

    <main>
      <!-- HERO -->
      <section class="hero">
        <div class="container hero-inner">
          <div>
            <div class="badge">
              <div class="badge-dot"></div>
              Возвращаем деньги за навязанные услуги в автосалонах
            </div>
            <h1 class="hero-title">
              Вернём <span>навязанные услуги</span> при покупке автомобиля — законно и под ключ
            </h1>
            <p class="hero-subtitle">
              КАСКО, допоборудование, «защита кузова», «расширенная гарантия» и другие услуги,
              без которых вас не хотели отпускать из автосалона. Поможем вернуть деньги или
              существенно снизить переплату.
            </p>

            <div class="hero-stats">
              <div class="hero-stat">До 180&nbsp;дней после покупки авто вы имеете право оспорить сделку</div>
              <div class="hero-stat">Более 1,5 млн ₽ возвращённых клиентам</div>
              <div class="hero-stat">Работаем по договору, оплата — по результату*</div>
            </div>

            <div class="hero-buttons">
              <button class="btn-primary" onclick="scrollToForm()">
                Рассчитать, сколько можно вернуть
                <span>→</span>
              </button>
              <button class="btn-outline" onclick="scrollToForm()">
                Загрузить договор из автосалона
              </button>
            </div>

            <p class="hero-note">
              *Формат оплаты обсуждается индивидуально. <strong>Первичная консультация — бесплатно.</strong>
            </p>
          </div>

          <div class="hero-media">
            <div class="hero-card">
              <div class="hero-card-header">
                <div>
                  <div class="hero-card-title">Ваш кейс</div>
                  <div style="font-size: 11px; opacity: 0.75">
                    Пример возврата навязанных услуг по договору автокредита
                  </div>
                </div>
                <div class="hero-card-tag">
                  ⚖ Разбор договора
                </div>
              </div>

              <div class="hero-car-image-wrap">
                <div class="hero-car-image"></div>
                <div class="hero-car-overlay"></div>
                <div class="hero-car-text">
                  <strong>Автосалон навязал КАСКО, страховки жизни и допы на 320&nbsp;000 ₽</strong>
                  <span>Вернули 247&nbsp;000 ₽ за 45 дней через претензию и переговоры с банком.</span>
                </div>
              </div>

              <div class="hero-card-footer">
                <div class="hero-card-pill">
                  <span>КАСКО + допы</span>
                  180&nbsp;000 ₽
                </div>
                <div class="hero-card-pill">
                  <span>Страхование жизни</span>
                  92&nbsp;000 ₽
                </div>
                <div class="hero-card-pill">
                  <span>Возврат клиенту</span>
                  247&nbsp;000 ₽
                </div>
              </div>
            </div>

            <div class="hero-floating">
              <div class="hero-floating-card">
                <strong>Отправьте фото договора</strong>
                Мы проверим условия кредита и навязанных услуг, расскажем, что можно вернуть,
                и предложим стратегию — без сложных терминов и лишней воды.
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- BENEFITS -->
      <section id="benefits" class="section">
        <div class="container">
          <h2 class="section-title">Почему вы можете вернуть деньги законно</h2>
          <p class="section-subtitle">
            Автосалоны часто нарушают права потребителей: вводят в заблуждение, давят на принятие
            решения, не раскрывают условия кредитования и «пакетных» услуг. Всё это даёт основания
            требовать возврата средств.
          </p>
          <div class="benefits-grid">
            <div class="benefit-card">
              <div class="benefit-icon">⚖</div>
              <div class="benefit-title">Нарушение закона о защите прав потребителей</div>
              <div class="benefit-text">
                Давление, скрытие информации, навязывание дополнительных услуг нарушают ваши
                права и дают нам возможность требовать расторжения или изменения договора.
              </div>
            </div>
            <div class="benefit-card">
              <div class="benefit-icon">📝</div>
              <div class="benefit-title">Право на отказ от страховок</div>
              <div class="benefit-text">
                По многим видам страхования жизни и дополнительных программ можно отказаться и
                вернуть значительную часть суммы, даже спустя время после покупки.
              </div>
            </div>
            <div class="benefit-card">
              <div class="benefit-icon">💰</div>
              <div class="benefit-title">Штрафы и неустойки — в вашу пользу</div>
              <div class="benefit-text">
                При грубых нарушениях автосалон и банк рискуют не только возвратом денег, но и
                выплатой штрафов, пени и компенсации морального вреда.
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- STEPS -->
      <section id="steps" class="section steps">
        <div class="container">
          <h2 class="section-title">Как мы работаем с вашим делом</h2>
          <p class="section-subtitle">
            Наша задача — забрать с вас юридическую рутину. От вас — только документы и краткое
            описание ситуации. Остальное мы берём на себя.
          </p>
          <div class="steps-grid">
            <div class="step-card">
              <div class="step-number">1</div>
              <div class="step-title">Заявка и консультация</div>
              <div class="step-text">
                Оставьте контакты и прикрепите договор/фото документов. Юрист свяжется с вами,
                уточнит детали и предварительно оценит перспективы возврата.
              </div>
            </div>
            <div class="step-card">
              <div class="step-number">2</div>
              <div class="step-title">Анализ договора</div>
              <div class="step-text">
                Изучаем кредитный договор, приложения, страховки, акты, допсоглашения.
                Составляем правовую позицию и план действий: претензия, переговоры, суд.
              </div>
            </div>
            <div class="step-card">
              <div class="step-number">3</div>
              <div class="step-title">Претензия и переговоры</div>
              <div class="step-text">
                Готовим и направляем претензии в автосалон и банк, ведём переписку и переговоры.
                Стремимся к досудебному возврату максимально возможной суммы.
              </div>
            </div>
            <div class="step-card">
              <div class="step-number">4</div>
              <div class="step-title">Суд и возврат средств</div>
              <div class="step-text">
                При необходимости подаём иск, представляем ваши интересы в суде и добиваемся
                возврата денег, штрафа и неустойки. Отчитываемся по результату.
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- CASES -->
      <section id="cases" class="section">
        <div class="container">
          <h2 class="section-title">Примеры наших дел</h2>
          <p class="section-subtitle">
            Каждый кейс индивидуален, но механика нарушений у автосалонов похожа. Вот несколько
            типовых ситуаций, с которыми к нам приходят клиенты.
          </p>
          <div class="cases-grid">
            <div class="case-card">
              <div class="case-image case-image--1"></div>
              <div class="case-body">
                <div class="case-badge">Навязанное КАСКО и допоборудование</div>
                <div class="case-title">Hyundai, кредит через банк, навязанные услуги на 260&nbsp;000 ₽</div>
                <p>
                  Автосалон связал одобрение кредита с покупкой КАСКО и пакета допоборудования.
                  Вернули 198&nbsp;000 ₽ через претензию, без суда.
                </p>
                <div class="case-meta">
                  <span>Срок: 32 дня</span>
                  <span>Регион: Москва</span>
                </div>
              </div>
            </div>

            <div class="case-card">
              <div class="case-image case-image--2"></div>
              <div class="case-body">
                <div class="case-badge">Страхование жизни при автокредите</div>
                <div class="case-title">KIA, страхование жизни на 120&nbsp;000 ₽</div>
                <p>
                  Клиенту сообщили, что без страховки банк «не одобрит» кредит. Оспорили договор
                  страхования, вернули 96&nbsp;000 ₽.
                </p>
                <div class="case-meta">
                  <span>Срок: 28 дней</span>
                  <span>Регион: СПб</span>
                </div>
              </div>
            </div>

            <div class="case-card">
              <div class="case-image case-image--3"></div>
              <div class="case-body">
                <div class="case-badge">«Защита кузова» и расширенная гарантия</div>
                <div class="case-title">VW, допуслуги на 180&nbsp;000 ₽</div>
                <p>
                  В договоре обнаружили завышенную стоимость «защиты кузова» и «расширенной
                  гарантии». Через суд взыскали 180&nbsp;000 ₽ + штраф и неустойку.
                </p>
                <div class="case-meta">
                  <span>Срок: 3,5 месяца</span>
                  <span>Регион: Екатеринбург</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- CONTACT -->
      <section id="contact" class="section contact">
        <div class="container contact-inner">
          <div>
            <h2 class="section-title">Оставьте заявку — разберём вашу ситуацию</h2>
            <p class="section-subtitle">
              Прикрепите договор или просто опишите, что навязал автосалон. Мы проверим документы,
              расскажем, сколько реально можно вернуть, и предложим оптимальный план действий.
            </p>
            <div class="contact-info">
              <p><strong>Что ускорит работу:</strong></p>
              <div class="contact-points">
                <div class="contact-point">
                  <div class="contact-dot"></div>
                  <div>Фото/сканы кредитного договора и всех приложений из автосалона.</div>
                </div>
                <div class="contact-point">
                  <div class="contact-dot"></div>
                  <div>Договоры страхования (жизни, КАСКО, «допзащита» и т.п.).</div>
                </div>
                <div class="contact-point">
                  <div class="contact-dot"></div>
                  <div>СМС от банка, график платежей, чек об оплате допуслуг.</div>
                </div>
              </div>

              <p style="margin-top: 16px; font-size: 13px; color: rgba(148, 163, 184, 0.95)">
                Мы не передаём ваши данные третьим лицам и используем их только для связи по вашему
                обращению. Юрист свяжется с вами в рабочее время.
              </p>
            </div>
          </div>

          <div class="contact-form-wrap">
            <div class="contact-form-title">Форма обратной связи</div>
            <div class="contact-form-subtitle">
              Заполните поля ниже — и мы свяжемся с вами, чтобы обсудить возможный возврат навязанных услуг.
            </div>

            <form id="contactForm" novalidate>
              <div class="form-grid">
                <div class="form-field">
                  <label for="name">Имя <span>*</span></label>
                  <input id="name" name="name" type="text" placeholder="Как к вам обращаться" />
                  <div class="error-text">Укажите ваше имя.</div>
                </div>

                <div class="form-field">
                  <label for="phone">Телефон / WhatsApp <span>*</span></label>
                  <input
                    id="phone"
                    name="phone"
                    type="tel"
                    placeholder="+7 (___) ___-__-__"
                  />
                  <div class="error-text">Укажите номер телефона для связи.</div>
                </div>

                <div class="form-field">
                  <label for="dealer">Автосалон / дилер</label>
                  <input
                    id="dealer"
                    name="dealer"
                    type="text"
                    placeholder="Название автосалона"
                  />
                </div>

                <div class="form-field">
                  <label for="city">Город</label>
                  <input id="city" name="city" type="text" placeholder="Ваш город" />
                </div>

                <div class="form-field form-field--full">
                  <label for="services">Какие услуги навязали? <span>*</span></label>
                  <textarea
                    id="services"
                    name="services"
                    rows="3"
                    placeholder="Например: КАСКО, страхование жизни, защита кузова, допоборудование…"
                  ></textarea>
                  <div class="error-text">Кратко опишите, какие услуги вам навязали.</div>
                </div>

                <div class="form-field form-field--full">
                  <label for="sum">Примерная сумма навязанных услуг</label>
                  <input
                    id="sum"
                    name="sum"
                    type="text"
                    placeholder="Например: около 250 000 ₽"
                  />
                </div>
              </div>

              <div class="form-row-inline">
                <input type="checkbox" id="policy" name="policy" />
                <label for="policy">
                  Я даю согласие на обработку персональных данных и согласен(на) с
                  <a href="#!" style="text-decoration: underline">политикой конфиденциальности</a>.
                </label>
              </div>

              <div class="form-footer">
                <button type="submit" class="btn-primary">
                  Отправить заявку юристу
                  <span>→</span>
                </button>
                <div class="form-hint">
                  Нажимая на кнопку, вы соглашаетесь на обработку данных. Мы не рассылаем спам и не
                  передаём контакты третьим лицам.
                </div>
              </div>
            </form>
          </div>
        </div>
      </section>
    </main>

    <footer>
      <div class="footer-inner">
        <div>© 2025 «LEX AUTO». Все права защищены. Не является публичной офертой.</div>
        <div class="footer-links">
          <a href="#!">Политика конфиденциальности</a>
          <a href="#!">Согласие на обработку ПДн</a>
        </div>
      </div>
    </footer>
  </div>

  <script>
    // Плавный скролл к форме
    function scrollToForm() {
      const formSection = document.getElementById("contact");
      if (formSection) {
        formSection.scrollIntoView({ behavior: "smooth" });
      }
    }

    // Простая валидация формы
    document.getElementById("contactForm").addEventListener("submit", function (e) {
      e.preventDefault();

      const form = e.target;
      let isValid = true;

      const requiredFields = [
        { id: "name" },
        { id: "phone" },
        { id: "services" },
      ];

      requiredFields.forEach((field) => {
        const input = form.querySelector("#" + field.id);
        const fieldWrapper = input.closest(".form-field");

        if (!input.value.trim()) {
          fieldWrapper.classList.add("error");
          isValid = false;
        } else {
          fieldWrapper.classList.remove("error");
        }
      });

      if (!isValid) {
        return;
      }

      // Здесь вы можете подключить отправку формы на сервер (AJAX/fetch)
      alert("Спасибо! Ваша заявка отправлена. Мы свяжемся с вами в ближайшее время.");
      form.reset();
    });
  </script>
</body>
</html>
