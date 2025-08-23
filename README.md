  <style>
    :root{
      --bg:#0b0b12;
      --panel:#0f1020;
      --ink:#e6e7ee;
      --muted:#9aa0b3;
      --brand-1:#7c3aed; /* violet */
      --brand-2:#00b3ff; /* cyan */
      --accent:#ff2ea1;  /* neon pink */
      --ring: 0 0 0 2px rgba(124,58,237,.25), 0 0 30px rgba(0,179,255,.15);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, "Helvetica Neue", Arial, "Apple Color Emoji", "Segoe UI Emoji";
      background: radial-gradient(1200px 600px at 80% -10%, rgba(124,58,237,.12), transparent 60%),
                  radial-gradient(1000px 500px at -10% 10%, rgba(0,179,255,.12), transparent 60%),
                  var(--bg);
      color:var(--ink);
      line-height:1.6;
      letter-spacing:.2px;
    }
    .wrap{max-width:1000px;margin:0 auto;padding:48px 24px 72px}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px;margin-bottom:36px}
    .brand{display:flex;align-items:center;gap:12px;text-decoration:none;color:inherit}
    .logo{
      width:40px;height:40px;border-radius:12px;position:relative;isolation:isolate;
      background: linear-gradient(135deg, var(--brand-1), var(--accent));
      box-shadow: 0 10px 30px rgba(124,58,237,.25), 0 6px 18px rgba(255,46,161,.18);
    }
    .logo::after{content:"";position:absolute;inset:-2px;border-radius:14px;filter:blur(10px);background:linear-gradient(135deg, rgba(124,58,237,.6), rgba(0,179,255,.45), rgba(255,46,161,.5));opacity:.7;z-index:-1}
    .brand h1{font-size:1.125rem;margin:0;font-weight:700;letter-spacing:.4px}
    .sub{color:var(--muted);font-size:.9rem}
    .hero{
      padding:48px;border-radius:24px;position:relative;overflow:hidden;background:linear-gradient(180deg, rgba(15,16,32,.65), rgba(15,16,32,.4));
      border:1px solid rgba(255,255,255,.06);box-shadow: 0 10px 30px rgba(0,0,0,.4), inset 0 0 0 1px rgba(255,255,255,.04);
      backdrop-filter: blur(6px);
    }
    .hero::before{
      content:"";position:absolute;inset:-40%;background: conic-gradient(from 180deg at 50% 50%, rgba(124,58,237,.15), rgba(0,179,255,.12), rgba(255,46,161,.15), rgba(124,58,237,.15));
      filter: blur(48px);opacity:.7;pointer-events:none;
    }
    .eyebrow{display:inline-flex;align-items:center;gap:8px;padding:6px 10px;border-radius:999px;font-size:.8rem;color:#d9d9e6;background:rgba(124,58,237,.12);border:1px solid rgba(124,58,237,.25)}
    .title{font-size:clamp(2rem, 4vw + .5rem, 3.25rem);line-height:1.1;margin:16px 0 12px;font-weight:800;letter-spacing:.3px}
    .title .grad{
      background: linear-gradient(90deg, var(--brand-1), var(--brand-2), var(--accent));
      -webkit-background-clip:text;background-clip:text;color:transparent
    }
    .lead{font-size:1.05rem;color:#d1d5e1;max-width:70ch}
    .stats{display:grid;grid-template-columns: repeat(4, 1fr);gap:14px;margin-top:28px}
    .stat{
      background:linear-gradient(180deg, rgba(17,19,37,.8), rgba(17,19,37,.6));
      border:1px solid rgba(255,255,255,.06);border-radius:16px;padding:18px 16px;position:relative;overflow:hidden
    }
    .stat::after{content:"";position:absolute;inset:auto -20% -20% -20%;height:2px;background:linear-gradient(90deg, transparent, rgba(124,58,237,.6), rgba(0,179,255,.6), rgba(255,46,161,.6), transparent);filter:blur(6px)}
    .stat .num{font-size:1.6rem;font-weight:800;letter-spacing:.4px}
    .stat .label{color:var(--muted);font-size:.9rem}
    .panel{margin-top:28px;padding:22px 20px;border-radius:18px;background:linear-gradient(180deg, rgba(15,16,32,.55), rgba(15,16,32,.4));border:1px solid rgba(255,255,255,.06)}
    .panel p{margin:0;color:#d1d5e1}
    footer{margin-top:36px;color:var(--muted);font-size:.9rem;display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap}
    @media (max-width: 900px){ .stats{grid-template-columns: repeat(2, 1fr)} }
    @media (max-width: 520px){ .hero{padding:32px} .stats{grid-template-columns: 1fr} header{flex-direction:column;align-items:flex-start} }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <a class="brand" href="#" aria-label="Anon Developers Lab">
        <div class="logo" aria-hidden="true"></div>
        <div>
          <h1>Anon Developers Lab</h1>
          <div class="sub">Futuristic Research &amp; Development Collective</div>
        </div>
      </a>
      <div class="sub">Est. • Privacy × Security × Innovation</div>
    </header>

    <section class="hero" aria-labelledby="title">
      <span class="eyebrow" aria-label="Tagline">Stealth • Ethics • Impact</span>
      <h2 id="title" class="title">Shaping the future of <span class="grad">privacy, security &amp; digital freedom</span>.</h2>
      <p class="lead">
        Anon Lab is a <strong>futuristic R&amp;D collective</strong> exploring emerging technologies to design systems that
        <strong>empower communities</strong> while rigorously protecting <strong>user sovereignty</strong>.
      </p>

      <div class="stats" aria-label="Impact metrics">
        <div class="stat"><div class="num">120+</div><div class="label">Innovations &amp; Experiments</div></div>
        <div class="stat"><div class="num">15+</div><div class="label">Countries Reached</div></div>
        <div class="stat"><div class="num">50+</div><div class="label">Active Collaborators</div></div>
        <div class="stat"><div class="num">🏆</div><div class="label">Recognized in Research Circles</div></div>
      </div>
    </section>

    <section class="panel" aria-label="About Anon Lab">
      <p><strong>Mission:</strong> Build quietly, ship boldly. We prototype responsibly, audit transparently, and deliver
        tools that uphold privacy by design.</p>
    </section>

    <footer>
      <span>✨ Innovating in silence. Impacting at scale. 🖤</span>
      <span>© 2025 Anon Developers Lab</span>
    </footer>
  </div>
</body>
</html>
