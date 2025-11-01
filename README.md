<!-- <!DOCTYPE html> -->
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
  <!-- Headings = Plus Jakarta Sans, Body = Inter -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Plus+Jakarta+Sans:wght@600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      /* Refined palette */
      --bg:#0a0f1f;
      --panel:#10172b;
      --panel-2:#0e1426;
      --text:#eef2ff;
      --muted:#aab4d6;
      --accent:#e88cff;   /* pink-violet */
      --accent-2:#7aa2ff; /* blue */
      --ring:rgba(232,140,255,.35);
      --ok:#47d17e;
      --shadow:0 10px 24px rgba(5,15,40,.55),0 4px 10px rgba(0,0,0,.25);
    }

    html,body{margin:0} html{scroll-behavior:smooth}
    body{
      font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif;
      background:radial-gradient(1200px 900px at 20% -10%,rgba(122,162,255,.10),transparent 55%),
                 linear-gradient(180deg,#0a0f1f 0%,#0b1224 55%,#0a0f20 100%);
      color:var(--text); -webkit-font-smoothing:antialiased
    }
    h1,h2,.brand{font-family:"Plus Jakarta Sans",Inter,system-ui,sans-serif; letter-spacing:.3px}

    a{color:var(--accent-2);text-decoration:none}
    a:hover{text-decoration:underline}

    /* Top nav */
    .topnav{position:sticky;top:0;z-index:50;backdrop-filter:saturate(140%) blur(10px);
      background:rgba(10,15,31,.58);border-bottom:1px solid rgba(255,255,255,.08);
      display:flex;align-items:center;justify-content:space-between;padding:10px 16px}
    .brand{font-weight:800;color:var(--text)}
    .brand .grad{
      background:linear-gradient(90deg,var(--accent) 0%, var(--accent-2) 60%, #8ee2ff 100%);
      -webkit-background-clip:text; background-clip:text; -webkit-text-fill-color:transparent
    }
    .links{display:flex;gap:16px}
    .topnav a{color:var(--text)}
    .topnav a.active{border-bottom:2px solid var(--accent)}
    .nav-toggle{display:none;background:none;border:0;color:var(--text);font-size:20px}
    @media(max-width:760px){
      .links{display:none}
      .topnav.open .links{display:flex;flex-direction:column;position:absolute;right:12px;top:48px;
        background:rgba(9,14,30,.95);padding:10px 12px;border-radius:12px;border:1px solid rgba(255,255,255,.08)}
      .nav-toggle{display:block}
    }

    /* Hero */
    .hero{min-height:100vh;display:flex;align-items:center;position:relative;overflow:hidden}
    .hero .rings{position:absolute;inset:-10% -10% auto -10%;pointer-events:none;opacity:.7}
    .hero .rings span{position:absolute;border:1px solid rgba(255,255,255,.12);border-radius:50%;
      left:50%;top:50%;transform:translate(-50%,-50%)}
    .hero .rings span:nth-child(1){width:420px;height:420px}
    .hero .rings span:nth-child(2){width:660px;height:660px;border-color:rgba(255,255,255,.10)}
    .hero .rings span:nth-child(3){width:900px;height:900px;border-color:rgba(255,255,255,.07)}
    .hero .rings span:nth-child(4){width:1200px;height:1200px;border-color:rgba(255,255,255,.05)}
    .hero .rings span:nth-child(5){width:1600px;height:1600px;border-color:rgba(255,255,255,.04)}

    /* Left-aligned hero layout on desktop */
    .hero .content{position:relative;z-index:1;max-width:1100px;margin:0 auto;padding:24px 20px;text-align:center}
    @media(min-width:960px){
      .hero .content{display:grid;grid-template-columns:140px 1fr;gap:24px;align-items:center;text-align:left}
    }

    .avatar{width:116px;height:116px;border-radius:999px;object-fit:cover;border:2px solid rgba(255,255,255,.35);
      box-shadow:0 10px 24px rgba(0,0,0,.35);margin:0 auto 16px}
    @media(min-width:960px){.avatar{margin:0}}

    .role{letter-spacing:.45em;text-transform:uppercase;color:var(--muted);font-size:12px;margin:6px 0 10px}
    h1.hero-title{font-size:56px;line-height:1.05;margin:6px 0 10px}
    @media(min-width:900px){h1.hero-title{font-size:72px}}
    /* Gradient title for subtle pop */
    .hero-title .grad{
      background:linear-gradient(90deg,var(--accent) 0%, var(--accent-2) 65%, #8ee2ff 100%);
      -webkit-background-clip:text; background-clip:text; -webkit-text-fill-color:transparent
    }

    .sub{color:var(--muted);max-width:720px;margin:0 auto 18px}
    @media(min-width:960px){.sub{margin:0 0 18px}}

    .quicklinks{display:flex;justify-content:center;gap:12px;flex-wrap:wrap;margin-top:14px}
    @media(min-width:960px){.quicklinks{justify-content:flex-start}}
    .btn{display:inline-flex;align-items:center;gap:8px;font-weight:600;
      background:linear-gradient(180deg,rgba(232,140,255,.22),rgba(232,140,255,.10));
      border:1px solid rgba(232,140,255,.55);padding:10px 14px;border-radius:12px;color:var(--text)}
    .quicklinks a{display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:999px;
      border:1px solid rgba(255,255,255,.16);background:rgba(255,255,255,.05)}
    .quicklinks a.primary{border-color:rgba(122,162,255,.55);
      background:linear-gradient(180deg,rgba(122,162,255,.22),rgba(122,162,255,.12))}

    .social{position:absolute;left:24px;top:24px;display:flex;gap:14px}
    .social svg{width:22px;height:22px;fill:currentColor;color:var(--muted)}
    .scroll-indicator{position:absolute;bottom:22px;left:50%;transform:translateX(-50%);width:36px;height:36px;border-radius:999px;border:1px solid rgba(255,255,255,.2);display:grid;place-items:center}
    .scroll-indicator svg{width:18px;height:18px;color:var(--muted)}

    /* Cat paws (keep as before) */
    .cats{position:absolute;inset:0;pointer-events:none;opacity:.25}
    .cats .paw{position:absolute;width:32px;height:32px;background-repeat:no-repeat;background-size:contain;animation:drift 26s linear infinite;
      background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64' fill='%23aab4d6'><circle cx='18' cy='18' r='7'/><circle cx='32' cy='12' r='6'/><circle cx='46' cy='18' r='7'/><path d='M16 40c4-9 28-9 32 0-3 8-11 14-16 14s-13-6-16-14z'/></svg>")}
    @keyframes drift{0%{transform:translateY(40vh) rotate(0)}100%{transform:translateY(-70vh) rotate(18deg)}}
    .cats .paw:nth-child(1){left:8%;animation-duration:28s}
    .cats .paw:nth-child(2){left:26%;animation-duration:32s;animation-delay:4s}
    .cats .paw:nth-child(3){left:44%;animation-duration:29s;animation-delay:8s}
    .cats .paw:nth-child(4){left:62%;animation-duration:31s;animation-delay:2s}
    .cats .paw:nth-child(5){left:78%;animation-duration:27s;animation-delay:6s}
    .cats .paw:nth-child(6){left:90%;animation-duration:34s;animation-delay:10s}
    .cats-off .cats{display:none}
    @media (prefers-reduced-motion:reduce){.cats{display:none}}

    /* Main layout + cards (unchanged) */
    .wrap{max-width:1100px;margin:0 auto;padding:28px 20px 64px}
    .section{margin-top:28px}.section h2{font-size:22px;margin:0 0 14px}
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
    <a href="/" class="brand"><span class="grad">Marwa Fawzy Qabeel</span></a>
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

      <!-- Left-aligned full name -->
      <h1 class="hero-title">Hi, I'm <span class="grad">Marwa Fawzy Qabeel</span></h1>

      <p class="sub">
        ML Engineer / Data Scientist. <span id="type"></span>
      </p>

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

  <!-- ===== Keep your existing MAIN content below unchanged ===== -->
  <!-- (About, Skills, Experience, Projects, Education, Certificates, Contact, Footer, JS) -->
  <!-- ... your existing sections ... -->

  <script>
    // Typewriter for the short descriptor under your name
    (function(){
      const words=["I build end-to-end ML systems","I run clear analyses","I ship results"];
      const el=document.getElementById('type'); let i=0,j=0,del=false;
      function tick(){
        const w=words[i]; el.textContent=w.slice(0,j);
        if(!del && j<w.length){j++;return setTimeout(tick,65)}
        if(j===w.length && !del){del=true;return setTimeout(tick,950)}
        if(del && j>0){j--;return setTimeout(tick,28)}
        if(j===0){del=false;i=(i+1)%words.length;setTimeout(tick,140)}
      } tick();
    })();

    // Navbar mobile toggle
    const nav=document.querySelector('.topnav'), btn=document.querySelector('.nav-toggle');
    if(btn){btn.onclick=()=>nav.classList.toggle('open');}

    // Active link on scroll (same as before if you already had it)
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
  </script>
</body>
</html>
