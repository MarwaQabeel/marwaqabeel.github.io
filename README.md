<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Marwa Qabeel — Data & AI Portfolio</title>

  <!-- SEO / Social -->
  <meta name="description" content="Marwa Qabeel — ML Engineer / Data Scientist. Projects, resume, and credentials." />
  <meta property="og:title" content="Marwa Qabeel — Data & AI" />
  <meta property="og:description" content="Selected projects, resume, skills, and certificates." />
  <meta property="og:image" content="/assets/og-cover.jpg" />
  <meta name="twitter:card" content="summary_large_image" />
  <link rel="icon" href="/assets/favicon.ico" />

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{--bg:#0b1220;--panel:#101a31;--panel-2:#0e162b;--text:#eaf0ff;--muted:#b6c1e2;--accent:#7aa2ff;--accent-2:#8ee2ff;--ring:rgba(122,162,255,.35);--ok:#47d17e;--shadow:0 10px 24px rgba(5,15,40,.55),0 4px 10px rgba(0,0,0,.25)}
    html,body{margin:0} html{scroll-behavior:smooth}
    body{font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif;background:linear-gradient(180deg,#0a1020 0%,#0c1425 60%,#0a0f20 100%);color:var(--text);-webkit-font-smoothing:antialiased}
    a{color:var(--accent);text-decoration:none} a:hover{text-decoration:underline}

    /* Nav */
    .topnav{position:sticky;top:0;z-index:50;backdrop-filter:saturate(140%) blur(10px);background:rgba(9,14,30,.55);border-bottom:1px solid rgba(255,255,255,.08);display:flex;align-items:center;justify-content:space-between;padding:10px 16px}
    .brand{font-weight:800;letter-spacing:.5px;color:var(--text)}
    .links{display:flex;gap:16px}
    .topnav a{color:var(--text)} .topnav a.active{border-bottom:2px solid var(--accent)}
    .nav-toggle{display:none;background:none;border:0;color:var(--text);font-size:20px}
    @media(max-width:760px){.links{display:none}.topnav.open .links{display:flex;flex-direction:column;position:absolute;right:12px;top:48px;background:rgba(9,14,30,.95);padding:10px 12px;border-radius:12px;border:1px solid rgba(255,255,255,.08)}.nav-toggle{display:block}}

    /* Hero */
    .hero{min-height:100vh;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden;background:radial-gradient(1200px 1200px at 50% -10%,rgba(138,167,255,.08),transparent 60%)}
    .hero .rings{position:absolute;inset:-10% -10% auto -10%;pointer-events:none;opacity:.7}
    .hero .rings span{position:absolute;border:1px solid rgba(255,255,255,.16);border-radius:50%;left:50%;top:50%;transform:translate(-50%,-50%)}
    .hero .rings span:nth-child(1){width:420px;height:420px}.hero .rings span:nth-child(2){width:660px;height:660px;border-color:rgba(255,255,255,.12)}
    .hero .rings span:nth-child(3){width:900px;height:900px;border-color:rgba(255,255,255,.08)}.hero .rings span:nth-child(4){width:1200px;height:1200px;border-color:rgba(255,255,255,.06)}
    .hero .rings span:nth-child(5){width:1600px;height:1600px;border-color:rgba(255,255,255,.05)}
    .content{text-align:center;z-index:1;padding:24px;position:relative}
    .avatar{width:116px;height:116px;border-radius:999px;object-fit:cover;border:2px solid rgba(255,255,255,.35);box-shadow:0 10px 24px rgba(0,0,0,.35);margin:0 auto 16px}
    .role{letter-spacing:.5em;text-transform:uppercase;color:var(--muted);font-size:12px;margin-bottom:8px}
    h1{font-size:56px;line-height:1.05;margin:6px 0 10px}@media(min-width:900px){h1{font-size:72px}}
    .sub{color:var(--muted);max-width:720px;margin:0 auto 18px}
    .quicklinks{display:flex;justify-content:center;gap:12px;flex-wrap:wrap;margin-top:14px}
    .btn{display:inline-flex;align-items:center;gap:8px;font-weight:600;background:linear-gradient(180deg,rgba(122,162,255,.22),rgba(122,162,255,.12));border:1px solid rgba(122,162,255,.45);padding:10px 12px;border-radius:12px;color:var(--text)}
    .quicklinks a{display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:999px;border:1px solid rgba(255,255,255,.16);background:rgba(255,255,255,.05)}
    .quicklinks a.primary{border-color:rgba(122,162,255,.55);background:linear-gradient(180deg,rgba(122,162,255,.22),rgba(122,162,255,.12))}
    .social{position:absolute;left:24px;top:24px;display:flex;gap:14px}.social svg{width:22px;height:22px;fill:currentColor;color:var(--muted)}
    .scroll-indicator{position:absolute;bottom:22px;left:50%;transform:translateX(-50%);width:36px;height:36px;border-radius:999px;border:1px solid rgba(255,255,255,.2);display:grid;place-items:center}
    .scroll-indicator svg{width:18px;height:18px;color:var(--muted)}

    /* Cats (toggle) */
    .cats{position:absolute;inset:0;pointer-events:none;opacity:.25}
    .cats .paw{position:absolute;width:32px;height:32px;background-repeat:no-repeat;background-size:contain;animation:drift 26s linear infinite;background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64' fill='%23b6c1e2'><circle cx='18' cy='18' r='7'/><circle cx='32' cy='12' r='6'/><circle cx='46' cy='18' r='7'/><path d='M16 40c4-9 28-9 32 0-3 8-11 14-16 14s-13-6-16-14z'/></svg>")}
    @keyframes drift{0%{transform:translateY(40vh) rotate(0)}100%{transform:translateY(-70vh) rotate(18deg)}}
    .cats .paw:nth-child(1){left:8%;animation-duration:28s}.cats .paw:nth-child(2){left:26%;animation-duration:32s;animation-delay:4s}
    .cats .paw:nth-child(3){left:44%;animation-duration:29s;animation-delay:8s}.cats .paw:nth-child(4){left:62%;animation-duration:31s;animation-delay:2s}
    .cats .paw:nth-child(5){left:78%;animation-duration:27s;animation-delay:6s}.cats .paw:nth-child(6){left:90%;animation-duration:34s;animation-delay:10s}
    .cats-off .cats{display:none} @media (prefers-reduced-motion:reduce){.cats{display:none}}

    /* Layout + cards */
    .wrap{max-width:1100px;margin:0 auto;padding:28px 20px 64px}
    .section{margin-top:28px}.section h2{font-size:20px;margin:0 0 14px}
    .grid{display:grid;grid-template-columns:repeat(12,1fr);gap:14px}
    .card{grid-column:span 12;background:linear-gradient(180deg,var(--panel),var(--panel-2));border:1px solid rgba(255,255,255,.06);border-radius:18px;box-shadow:var(--shadow);position:relative;overflow:hidden}
    .card:hover{transform:translateY(-2px);transition:transform .2s ease}
    .card .hd{display:flex;justify-content:space-between;gap:8px;padding:16px 18px;border-bottom:1px solid rgba(255,255,255,.06)}
    .card .hd .name{font-weight:700}.card .hd .org{color:var(--muted)}
    .card .body{padding:14px 18px}
    .list{display:grid;gap:8px;margin:12px 0 2px;padding:0;list-style:none}
    .list li{display:flex;justify-content:space-between;align-items:center;gap:12px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);border-radius:12px;padding:10px 12px}
    .course{font-weight:600}
    .badge{font-size:12px;font-weight:700;color:#06230f;background:linear-gradient(180deg,#6cf3a2,#38d878);border:1px solid rgba(0,0,0,.15);padding:4px 8px;border-radius:999px;white-space:nowrap}
    .tags{display:flex;flex-wrap:wrap;gap:8px;margin-top:8px}.chip{font-size:12px;background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.12);padding:4px 8px;border-radius:999px}
    .bullets{margin:10px 0 0 18px;color:var(--muted)} .bullets li{margin:6px 0}
    @media(min-width:720px){.card--half{grid-column:span 6}} @media(min-width:1000px){.card--third{grid-column:span 4}}
    footer{margin-top:36px;color:var(--muted);font-size:14px}
  </style>
</head>
<body class="cats-off">
  <!-- NAVBAR -->
  <nav class="topnav">
    <a href="/" class="brand">Marwa</a>
    <button class="nav-toggle" aria-label="Toggle menu">☰</button>
    <div class="links">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#education">Education</a>
      <a href="#certificates">Certificates</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero" id="intro">
    <div class="rings" aria-hidden="true"><span></span><span></span><span></span><span></span><span></span></div>
    <div class="cats" aria-hidden="true"><span class="paw"></span><span class="paw"></span><span class="paw"></span><span class="paw"></span><span class="paw"></span><span class="paw"></span></div>

    <div class="social" aria-label="social links">
      <a href="https://www.linkedin.com/in/marwaqabeel" target="_blank" rel="noopener" aria-label="LinkedIn">
        <svg viewBox="0 0 24 24"><path d="M4.98 3.5C4.98 4.88 3.86 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1s2.48 1.12 2.48 2.5zM.5 8.5h4V24h-4V8.5zM8 8.5h3.8v2.1h.05c.53-1 1.83-2.1 3.77-2.1 4.03 0 4.78 2.65 4.78 6.1V24h-4v-7.3c0-1.74-.03-3.98-2.43-3.98-2.44 0-2.82 1.9-2.82 3.86V24H8V8.5z"/></svg>
      </a>
      <a href="https://github.com/MarwaQabeel" target="_blank" rel="noopener" aria-label="GitHub">
        <svg viewBox="0 0 24 24"><path d="M12 .5a12 12 0 0 0-3.79 23.4c.6.11.82-.26.82-.58 0-.29-.01-1.06-.02-2.07-3.34.73-4.05-1.61-4.05-1.61-.55-1.38-1.34-1.75-1.34-1.75-1.09-.75.08-.74.08-.74 1.2.09 1.83 1.24 1.83 1.24 1.07 1.83 2.81 1.3 3.5.99.11-.78.42-1.3.76-1.6-2.67-.3-5.48-1.34-5.48-5.95 0-1.31.47-2.38 1.24-3.22-.12-.31-.54-1.56.12-3.25 0 0 1.01-.32 3.3 1.23a11.5 11.5 0 0 1 6 0c2.29-1.55 3.3-1.23 3.3-1.23.66 1.69.24 2.94.12 3.25.77.84 1.24 1.91 1.24 3.22 0 4.62-2.81 5.64-5.49 5.94.43.37.81 1.1.81 2.22 0 1.6-.02 2.88-.02 3.27 0 .32.21.7.83.58A12 12 0 0 0 12 .5z"/></svg>
      </a>
      <a href="mailto:mqabeel3@gatech.edu" aria-label="Email">
        <svg viewBox="0 0 24 24"><path d="M2 4h20a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2zm0 2v.01L12 13 22 6.01V6H2zm0 12h20V8l-10 7L2 8v10z"/></svg>
      </a>
    </div>

    <div class="content">
      <img class="avatar" src="/assets/avatar.jpg" width="116" height="116" alt="Marwa Qabeel portrait" />
      <div class="role">DATA • AI</div>
      <h1>Hi, I'm <span id="type"></span></h1>
      <p class="sub">ML Engineer / Data Scientist. I build end-to-end ML systems, run clear analyses, and ship results.</p>
      <div class="quicklinks">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#experience">Experience</a>
        <a href="#projects" class="primary">View Projects</a>
        <a href="/assets/Marwa_Qabeel_Resume.pdf" class="primary">Resume</a>
      </div>
      <button id="catToggle" class="btn" type="button" aria-pressed="false">🐾 Toggle Paws</button>
    </div>

    <a class="scroll-indicator" href="#main" aria-label="Scroll to content">
      <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 16l-6-6h12z"/></svg>
    </a>
  </section>

  <!-- MAIN CONTENT -->
  <div class="wrap" id="main">

    <!-- About -->
    <section id="about" class="section">
      <h2>About</h2>
      <p>Georgia Tech OMSCS (’26). Udacity Independent Consultant (4.8/5 CSAT across 100+ sessions). I design, train, and evaluate ML pipelines (Python, PyTorch, scikit-learn) and care about production ML, MLOps, and A/B testing.</p>
    </section>

    <!-- Skills (expanded) -->
    <section id="skills" class="section">
      <h2>Skills</h2>
      <div class="grid">
        <article class="card card--third">
          <div class="hd"><div><div class="name">Machine Learning</div><div class="org">Modeling & Evaluation</div></div></div>
          <div class="body">
            <div class="tags">
              <span class="chip">PyTorch</span><span class="chip">TensorFlow</span><span class="chip">scikit-learn</span>
              <span class="chip">BERT</span><span class="chip">GPT-2</span><span class="chip">CNNs/RNNs</span>
              <span class="chip">A/B Testing</span><span class="chip">Stats</span>
            </div>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">NLP & Vision</div><div class="org">Deep Learning</div></div></div>
          <div class="body">
            <div class="tags">
              <span class="chip">Transformers</span><span class="chip">Text Classification</span><span class="chip">Topic Modeling</span>
              <span class="chip">YOLO</span><span class="chip">SSD</span><span class="chip">R-CNN</span>
              <span class="chip">Object Tracking</span><span class="chip">Localization</span>
            </div>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Data & Analytics</div><div class="org">Wrangling & Viz</div></div></div>
          <div class="body">
            <div class="tags">
              <span class="chip">Python</span><span class="chip">NumPy</span><span class="chip">pandas</span>
              <span class="chip">SQL (MySQL, Postgres)</span><span class="chip">Tableau</span><span class="chip">Power BI</span>
              <span class="chip">Matplotlib</span><span class="chip">Advanced Excel</span>
            </div>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Pipelines & MLOps</div><div class="org">Training to Serving</div></div></div>
          <div class="body">
            <div class="tags">
              <span class="chip">Feature Engineering</span><span class="chip">Model Selection</span>
              <span class="chip">Experimentation</span><span class="chip">Flask APIs</span>
              <span class="chip">Docker</span><span class="chip">GitHub</span>
            </div>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Cloud</div><div class="org">Deploy & Analyze</div></div></div>
          <div class="body">
            <div class="tags">
              <span class="chip">AWS</span><span class="chip">Azure</span><span class="chip">Google Cloud</span>
              <span class="chip">BigQuery</span><span class="chip">Amazon Q</span><span class="chip">QuickSight</span>
            </div>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Languages & Tools</div><div class="org">Daily Drivers</div></div></div>
          <div class="body">
            <div class="tags">
              <span class="chip">Python</span><span class="chip">JavaScript</span><span class="chip">R</span>
              <span class="chip">MongoDB</span><span class="chip">VS Code</span><span class="chip">PyCharm</span>
              <span class="chip">Algorithms & DS</span>
            </div>
          </div>
        </article>
      </div>
    </section>

    <!-- Experience -->
    <section id="experience" class="section">
      <h2>Experience</h2>
      <div class="grid">
        <article class="card card--half">
          <div class="hd">
            <div>
              <div class="name">Independent Consultant (Data Science)</div>
              <div class="org">Udacity · Remote · Jan 2019 – Present</div>
            </div>
          </div>
          <div class="body">
            <ul class="bullets">
              <li>Reviewed Data Analyst & Business Analytics projects; average CSAT 4.8/5 across 100+ sessions.</li>
              <li>Led webinars and 1:1 mentoring; built feedback templates that cut review time ~30%.</li>
              <li>Onboarded mentors and authored rubric clarifications to raise pass rates.</li>
            </ul>
          </div>
        </article>

        <article class="card card--half">
          <div class="hd">
            <div>
              <div class="name">Data Science Intern</div>
              <div class="org">Mozilla/Firefox · Remote · Sep 2019 – Mar 2020</div>
            </div>
          </div>
          <div class="body">
            <ul class="bullets">
              <li>Prototyped retention propensity (Python/SQL on BigQuery) with ~5 engineered features.</li>
              <li>Built cohort-retention queries and a light dashboard (BigQuery + Data Studio/Tableau) for PM self-serve.</li>
              <li>Supported experiment readouts and success metrics with DS/PM stakeholders.</li>
            </ul>
          </div>
        </article>
      </div>
    </section>

    <!-- Projects (unchanged core cards) -->
    <section id="projects" class="section">
      <h2>Featured Projects</h2>
      <div class="grid">
        <article class="card card--third">
          <div class="hd"><div><div class="name">Amazon Q in QuickSight – KPI Dashboard</div><div class="org">September 2025</div></div></div>
          <div class="body">
            <div class="tags"><span class="chip">AWS QuickSight</span><span class="chip">Amazon Q</span><span class="chip">KPI</span><span class="chip">Data Visualization</span></div>
            <ul class="bullets"><li>Configured Q, authored topics and Q Bar queries, and built an executive KPI dashboard.</li><li>Refined responses using feedback for concise insights.</li></ul>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Fairness-Aware Educational Data Mining</div><div class="org">Aug 2024 – Jan 2025</div></div></div>
          <div class="body">
            <div class="tags"><span class="chip">Python</span><span class="chip">PyTorch</span><span class="chip">Adversarial ML</span><span class="chip">Fairness Metrics</span></div>
            <ul class="bullets"><li>Raised equity by ~15% with no measured accuracy loss.</li><li>Engineered features and tracked parity/EO metrics.</li></ul>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Detecting Fake News using Deep Neural Networks</div><div class="org">May – Aug 2023</div></div></div>
          <div class="body">
            <div class="tags"><span class="chip">Python</span><span class="chip">TensorFlow</span><span class="chip">PyTorch</span><span class="chip">BERT</span><span class="chip">GPT-2</span></div>
            <ul class="bullets"><li>Benchmarked RNN/LSTM vs. transformers; achieved ~99.5% test accuracy.</li><li>Released code and report.</li></ul>
            <a class="btn" href="https://github.com/MarwaQabeel/Detecting-Fake-News-using-Deep-Neural-Networks" target="_blank" rel="noopener">View Repository</a>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Time-Series Depression Scores on Twitter (BERT)</div><div class="org">Jan – Apr 2023</div></div></div>
          <div class="body">
            <div class="tags"><span class="chip">Python</span><span class="chip">PyTorch</span><span class="chip">BERT</span><span class="chip">Tableau</span></div>
            <ul class="bullets"><li>Modeled regional mental-health trends; analyzed seasonality and geography.</li><li>Built Tableau visuals.</li></ul>
            <a class="btn" href="https://github.com/MarwaQabeel/Time-series-analysis-of-geographic-depression-scores-on-Twitter-using-BERT" target="_blank" rel="noopener">View Repository</a>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd"><div><div class="name">Disease Detection using Chest X-ray (ChestX-ray8)</div><div class="org">Aug 2019</div></div></div>
          <div class="body">
            <div class="tags"><span class="chip">Python</span><span class="chip">PyTorch</span><span class="chip">CNN</span><span class="chip">Localization</span></div>
            <ul class="bullets"><li>Built a CNN-based detector with localization to aid clinical review.</li></ul>
            <a class="btn" href="https://github.com/SGNovice/Disease-detection-using-chest-xrays/" target="_blank" rel="noopener">View Repository</a>
          </div>
        </article>
      </div>
    </section>

    <!-- Education -->
    <section id="education" class="section">
      <h2>Education</h2>
      <div class="grid">
        <article class="card card--half">
          <div class="hd"><div><div class="name">M.S. in Computer Science</div><div class="org">Georgia Institute of Technology · Jan 2021 – Apr 2026 (expected)</div></div></div>
          <div class="body">
            <div class="tags"><span class="chip">Algorithms</span><span class="chip">ML</span><span class="chip">Systems</span></div>
          </div>
        </article>
        <article class="card card--half">
          <div class="hd"><div><div class="name">B.S. in Biology</div><div class="org">South Valley University · Sep 2005 – Jul 2010</div></div></div>
          <div class="body"></div>
        </article>
      </div>
    </section>

    <!-- Certificates (as before) -->
    <section id="certificates" class="section">
      <h2>Certificates & Nanodegrees</h2>
      <div class="grid">
        <article class="card card--half">
          <div class="hd"><div><div class="name">Data Structures and Algorithms Specialization</div><div class="org">UC San Diego</div></div>
            <a class="btn" href="https://coursera.org/share/3d915db4303a0b4b5b54d313df7f2eb4" target="_blank" rel="noopener">Certificate</a>
          </div>
          <div class="body">
            <ul class="list">
              <li><span class="course">Algorithmic Toolbox</span><span class="badge">97.4%</span></li>
              <li><span class="course">Data Structures</span><span class="badge">82.4%</span></li>
              <li><span class="course">Algorithms on Graphs</span><span class="badge">100%</span></li>
              <li><span class="course">Algorithms on Strings</span><span class="badge">85.1%</span></li>
              <li><span class="course">Advanced Algorithms & Complexity</span><span class="badge">92.4%</span></li>
              <li><span class="course">Genome Assembly Challenge</span><span class="badge">84.6%</span></li>
            </ul>
          </div>
        </article>

        <article class="card card--half">
          <div class="hd"><div><div class="name">Discrete Mathematics for CS</div><div class="org">UC San Diego</div></div>
            <a class="btn" href="https://coursera.org/share/576f499c1ff93fa479f077e604ac1e2b" target="_blank" rel="noopener">Certificate</a>
          </div>
          <div class="body">
            <ul class="list">
              <li><span class="course">Mathematical Thinking</span><span class="badge">99.5%</span></li>
              <li><span class="course">Combinatorics & Probability</span><span class="badge">100%</span></li>
              <li><span class="course">Graph Theory</span><span class="badge">98.0%</span></li>
              <li><span class="course">Number Theory & Cryptography</span><span class="badge">99.8%</span></li>
              <li><span class="course">Delivery Problem</span><span class="badge">100%</span></li>
            </ul>
          </div>
        </article>
      </div>

      <div class="section">
        <h2>Udacity Nanodegree Programs</h2>
        <div class="grid">
          <article class="card card--third"><div class="hd"><div><div class="name">Data Structures & Algorithms</div><div class="org">Udacity</div></div></div><div class="body"><a class="btn" href="https://github.com/MarwaQabeel/Data-Structures-and-Algorithms-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a></div></article>
          <article class="card card--third"><div class="hd"><div><div class="name">Deep Learning</div><div class="org">Udacity</div></div></div><div class="body"><a class="btn" href="https://github.com/MarwaQabeel/Udacity-Deep-Learning-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a></div></article>
          <article class="card card--third"><div class="hd"><div><div class="name">Computer Vision</div><div class="org">Udacity</div></div></div><div class="body"><a class="btn" href="https://github.com/MarwaQabeel/Udacity-Computer-Vision-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a></div></article>
          <article class="card card--third"><div class="hd"><div><div class="name">Data Analyst</div><div class="org">Udacity</div></div></div><div class="body"><a class="btn" href="https://github.com/MarwaQabeel/Udacity-Data-Analyst-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a></div></article>
          <article class="card card--third"><div class="hd"><div><div class="name">Data Foundations</div><div class="org">Udacity</div></div></div><div class="body"><a class="btn" href="https://github.com/MarwaQabeel/Udacity-Data-Foundations-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a></div></article>
          <article class="card card--third"><div class="hd"><div><div class="name">Intro to Self-Driving Cars</div><div class="org">Udacity</div></div></div><div class="body"><a class="btn" href="https://confirm.udacity.com/YQSMPUQ2" target="_blank" rel="noopener">View Certificate</a></div></article>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="section">
      <h2>Contact</h2>
      <ul class="list">
        <li><span class="course">Email</span><a href="mailto:mqabeel3@gatech.edu">mqabeel3@gatech.edu</a></li>
        <li><span class="course">Phone</span><a href="tel:+201006535689">+20 100 653 5689</a></li>
        <li><span class="course">LinkedIn</span><a href="https://www.linkedin.com/in/marwaqabeel" target="_blank" rel="noopener">linkedin.com/in/marwaqabeel</a></li>
        <li><span class="course">GitHub</span><a href="https://github.com/MarwaQabeel" target="_blank" rel="noopener">github.com/MarwaQabeel</a></li>
        <li><span class="course">Portfolio</span><a href="https://marwaqabeel.github.io" target="_blank" rel="noopener">marwaqabeel.github.io</a></li>
      </ul>
    </section>

    <footer>Last updated: <span id="updated"></span></footer>
  </div>

  <!-- JS -->
  <script>
    // Typewriter
    (function(){
      const words=["Marwa","a Data Scientist","an AI Mentor","a cat-loving builder"];
      const el=document.getElementById('type'); let i=0,j=0,del=false;
      function tick(){const w=words[i]; el.textContent=w.slice(0,j);
        if(!del && j<w.length){j++;return setTimeout(tick,80)}
        if(j===w.length && !del){del=true;return setTimeout(tick,1000)}
        if(del && j>0){j--;return setTimeout(tick,35)}
        if(j===0){del=false;i=(i+1)%words.length;setTimeout(tick,200)}}
      tick();
    })();

    // Navbar mobile toggle
    const nav=document.querySelector('.topnav'), btn=document.querySelector('.nav-toggle');
    if(btn){btn.onclick=()=>nav.classList.toggle('open');}

    // Active link on scroll
    const ids=['about','skills','experience','projects','education','certificates','contact'];
    const obs=new IntersectionObserver(entries=>{
      entries.forEach(e=>{
        if(e.isIntersecting){
          document.querySelectorAll('.topnav a').forEach(a=>a.classList.remove('active'));
          const hit=document.querySelector(`.topnav a[href="#${e.target.id}"]`);
          if(hit) hit.classList.add('active');
        }
      });
    },{rootMargin:'-45% 0px -50% 0px',threshold:0.01});
    ids.forEach(id=>{const el=document.getElementById(id); if(el) obs.observe(el);});

    // Cat toggle
    const ct=document.getElementById('catToggle');
    if(ct){ct.onclick=()=>{
      document.body.classList.toggle('cats-off');
      ct.setAttribute('aria-pressed', document.body.classList.contains('cats-off') ? 'false' : 'true');
    }}

    // Footer date
    const el=document.getElementById('updated');
    if(el){const d=new Date(),pad=n=>n.toString().padStart(2,'0'); el.textContent=`${d.getFullYear()}-${pad(d.getMonth()+1)}-${pad(d.getDate())}`;}
  </script>
</body>
</html>
