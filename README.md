<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Certificates & Nanodegrees · Marwa Qabeel</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b1220;
      --panel: #101a31;
      --panel-2: #0e162b;
      --text: #eaf0ff;
      --muted: #b6c1e2;
      --accent: #7aa2ff;
      --accent-2: #8ee2ff;
      --ring: rgba(122,162,255,.35);
      --ok: #47d17e;
      --shadow: 0 10px 24px rgba(5, 15, 40, .55), 0 4px 10px rgba(0,0,0,.25);
    }
    html,body{margin:0}
    body{font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif;background:linear-gradient(180deg,#0a1020 0%,#0c1425 60%,#0a0f20 100%);color:var(--text);-webkit-font-smoothing:antialiased}
    a{color:var(--accent);text-decoration:none}
    a:hover{text-decoration:underline}
    .wrap{max-width:1100px;margin:0 auto;padding:28px 20px 64px}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px;margin:8px 0 24px}
    .title{display:flex;flex-direction:column;gap:6px}
    .title h1{font-size:28px;line-height:1.15;margin:0}
    .title p{margin:0;color:var(--muted)}
    .note{background:linear-gradient(180deg,rgba(122,162,255,.12),rgba(122,162,255,.06));border:1px solid rgba(122,162,255,.25);padding:12px 14px;border-radius:12px;color:var(--muted)}

    .section{margin-top:28px}
    .section h2{font-size:20px;margin:0 0 14px}

    .grid{display:grid;grid-template-columns:repeat(12,1fr);gap:14px}

    .card{grid-column:span 12;background:linear-gradient(180deg,var(--panel),var(--panel-2));border:1px solid rgba(255,255,255,.06);border-radius:18px;box-shadow:var(--shadow);position:relative;overflow:hidden}
    .card:hover{transform:translateY(-2px);transition:transform .2s ease}

    .card .hd{display:flex;justify-content:space-between;gap:8px;padding:16px 18px;border-bottom:1px solid rgba(255,255,255,.06)}
    .card .hd .name{font-weight:700}
    .card .hd .org{color:var(--muted)}

    .card .body{padding:14px 18px}

    .pill{display:inline-flex;align-items:center;gap:8px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.08);padding:8px 10px;border-radius:12px}
    .pill .dot{width:8px;height:8px;border-radius:50%;background:var(--ok)}

    .list{display:grid;gap:8px;margin:12px 0 2px;padding:0;list-style:none}
    .list li{display:flex;justify-content:space-between;align-items:center;gap:12px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);border-radius:12px;padding:10px 12px}
    .course{font-weight:600}

    .badge{font-size:12px;font-weight:700;color:#06230f;background:linear-gradient(180deg,#6cf3a2,#38d878);border:1px solid rgba(0,0,0,.15);padding:4px 8px;border-radius:999px;white-space:nowrap}

    .btn{display:inline-flex;align-items:center;gap:8px;font-weight:600;background:linear-gradient(180deg,rgba(122,162,255,.22),rgba(122,162,255,.12));border:1px solid rgba(122,162,255,.45);padding:10px 12px;border-radius:12px}
    .btn svg{width:16px;height:16px}

    .subgrid{display:grid;grid-template-columns:repeat(12,1fr);gap:10px}
    .mini{grid-column:span 12;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);border-radius:14px;padding:12px}

    /* layout */
    @media(min-width:720px){
      .card--half{grid-column:span 6}
      .mini{grid-column:span 6}
    }
    @media(min-width:1000px){
      .card--third{grid-column:span 4}
      .mini{grid-column:span 4}
    }

    /* subtle focus */
    .focusable:focus{outline:2px solid var(--ring);outline-offset:3px;border-radius:12px}

    /* dark-mode friendly link underlines */
    .linkish{border-bottom:1px dotted rgba(255,255,255,.35)}

    footer{margin-top:36px;color:var(--muted);font-size:14px}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="title">
        <h1>Certificates & Nanodegrees</h1>
        <p>Selected credentials with grades and verification links.</p>
      </div>
    </header>

    <!-- Coursera Specializations -->
    <section class="section">
      <h2>Coursera Specializations</h2>
      <div class="grid">
        <!-- 1. DSA Specialization -->
        <article class="card card--half">
          <div class="hd">
            <div>
              <div class="name">Data Structures and Algorithms Specialization</div>
              <div class="org">University of California, San Diego</div>
            </div>
            <a class="btn focusable" href="https://coursera.org/share/3d915db4303a0b4b5b54d313df7f2eb4" target="_blank" rel="noopener" aria-label="View specialization certificate">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M14 3h7v7h-2V6.41l-9.29 9.3-1.42-1.42 9.3-9.29H14V3z"/></svg>
              Certificate
            </a>
          </div>
          <div class="body">
            <ul class="list">
              <li><span class="course">Algorithmic Toolbox</span><span class="badge">97.4%</span></li>
              <li><span class="course">Data Structures</span><span class="badge">82.4%</span></li>
              <li><span class="course">Algorithms on Graphs</span><span class="badge">100%</span></li>
              <li><span class="course">Algorithms on Strings</span><span class="badge">85.1%</span></li>
              <li><span class="course">Advanced Algorithms and Complexity</span><span class="badge">92.4%</span></li>
              <li><span class="course">Genome Assembly Programming Challenge</span><span class="badge">84.6%</span></li>
            </ul>
            <div class="subgrid">
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/BNGXGH4SB4ZN" target="_blank" rel="noopener">Algorithmic Toolbox – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/Z2VVAQ5WPJZQ" target="_blank" rel="noopener">Data Structures – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/K7QBHEPHCM7P" target="_blank" rel="noopener">Algorithms on Graphs – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/E9N694PZNM2E" target="_blank" rel="noopener">Algorithms on Strings – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/3KK8LEYMFD2Q" target="_blank" rel="noopener">Advanced Algorithms & Complexity – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/WGYQMSL2SULZ" target="_blank" rel="noopener">Genome Assembly Challenge – verify</a></div>
            </div>
          </div>
        </article>

        <!-- 2. Discrete Math Specialization -->
        <article class="card card--half">
          <div class="hd">
            <div>
              <div class="name">Introduction to Discrete Mathematics for Computer Science</div>
              <div class="org">University of California, San Diego</div>
            </div>
            <a class="btn focusable" href="https://coursera.org/share/576f499c1ff93fa479f077e604ac1e2b" target="_blank" rel="noopener" aria-label="View specialization certificate">
              <svg viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M14 3h7v7h-2V6.41l-9.29 9.3-1.42-1.42 9.3-9.29H14V3z"/></svg>
              Certificate
            </a>
          </div>
          <div class="body">
            <ul class="list">
              <li><span class="course">Mathematical Thinking in CS</span><span class="badge">99.5%</span></li>
              <li><span class="course">Combinatorics and Probability</span><span class="badge">100%</span></li>
              <li><span class="course">Introduction to Graph Theory</span><span class="badge">98.0%</span></li>
              <li><span class="course">Number Theory and Cryptography</span><span class="badge">99.8%</span></li>
              <li><span class="course">Delivery Problem</span><span class="badge">100%</span></li>
            </ul>
            <div class="subgrid">
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/9CK4CKKK7533" target="_blank" rel="noopener">Mathematical Thinking – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/YHA2N6DFUN9R" target="_blank" rel="noopener">Combinatorics & Probability – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/KLWJEDV2V4DT" target="_blank" rel="noopener">Graph Theory – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/7BQJXHPLJ9F2" target="_blank" rel="noopener">Number Theory & Cryptography – verify</a></div>
              <div class="mini"><a class="linkish" href="https://www.coursera.org/account/accomplishments/certificate/C4UEM9BETDDV" target="_blank" rel="noopener">Delivery Problem – verify</a></div>
            </div>
          </div>
        </article>
      </div>
    </section>

    <!-- Udacity Nanodegrees -->
    <section class="section">
      <h2>Udacity Nanodegree Programs</h2>
      <div class="grid">
        <article class="card card--third">
          <div class="hd">
            <div>
              <div class="name">Data Structures & Algorithms</div>
              <div class="org">Udacity</div>
            </div>
          </div>
          <div class="body">
            <a class="btn focusable" href="https://github.com/MarwaQabeel/Data-Structures-and-Algorithms-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd">
            <div>
              <div class="name">Deep Learning</div>
              <div class="org">Udacity</div>
            </div>
          </div>
          <div class="body">
            <a class="btn focusable" href="https://github.com/MarwaQabeel/Udacity-Deep-Learning-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd">
            <div>
              <div class="name">Computer Vision</div>
              <div class="org">Udacity</div>
            </div>
          </div>
          <div class="body">
            <a class="btn focusable" href="https://github.com/MarwaQabeel/Udacity-Computer-Vision-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd">
            <div>
              <div class="name">Data Analyst</div>
              <div class="org">Udacity</div>
            </div>
          </div>
          <div class="body">
            <a class="btn focusable" href="https://github.com/MarwaQabeel/Udacity-Data-Analyst-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd">
            <div>
              <div class="name">Data Foundations</div>
              <div class="org">Udacity</div>
            </div>
          </div>
          <div class="body">
            <a class="btn focusable" href="https://github.com/MarwaQabeel/Udacity-Data-Foundations-Nanodegree" target="_blank" rel="noopener">Projects & Certificate</a>
          </div>
        </article>

        <article class="card card--third">
          <div class="hd">
            <div>
              <div class="name">Intro to Self‑Driving Cars</div>
              <div class="org">Udacity</div>
            </div>
          </div>
          <div class="body">
            <a class="btn focusable" href="https://confirm.udacity.com/YQSMPUQ2" target="_blank" rel="noopener">View Certificate</a>
          </div>
        </article>
      </div>
    </section>

    <footer>
      Last updated: <span id="updated"></span>
    </footer>
  </div>

  <script>
    const el=document.getElementById('updated');
    if(el){
      const d=new Date();
      const pad=n=>n.toString().padStart(2,'0');
      el.textContent = `${d.getFullYear()}-${pad(d.getMonth()+1)}-${pad(d.getDate())}`;
    }
  </script>
</body>
</html>
