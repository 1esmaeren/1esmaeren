<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Esma Eren — GitHub Profil</title>
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: #0a0a0f;
      color: #f0eaf5;
      min-height: 100vh;
      padding-bottom: 60px;
      position: relative;
      overflow-x: hidden;
    }

    .bg-grid {
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(rgba(255,105,180,0.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,105,180,0.04) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
      z-index: 0;
    }

    .bg-orb {
      position: fixed;
      border-radius: 50%;
      filter: blur(80px);
      pointer-events: none;
      z-index: 0;
    }
    .orb1 { width: 320px; height: 320px; background: rgba(255,105,180,0.12); top: -80px; right: -60px; }
    .orb2 { width: 200px; height: 200px; background: rgba(160,100,220,0.08); bottom: 100px; left: -60px; }

    .container {
      position: relative;
      z-index: 1;
      max-width: 680px;
      margin: 0 auto;
      padding: 0 32px;
    }

    /* HERO */
    .hero {
      padding: 60px 0 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
    }

    .avatar-ring {
      width: 96px;
      height: 96px;
      border-radius: 50%;
      background: linear-gradient(135deg, #ff69b4, #a064dc, #ff69b4);
      padding: 2px;
      margin-bottom: 24px;
      animation: spin-slow 8s linear infinite;
    }
    @keyframes spin-slow {
      from { transform: rotate(0deg); }
      to   { transform: rotate(360deg); }
    }
    .avatar-inner {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background: #0a0a0f;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'DM Serif Display', serif;
      font-size: 28px;
      color: #ff69b4;
      animation: spin-slow 8s linear infinite reverse;
    }

    .hero-name {
      font-family: 'DM Serif Display', serif;
      font-size: 38px;
      letter-spacing: -0.5px;
      background: linear-gradient(135deg, #ff69b4 0%, #e8a0d0 50%, #c084fc 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 6px;
    }

    .hero-title {
      font-size: 13px;
      font-weight: 300;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: rgba(240,234,245,0.45);
      margin-bottom: 20px;
    }

    .hero-quote {
      font-family: 'DM Serif Display', serif;
      font-style: italic;
      font-size: 16px;
      color: rgba(240,234,245,0.55);
      border-left: 2px solid rgba(255,105,180,0.4);
      padding-left: 16px;
      text-align: left;
      max-width: 280px;
      margin-bottom: 28px;
      line-height: 1.6;
    }

    .social-links {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .social-btn {
      display: flex;
      align-items: center;
      gap: 7px;
      padding: 8px 16px;
      border-radius: 40px;
      border: 0.5px solid rgba(255,105,180,0.25);
      background: rgba(255,105,180,0.06);
      color: rgba(240,234,245,0.75);
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-decoration: none;
      transition: all 0.2s;
    }
    .social-btn:hover {
      background: rgba(255,105,180,0.14);
      border-color: rgba(255,105,180,0.5);
      color: #ff69b4;
      transform: translateY(-1px);
    }
    .social-btn svg { width: 14px; height: 14px; flex-shrink: 0; }

    /* DIVIDER */
    .divider {
      width: 60px;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,105,180,0.5), transparent);
      margin: 36px auto;
    }

    /* SECTION */
    .section { margin-bottom: 0; }

    .section-label {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: rgba(255,105,180,0.6);
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .section-label::after {
      content: '';
      flex: 1;
      height: 0.5px;
      background: rgba(255,105,180,0.15);
    }

    /* ABOUT */
    .about-text {
      font-size: 15px;
      line-height: 1.85;
      color: rgba(240,234,245,0.65);
      font-weight: 300;
    }
    .about-text em {
      color: rgba(255,105,180,0.85);
      font-style: normal;
      font-weight: 400;
    }

    /* TECH */
    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .tech-chip {
      padding: 7px 14px;
      border-radius: 6px;
      border: 0.5px solid rgba(255,105,180,0.2);
      background: rgba(255,105,180,0.05);
      font-size: 12px;
      font-weight: 500;
      color: rgba(240,234,245,0.7);
      letter-spacing: 0.3px;
      display: flex;
      align-items: center;
      gap: 7px;
      transition: all 0.2s;
      cursor: default;
    }
    .tech-chip:hover {
      border-color: rgba(255,105,180,0.45);
      background: rgba(255,105,180,0.1);
      color: #f0eaf5;
      transform: translateY(-1px);
    }
    .tech-dot {
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background: #ff69b4;
      opacity: 0.7;
      flex-shrink: 0;
    }

    /* PROJECT */
    .project-card {
      border: 0.5px solid rgba(255,105,180,0.18);
      border-radius: 16px;
      background: rgba(255,105,180,0.04);
      padding: 28px;
      position: relative;
      overflow: hidden;
      transition: all 0.25s;
    }
    .project-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(255,105,180,0.5), transparent);
    }
    .project-card:hover {
      border-color: rgba(255,105,180,0.35);
      background: rgba(255,105,180,0.07);
      transform: translateY(-2px);
    }

    .project-icon {
      width: 44px;
      height: 44px;
      border-radius: 10px;
      background: rgba(255,105,180,0.12);
      border: 0.5px solid rgba(255,105,180,0.25);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      margin-bottom: 16px;
    }

    .project-name {
      font-family: 'DM Serif Display', serif;
      font-size: 20px;
      color: #f0eaf5;
      margin-bottom: 8px;
    }
    .project-name span {
      font-size: 13px;
      font-weight: 300;
      font-family: 'DM Sans', sans-serif;
      color: rgba(255,105,180,0.7);
      margin-left: 8px;
    }

    .project-desc {
      font-size: 14px;
      line-height: 1.75;
      color: rgba(240,234,245,0.55);
      font-weight: 300;
      margin-bottom: 20px;
    }

    .project-tags {
      display: flex;
      gap: 6px;
      flex-wrap: wrap;
      margin-bottom: 20px;
    }
    .tag {
      font-size: 11px;
      padding: 3px 10px;
      border-radius: 4px;
      background: rgba(255,105,180,0.08);
      border: 0.5px solid rgba(255,105,180,0.2);
      color: rgba(255,105,180,0.8);
      font-weight: 500;
      letter-spacing: 0.3px;
    }

    .project-links { display: flex; gap: 10px; }

    .proj-btn {
      display: flex;
      align-items: center;
      gap: 6px;
      padding: 8px 18px;
      border-radius: 8px;
      font-size: 12px;
      font-weight: 500;
      text-decoration: none;
      transition: all 0.2s;
      letter-spacing: 0.3px;
      font-family: 'DM Sans', sans-serif;
    }
    .proj-btn.primary {
      background: rgba(255,105,180,0.2);
      border: 0.5px solid rgba(255,105,180,0.4);
      color: #ff69b4;
    }
    .proj-btn.primary:hover { background: rgba(255,105,180,0.3); }
    .proj-btn.secondary {
      background: rgba(240,234,245,0.04);
      border: 0.5px solid rgba(240,234,245,0.12);
      color: rgba(240,234,245,0.6);
    }
    .proj-btn.secondary:hover { background: rgba(240,234,245,0.08); color: #f0eaf5; }

    /* STATS */
    .stats-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }
    .stat-card {
      border: 0.5px solid rgba(255,105,180,0.15);
      border-radius: 12px;
      overflow: hidden;
      background: rgba(15,10,20,0.5);
    }
    .stat-card img {
      width: 100%;
      display: block;
      opacity: 0.9;
    }
    .stat-card-full {
      border: 0.5px solid rgba(255,105,180,0.15);
      border-radius: 12px;
      overflow: hidden;
      background: rgba(15,10,20,0.5);
      margin-top: 12px;
    }
    .stat-card-full img {
      width: 100%;
      display: block;
      opacity: 0.85;
    }

    /* FOOTER */
    .footer {
      text-align: center;
      padding-top: 48px;
      font-size: 12px;
      color: rgba(240,234,245,0.2);
      letter-spacing: 1px;
    }
  </style>
</head>
<body>

  <div class="bg-grid"></div>
  <div class="bg-orb orb1"></div>
  <div class="bg-orb orb2"></div>

  <div class="container">

    <!-- HERO -->
    <div class="hero">
      <div class="avatar-ring">
        <div class="avatar-inner">E</div>
      </div>

      <h1 class="hero-name">Esma Eren</h1>
      <p class="hero-title">Endüstri Mühendisi &nbsp;·&nbsp; Bilgi İşlem</p>

      <blockquote class="hero-quote">
        "Sade düşün, doğru çöz."
      </blockquote>

      <div class="social-links">
        <a class="social-btn" href="mailto:esma_eren147@hotmail.com">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
            <path d="M3 8l9 6 9-6M3 8v10a1 1 0 001 1h16a1 1 0 001-1V8M3 8a1 1 0 011-1h16a1 1 0 011 1"/>
          </svg>
          Hotmail
        </a>
        <a class="social-btn" href="https://github.com/1esmaeren">
          <svg viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/>
          </svg>
          GitHub
        </a>
        <a class="social-btn" href="https://www.linkedin.com/in/esma-eren-5b2925158/">
          <svg viewBox="0 0 24 24" fill="currentColor">
            <path d="M19 3a2 2 0 012 2v14a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h14m-.5 15.5v-5.3a3.26 3.26 0 00-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 011.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 001.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 00-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/>
          </svg>
          LinkedIn
        </a>
      </div>
    </div>

    <div class="divider"></div>

    <!-- ABOUT -->
    <div class="section">
      <p class="section-label">Hakkımda</p>
      <p class="about-text">
        Endüstri mühendisiyim; şu an <em>bilgi işlem</em> alanında çalışıyorum.<br><br>
        Mesleğimin getirdiği analitik bakış açısıyla <em>süreç modelleme</em>,
        <em>simülasyon</em> ve veri odaklı çözümlere ilgi duyuyorum.
      </p>
    </div>

    <div class="divider"></div>

    <!-- TECH -->
    <div class="section">
      <p class="section-label">Teknolojiler</p>
      <div class="tech-grid">
        <div class="tech-chip"><span class="tech-dot"></span>JavaScript</div>
        <div class="tech-chip"><span class="tech-dot"></span>HTML5</div>
        <div class="tech-chip"><span class="tech-dot"></span>CSS3</div>
        <div class="tech-chip"><span class="tech-dot"></span>PHP</div>
        <div class="tech-chip"><span class="tech-dot"></span>MySQL</div>
      </div>
    </div>

    <div class="divider"></div>

    <!-- PROJECT -->
    <div class="section">
      <p class="section-label">Öne Çıkan Proje</p>
      <div class="project-card">
        <div class="project-icon">🏭</div>
        <h3 class="project-name">VSM Studio <span>Üretim Hattı Simülatörü</span></h3>
        <p class="project-desc">
          Sürükle-bırak arayüzüyle üretim hattı kurun; gerçek zamanlı simülasyon ile
          darboğazları ve kayıpları anında görün.
        </p>
        <div class="project-tags">
          <span class="tag">JavaScript</span>
          <span class="tag">HTML5</span>
          <span class="tag">Tarayıcıda Çalışır</span>
        </div>
        <div class="project-links">
          <a class="proj-btn primary" href="https://1esmaeren.github.io/simulasyon">
            <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M18 13v6a2 2 0 01-2 2H5a2 2 0 01-2-2V8a2 2 0 012-2h6M15 3h6v6M10 14L21 3"/>
            </svg>
            Canlı Demo
          </a>
          <a class="proj-btn secondary" href="https://github.com/1esmaeren/simulasyon">
            <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/>
            </svg>
            Kaynak Kod
          </a>
        </div>
      </div>
    </div>

    <div class="divider"></div>

    <!-- STATS -->
    <div class="section">
      <p class="section-label">GitHub İstatistikleri</p>
      <div class="stats-grid">
        <div class="stat-card">
          <img
            src="https://github-readme-stats.vercel.app/api?username=1esmaeren&show_icons=true&title_color=ff69b4&icon_color=ff69b4&text_color=c084fc&bg_color=0d1117&locale=tr&hide_border=true"
            alt="GitHub Stats"
          />
        </div>
        <div class="stat-card">
          <img
            src="https://github-readme-stats.vercel.app/api/top-langs/?username=1esmaeren&layout=compact&title_color=ff69b4&text_color=c084fc&bg_color=0d1117&locale=tr&hide_border=true"
            alt="Top Languages"
          />
        </div>
      </div>
      <div class="stat-card-full">
        <img
          src="https://github-readme-streak-stats.herokuapp.com/?user=1esmaeren&theme=dark&background=0D1117&currStreakLabel=ff69b4&sideLabels=c084fc&dates=888888&ring=ff69b4&fire=ff69b4&currStreakNum=ffffff&hide_border=true&locale=tr"
          alt="GitHub Streak"
        />
      </div>
      <div class="stat-card-full">
        <img
          src="https://github-readme-activity-graph.vercel.app/graph?username=1esmaeren&bg_color=0d1117&color=c084fc&line=ff69b4&point=ffb6c1&area=true&hide_border=true"
          alt="Activity Graph"
        />
      </div>
    </div>

    <p class="footer">esma eren · 2025</p>

  </div>
</body>
</html>
