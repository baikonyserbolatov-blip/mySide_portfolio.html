<!doctype html>
<html lang="kk">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Портфолио — Байқоныc Ерболат</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f1724;
      --card:#0b1220;
      --muted:#94a3b8;
      --accent:#60a5fa;
      --glass: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,#071023 0%, #071428 60%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:24px;
    }
    .container{max-width:1000px;margin:0 auto;}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:12px}
    .avatar{width:56px;height:56px;border-radius:8px;object-fit:cover;border:2px solid rgba(255,255,255,0.06)}
    h1{margin:0;font-size:1.15rem;font-weight:700}
    p.lead{margin:0;color:var(--muted);font-size:0.95rem}

    nav.desktop{display:flex;gap:12px}
    nav a{color:var(--muted);text-decoration:none;padding:8px;border-radius:8px;font-size:0.95rem}
    nav a:hover{background:var(--glass);color:#fff}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 320px;gap:20px;align-items:center;margin-top:28px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:20px;border-radius:12px;box-shadow:0 6px 18px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03)}
    .bio{font-size:0.98rem;color:#dbeafe}
    .actions{margin-top:14px;display:flex;gap:10px;flex-wrap:wrap}
    .btn{display:inline-block;padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:600}
    .btn-primary{background:linear-gradient(90deg,var(--accent),#3b82f6);color:#001529}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted)}

    /* Projects */
    #projects{margin-top:28px}
    .projects-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}
    .proj{display:flex;flex-direction:column;gap:10px;overflow:hidden}
    .proj img{width:100%;height:160px;object-fit:cover;border-radius:8px}
    .proj h3{margin:0;font-size:1rem}
    .tags{display:flex;gap:8px;flex-wrap:wrap}
    .tag{font-size:0.8rem;padding:6px 8px;border-radius:8px;background:rgba(255,255,255,0.03);color:var(--muted)}

    /* Skills & contact */
    .side{display:flex;flex-direction:column;gap:12px}
    .skills{display:flex;gap:8px;flex-wrap:wrap}
    .skill{background:rgba(255,255,255,0.02);padding:8px 10px;border-radius:8px;color:var(--muted);font-weight:600}

    footer{margin-top:32px;color:var(--muted);font-size:0.9rem;text-align:center}

    /* Responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr}
      .projects-grid{grid-template-columns:1fr}
      nav.desktop{display:none}
    }

    /* Mobile nav simple button */
    .mobile-toggle{display:none}
    @media (max-width:900px){.mobile-toggle{display:inline-flex;align-items:center;gap:8px;background:transparent;border:1px solid rgba(255,255,255,0.04);padding:8px;border-radius:8px;color:var(--muted)}}

    /* Modal */
    .modal-back{position:fixed;inset:0;background:rgba(2,6,23,0.6);display:none;align-items:center;justify-content:center;padding:20px;z-index:50}
    .modal{background:linear-gradient(180deg,#071428,#041024);padding:18px;border-radius:12px;max-width:720px;width:100%;border:1px solid rgba(255,255,255,0.04)}
    .modal img{width:100%;height:280px;object-fit:cover;border-radius:8px}
    .modal .close{display:inline-block;margin-top:10px;padding:8px 12px;border-radius:8px;background:transparent;border:1px solid rgba(255,255,255,0.06);cursor:pointer;color:var(--muted)}

    /* small tweaks */
    .muted{color:var(--muted)}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <img class="avatar" src="https://placehold.co/200x200?text=BE" alt="avatar">
        <div>
          <h1>Байконы Ерболат</h1>
          <p class="lead">Frontend Developer • UI/UX enthusiast • Алматы, Қазақстан</p>
        </div>
      </div>

      <div style="display:flex;align-items:center;gap:10px">
        <button class="mobile-toggle" id="toggleBtn">Меню ☰</button>
        <nav class="desktop" id="desktopNav">
          <a href="#projects">Жобалар</a>
          <a href="#skills">Дағдылар</a>
          <a href="#contact">Байланыс</a>
          <a href="#" onclick="window.open('https://github.com/yourusername','_blank')">GitHub</a>
        </nav>
      </div>
    </header>

    <section class="hero" aria-label="Hero section">
      <div class="card">
        <p style="font-size:0.9rem;color:var(--muted);margin:0 0 8px 0">Сәлем! Мен веб-интерфейстер мен веб-қосымшаларды жасаймын.</p>
        <h2 style="margin:0 0 10px 0">Жаңа жобалар, таза дизайн, жылдам фронтенд</h2>
        <p class="bio">Менің фокустарым — React, Vanilla JS, адаптивті дизайн және UI/UX. Төменде таңдаулы проектерім бар — әрқайсысының қысқаша сипаттамасы және сілтемесі көрсетілген.</p>

        <div class="actions">
          <a class="btn btn-primary" href="#projects">Жобаларымды қарау</a>
          <a class="btn btn-ghost" href="#contact">Хабарласу</a>
        </div>

        <div style="margin-top:14px" class="muted">
          Электрондық пошта: <a href="mailto:youremail@example.com" style="color:inherit;text-decoration:underline">youremail@example.com</a>
        </div>
      </div>

      <aside class="side">
        <div class="card">
          <h3 style="margin:0 0 10px 0">Дағдылар</h3>
          <div class="skills" id="skills">
            <span class="skill">HTML</span>
            <span class="skill">CSS</span>
            <span class="skill">JavaScript</span>
            <span class="skill">React</span>
            <span class="skill">Tailwind</span>
            <span class="skill">Figma</span>
            <span class="skill">Git</span>
          </div>
        </div>

        <div class="card">
          <h3 style="margin:0 0 10px 0">Қысқаша CV</h3>
          <p class="muted" style="margin:0 0 8px 0">React, SPA, адаптивті дизайн, REST API, негіздер — UI/UX принцптері.</p>
          <a class="btn btn-ghost" href="#" onclick="alert('PDF-ні жүктеу опциясын қосыңыз')">CV жүктеу</a>
        </div>
      </aside>
    </section>

    <section id="projects">
      <h2 style="margin-top:28px">Таңдаулы жобалар</h2>
      <div class="projects-grid">
        <!-- Project 1 -->
        <article class="proj card" data-title="Веб-қосымша (React)" data-desc="SPA — аутентификация, REST API интеграциясы. React + Context + Axios." data-img="https://placehold.co/800x450?text=Project+1">
          <img src="https://placehold.co/800x450?text=Project+1" alt="Project 1">
          <div>
            <h3>Веб-қосымша (React)</h3>
            <p class="muted" style="margin:6px 0 10px 0;font-size:0.95rem">React негізіндегі SPA: тіркелу, профиль және динамикалық контент.</p>
            <div class="tags">
              <span class="tag">React</span><span class="tag">API</span><span class="tag">Auth</span>
            </div>
            <div style="margin-top:10px">
              <button class="btn btn-primary" onclick="openModal(this)">Көру</button>
              <a class="btn btn-ghost" href="#" onclick="window.open('#')">Сілтеме</a>
            </div>
          </div>
        </article>

        <!-- Project 2 -->
        <article class="proj card" data-title="E-commerce дүкен" data-desc="Simple e-commerce: каталог, себет, төлем тұжырымдамасы." data-img="https://placehold.co/800x450?text=Project+2">
          <img src="https://placehold.co/800x450?text=Project+2" alt="Project 2">
          <div>
            <h3>E-commerce дүкен</h3>
            <p class="muted" style="margin:6px 0 10px 0">Тауарлар каталогы және себет. Backend үшін Node/Express ұсынылады.</p>
            <div class="tags">
              <span class="tag">Next.js</span><span class="tag">Stripe</span><span class="tag">Shop</span>
            </div>
            <div style="margin-top:10px">
              <button class="btn btn-primary" onclick="openModal(this)">Көру</button>
              <a class="btn btn-ghost" href="#" onclick="window.open('#')">Сілтеме</a>
            </div>
          </div>
        </article>

        <!-- Project 3 -->
        <article class="proj card" data-title="UI/UX прототип" data-desc="Figma прототипі, мобиль және веб флоу." data-img="https://placehold.co/800x450?text=Project+3">
          <img src="https://placehold.co/800x450?text=Project+3" alt="Project 3">
          <div>
            <h3>UI/UX прототип</h3>
            <p class="muted" style="margin:6px 0 10px 0">Пайдаланушы флоулары, интеракциялар және компонент кітапхана.</p>
            <div class="tags">
              <span class="tag">Figma</span><span class="tag">Prototype</span>
            </div>
            <div style="margin-top:10px">
              <button class="btn btn-primary" onclick="openModal(this)">Көру</button>
              <a class="btn btn-ghost" href="#" onclick="window.open('#')">Сілтеме</a>
            </div>
          </div>
        </article>

        <!-- Project 4 (example) -->
        <article class="proj card" data-title="Портфолио сайт" data-desc="Бұл өзі — ағымдағы портфолио сайтым. HTML/CSS/JS single-file." data-img="https://placehold.co/800x450?text=This+Portfolio">
          <img src="https://placehold.co/800x450?text=This+Portfolio" alt="This portfolio">
          <div>
            <h3>Портфолио сайт</h3>
            <p class="muted" style="margin:6px 0 10px 0">Шаршы, жылдам және тек бір файлда.</p>
            <div class="tags">
              <span class="tag">HTML</span><span class="tag">CSS</span><span class="tag">JS</span>
            </div>
            <div style="margin-top:10px">
              <button class="btn btn-primary" onclick="openModal(this)">Көру</button>
              <a class="btn btn-ghost" href="#" onclick="window.open('#')">Сілтеме</a>
            </div>
          </div>
        </article>
      </div>
    </section>

    <footer id="contact">
      <div class="card" style="display:inline-block;margin-top:16px">
        <h3 style="margin:0 0 8px 0">Байланыс</h3>
        <p class="muted" style="margin:0 0 10px 0">Эл. пошта: <a href="mailto:youremail@example.com" style="color:inherit;text-decoration:underline">youremail@example.com</a></p>
        <p class="muted" style="margin:0">Телефон / Telegram: +7 (7xx) xxx-xx-xx</p>
      </div>

      <div style="margin-top:14px">© <span id="year"></span> Байконы Ерболат — Барлық құқықтар қорғалған.</div>
    </footer>
  </div>

  <!-- Modal -->
  <div class="modal-back" id="modal">
    <div class="modal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
      <h3 id="modalTitle" style="margin:0 0 8px 0"></h3>
      <img id="modalImg" src="" alt="">
      <p id="modalDesc" style="margin-top:10px;color:var(--muted)"></p>
      <div style="margin-top:12px">
        <button class="close" onclick="closeModal()" aria-label="close">Жабу</button>
      </div>
    </div>
  </div>

  <script>
    // Small JS: mobile toggle, modal, year
    document.getElementById('year').textContent = new Date().getFullYear();

    const toggleBtn = document.getElementById('toggleBtn');
    toggleBtn.addEventListener('click', ()=>{
      const nav = document.getElementById('desktopNav');
      if(nav.style.display === 'flex') nav.style.display = '';
      else nav.style.display = 'flex';
    });

    function openModal(btn){
      // find containing article
      const art = btn.closest('article');
      const title = art.getAttribute('data-title') || art.querySelector('h3').innerText;
      const desc = art.getAttribute('data-desc') || art.querySelector('p').innerText;
      const img = art.getAttribute('data-img') || art.querySelector('img').src;
      document.getElementById('modalTitle').innerText = title;
      document.getElementById('modalDesc').innerText = desc;
      document.getElementById('modalImg').src = img;
      document.getElementById('modal').style.display = 'flex';
      document.body.style.overflow = 'hidden';
    }
    function closeModal(){
      document.getElementById('modal').style.display = 'none';
      document.body.style.overflow = '';
    }
    // close modal on background click
    document.getElementById('modal').addEventListener('click', function(e){
      if(e.target === this) closeModal();
    });

    // Accessibility: close modal on Esc
    document.addEventListener('keydown', function(e){
      if(e.key === 'Escape') closeModal();
    });
  </script>
</body>
</html>
