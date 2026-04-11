<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>Abdullah Al Asik — Portfolio</title>
<meta name="description" content="Full-Stack Engineer & Cinematic Designer from Bangladesh. Precision-driven solutions for the modern web."/>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
:root{
  --bg:#05050a;
  --bg2:#0a0a12;
  --bg3:#0f0f1a;
  --border:#1a1a28;
  --gold:#c9a84c;
  --gold2:#e8c97a;
  --gold-dim:#c9a84c30;
  --text:#c8c4b8;
  --white:#f0ead6;
  --muted:#5a5560;
  --mono:'JetBrains Mono',monospace;
  --serif:'Cormorant Garamond',Georgia,serif;
  --sans:'Space Grotesk',sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:var(--sans);background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden}

/* ── CURSOR GLOW ── */
.cursor-glow{pointer-events:none;position:fixed;width:400px;height:400px;border-radius:50%;background:radial-gradient(circle,#c9a84c08 0%,transparent 70%);transform:translate(-50%,-50%);transition:left .08s,top .08s;z-index:0}

/* ── NAV ── */
nav{position:fixed;top:0;left:0;right:0;z-index:100;padding:0 2.5rem;height:60px;display:flex;align-items:center;justify-content:space-between;background:rgba(5,5,10,.8);backdrop-filter:blur(16px);border-bottom:1px solid var(--border)}
.nav-logo{font-family:var(--serif);font-size:1.2rem;font-weight:600;color:var(--gold);letter-spacing:.04em;font-style:italic}
.nav-links{display:flex;gap:2rem}
.nav-links a{font-size:.75rem;color:var(--muted);text-decoration:none;letter-spacing:.12em;text-transform:uppercase;font-weight:500;transition:color .2s}
.nav-links a:hover{color:var(--gold)}
.nav-status{display:flex;align-items:center;gap:6px;font-family:var(--mono);font-size:.65rem;color:var(--muted)}
.nav-dot{width:6px;height:6px;border-radius:50%;background:#4ade80;animation:pulse 2s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.4}}

/* ── HERO ── */
.hero{min-height:100vh;display:flex;flex-direction:column;justify-content:center;padding:7rem 2.5rem 4rem;position:relative;overflow:hidden}
.hero::before{content:'';position:absolute;top:-200px;right:-200px;width:600px;height:600px;border-radius:50%;background:radial-gradient(circle,#c9a84c0a,transparent 70%);pointer-events:none}
.hero::after{content:'';position:absolute;bottom:-200px;left:-100px;width:500px;height:500px;border-radius:50%;background:radial-gradient(circle,#c9a84c06,transparent 70%);pointer-events:none}
.hero-inner{max-width:1000px;margin:0 auto;width:100%;position:relative;z-index:1}
.hero-eyebrow{font-family:var(--mono);font-size:.68rem;color:var(--gold);letter-spacing:.2em;text-transform:uppercase;margin-bottom:1.5rem;display:flex;align-items:center;gap:.8rem}
.hero-eyebrow::before{content:'';width:32px;height:1px;background:var(--gold)}
.hero-layout{display:grid;grid-template-columns:1fr auto;gap:4rem;align-items:center}
.hero-title{font-family:var(--serif);font-size:clamp(3rem,8vw,6rem);font-weight:300;color:var(--white);line-height:1;letter-spacing:-.02em;margin-bottom:.4rem}
.hero-title em{font-style:italic;color:var(--gold)}
.hero-title strong{font-weight:700;display:block}
.hero-subtitle{font-family:var(--mono);font-size:.72rem;color:var(--muted);letter-spacing:.15em;text-transform:uppercase;margin-bottom:1.5rem;border-left:2px solid var(--gold);padding-left:.8rem}
.hero-desc{font-size:1rem;color:var(--text);line-height:1.75;max-width:480px;margin-bottom:2rem;font-weight:300}
.hero-ctas{display:flex;gap:12px;flex-wrap:wrap}
.btn-gold{padding:.65rem 1.6rem;background:var(--gold);color:#05050a;border:none;border-radius:3px;font-weight:700;font-size:.82rem;cursor:pointer;text-decoration:none;display:inline-block;letter-spacing:.05em;transition:background .2s,transform .15s}
.btn-gold:hover{background:var(--gold2);transform:translateY(-2px)}
.btn-ghost{padding:.65rem 1.6rem;background:transparent;color:var(--gold);border:1px solid var(--gold);border-radius:3px;font-weight:500;font-size:.82rem;cursor:pointer;text-decoration:none;display:inline-block;letter-spacing:.05em;transition:all .2s}
.btn-ghost:hover{background:var(--gold-dim);transform:translateY(-2px)}
.hero-avatar-col{display:flex;flex-direction:column;align-items:center;gap:1.2rem}
.avatar-frame{position:relative;width:180px;height:180px}
.avatar-ring{position:absolute;inset:-6px;border-radius:50%;border:1px solid var(--gold);opacity:.4}
.avatar-ring2{position:absolute;inset:-14px;border-radius:50%;border:1px dashed var(--gold);opacity:.15;animation:spin-slow 20s linear infinite}
@keyframes spin-slow{to{transform:rotate(360deg)}}
.avatar-img{width:180px;height:180px;border-radius:50%;object-fit:cover;border:2px solid var(--gold)}
.avatar-ph{width:180px;height:180px;border-radius:50%;background:var(--bg3);border:2px solid var(--gold);display:flex;align-items:center;justify-content:center;font-family:var(--serif);font-size:4rem;font-weight:300;color:var(--gold);font-style:italic}
.hero-stats{display:flex;gap:2rem;margin-top:1rem}
.stat{text-align:center}
.stat-n{font-family:var(--serif);font-size:2rem;font-weight:600;color:var(--white)}
.stat-l{font-family:var(--mono);font-size:.6rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;margin-top:2px}
.hero-flag{font-family:var(--mono);font-size:.68rem;color:var(--muted);letter-spacing:.08em}

/* ── SECTION COMMON ── */
section{padding:6rem 2.5rem;border-top:1px solid var(--border);position:relative}
.sec-inner{max-width:1000px;margin:0 auto}
.sec-kicker{font-family:var(--mono);font-size:.65rem;color:var(--gold);letter-spacing:.2em;text-transform:uppercase;margin-bottom:.6rem;display:flex;align-items:center;gap:.6rem}
.sec-kicker::before{content:'';width:20px;height:1px;background:var(--gold)}
.sec-title{font-family:var(--serif);font-size:clamp(2rem,5vw,3.2rem);font-weight:300;color:var(--white);letter-spacing:-.02em;margin-bottom:3rem}
.sec-title em{font-style:italic;color:var(--gold)}

/* ── ABOUT ── */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:start}
.about-text p{font-size:.95rem;color:var(--text);line-height:1.85;margin-bottom:1.2rem;font-weight:300}
.about-text p strong{color:var(--white);font-weight:600}
.about-highlights{display:flex;flex-direction:column;gap:.8rem}
.highlight-item{display:flex;align-items:flex-start;gap:.8rem;padding:1rem 1.2rem;background:var(--bg2);border:1px solid var(--border);border-left:2px solid var(--gold);border-radius:2px}
.hi-icon{font-size:1.1rem;margin-top:1px}
.hi-label{font-family:var(--mono);font-size:.65rem;color:var(--gold);letter-spacing:.1em;text-transform:uppercase;margin-bottom:2px}
.hi-val{font-size:.88rem;color:var(--text)}

/* ── SKILLS ── */
.skills-layout{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1.5rem}
.skill-block{padding:1.5rem;background:var(--bg2);border:1px solid var(--border);border-radius:4px;transition:border-color .2s}
.skill-block:hover{border-color:var(--gold)}
.skill-block-title{font-family:var(--mono);font-size:.65rem;color:var(--gold);text-transform:uppercase;letter-spacing:.12em;margin-bottom:1rem;padding-bottom:.6rem;border-bottom:1px solid var(--border)}
.skill-pills{display:flex;flex-wrap:wrap;gap:6px}
.pill{font-family:var(--mono);font-size:.7rem;padding:4px 10px;border-radius:2px;background:var(--bg3);border:1px solid var(--border);color:var(--text);transition:all .15s}
.pill:hover,.pill.hot{border-color:var(--gold);color:var(--gold);background:#c9a84c0a}

/* ── PROJECTS ── */
.proj-controls{display:flex;gap:10px;margin-bottom:1.5rem;flex-wrap:wrap;align-items:center}
.proj-search{background:var(--bg2);border:1px solid var(--border);border-radius:3px;padding:.5rem .9rem;color:var(--text);font-family:var(--mono);font-size:.75rem;outline:none;width:220px}
.proj-search:focus{border-color:var(--gold)}
.proj-search::placeholder{color:var(--muted)}
.lang-btn{font-family:var(--mono);font-size:.65rem;padding:5px 12px;border-radius:2px;border:1px solid var(--border);color:var(--muted);cursor:pointer;background:transparent;transition:all .15s}
.lang-btn:hover{border-color:var(--gold);color:var(--gold)}
.lang-btn.on{background:var(--gold);border-color:var(--gold);color:#05050a;font-weight:700}
.sort-bar{display:flex;align-items:center;gap:8px;margin-bottom:1.5rem}
.sort-lbl{font-family:var(--mono);font-size:.62rem;color:var(--muted)}
.sort-btn{font-family:var(--mono);font-size:.65rem;color:var(--muted);background:none;border:none;cursor:pointer;padding:3px 8px;border-radius:2px}
.sort-btn.on{color:var(--gold);background:#c9a84c12}
.rcount{margin-left:auto;font-family:var(--mono);font-size:.62rem;color:var(--muted)}
.repo-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1px;background:var(--border);border-radius:4px;overflow:hidden}
.repo-card{background:var(--bg2);padding:1.5rem;display:flex;flex-direction:column;gap:10px;text-decoration:none;transition:background .15s}
.repo-card:hover{background:var(--bg3)}
.rc-name{font-size:.9rem;font-weight:600;color:var(--gold2)}
.rc-desc{font-family:var(--mono);font-size:.72rem;color:var(--muted);line-height:1.65;flex:1}
.rc-topics{display:flex;flex-wrap:wrap;gap:5px}
.rc-topic{font-family:var(--mono);font-size:.6rem;padding:2px 7px;border-radius:2px;background:#c9a84c0a;color:var(--gold);border:1px solid #c9a84c20}
.rc-meta{display:flex;align-items:center;gap:10px}
.rc-lang{font-family:var(--mono);font-size:.67rem;color:var(--muted);display:flex;align-items:center;gap:4px}
.ldot{width:7px;height:7px;border-radius:50%;flex-shrink:0}
.rc-stars,.rc-date{font-family:var(--mono);font-size:.67rem;color:var(--muted)}
.rc-date{margin-left:auto;color:var(--border)}
.repo-loading,.repo-empty{text-align:center;padding:3rem;grid-column:1/-1;font-family:var(--mono);font-size:.78rem;color:var(--muted)}
.spin{width:24px;height:24px;border:1px solid var(--border);border-top-color:var(--gold);border-radius:50%;animation:spin .7s linear infinite;margin:0 auto 1rem}
@keyframes spin{to{transform:rotate(360deg)}}

/* ── FEATURED PROJ ── */
.featured{display:grid;grid-template-columns:1fr 1fr;gap:2rem;margin-bottom:2rem}
.feat-card{background:var(--bg2);border:1px solid var(--gold);border-radius:4px;padding:2rem;position:relative;overflow:hidden}
.feat-card::before{content:'FEATURED';position:absolute;top:1rem;right:1rem;font-family:var(--mono);font-size:.55rem;color:var(--gold);letter-spacing:.15em;opacity:.6}
.feat-badge{font-family:var(--mono);font-size:.6rem;color:var(--gold);letter-spacing:.12em;text-transform:uppercase;margin-bottom:.8rem;opacity:.7}
.feat-name{font-family:var(--serif);font-size:1.6rem;font-weight:600;color:var(--white);margin-bottom:.5rem}
.feat-desc{font-size:.85rem;color:var(--text);line-height:1.7;margin-bottom:1.2rem;font-weight:300}
.feat-tech{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:1.5rem}
.feat-pill{font-family:var(--mono);font-size:.65rem;padding:3px 9px;border-radius:2px;background:#c9a84c10;color:var(--gold);border:1px solid #c9a84c25}
.feat-links{display:flex;gap:10px}
.feat-link{font-family:var(--mono);font-size:.72rem;color:var(--gold);text-decoration:none;padding:6px 14px;border:1px solid var(--gold);border-radius:2px;transition:all .2s}
.feat-link:hover{background:var(--gold);color:#05050a}
.feat-link.demo{background:var(--gold);color:#05050a}
.feat-link.demo:hover{background:var(--gold2)}

/* ── CONTACT ── */
.contact-layout{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:start}
.contact-intro{font-size:.95rem;color:var(--text);line-height:1.85;font-weight:300;margin-bottom:2rem}
.contact-intro strong{color:var(--white)}
.contact-cards{display:flex;flex-direction:column;gap:10px}
.contact-card{display:flex;align-items:center;gap:1rem;padding:1rem 1.2rem;background:var(--bg2);border:1px solid var(--border);border-radius:3px;text-decoration:none;color:var(--text);transition:all .2s}
.contact-card:hover{border-color:var(--gold);background:var(--bg3);transform:translateX(4px)}
.cc-icon{width:36px;height:36px;border-radius:3px;background:var(--bg3);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;flex-shrink:0}
.cc-icon svg{width:16px;height:16px}
.cc-label{font-family:var(--mono);font-size:.6rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em}
.cc-val{font-size:.85rem;color:var(--white);font-weight:500;margin-top:1px}
.contact-note{padding:1.5rem;background:var(--bg2);border:1px solid var(--border);border-left:2px solid var(--gold);border-radius:2px;font-family:var(--mono);font-size:.75rem;color:var(--text);line-height:1.7;margin-top:1.5rem}
.contact-note span{color:var(--gold)}

/* ── FOOTER ── */
footer{border-top:1px solid var(--border);padding:2.5rem;text-align:center;font-family:var(--mono);font-size:.65rem;color:var(--muted)}
footer a{color:var(--gold);text-decoration:none}
.footer-flag{font-size:1rem}

/* ── RESPONSIVE ── */
@media(max-width:700px){
  .hero-layout,.about-grid,.contact-layout,.featured{grid-template-columns:1fr}
  .hero-avatar-col{order:-1}
  .nav-status,.nav-links a:not(:first-child){display:none}
  .nav-links{gap:1rem}
}
</style>
</head>
<body>

<div class="cursor-glow" id="glow"></div>

<!-- NAV -->
<nav>
  <span class="nav-logo">Abdullah Al Asik</span>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </div>
  <div class="nav-status">
    <div class="nav-dot"></div>
    System.Status(Active)
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-inner">
    <div class="hero-eyebrow">Precision-Driven Solutions for the Modern Web</div>
    <div class="hero-layout">
      <div>
        <h1 class="hero-title">
          <em>Abdullah</em>
          <strong>Al Asik</strong>
        </h1>
        <div class="hero-subtitle">Statistical Analysis · Full-Stack Engineering · Cinematic Design</div>
        <p class="hero-desc">
          Building high-performance web experiences and AI-powered tools from Bangladesh.
          Focused on elegant code, visual precision, and free technology for everyone.
        </p>
        <div class="hero-ctas">
          <a href="#projects" class="btn-gold">View Projects</a>
          <a href="https://abdullahalasikshadow.github.io/asik.ai/" target="_blank" class="btn-ghost">Live Demo ↗</a>
          <a href="#contact" class="btn-ghost">Contact</a>
        </div>
      </div>
      <div class="hero-avatar-col">
        <div class="avatar-frame">
          <div class="avatar-ring"></div>
          <div class="avatar-ring2"></div>
          <img
            class="avatar-img"
            src="https://avatars.githubusercontent.com/u/274320672?v=4"
            alt="Abdullah Al Asik"
            onerror="this.style.display='none';document.getElementById('avPh').style.display='flex'"
          />
          <div class="avatar-ph" id="avPh" style="display:none">A</div>
        </div>
        <div class="hero-stats" id="heroStats">
          <div class="stat"><div class="stat-n" id="sRepos">4</div><div class="stat-l">Repos</div></div>
          <div class="stat"><div class="stat-n" id="sFollowers">—</div><div class="stat-l">Followers</div></div>
          <div class="stat"><div class="stat-n" id="sFollowing">—</div><div class="stat-l">Following</div></div>
        </div>
        <div class="hero-flag">🇧🇩 Dhaka, Bangladesh</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="sec-inner">
    <div class="sec-kicker">01 — About</div>
    <h2 class="sec-title">Who I <em>Am</em></h2>
    <div class="about-grid">
      <div class="about-text">
        <p>
          I'm <strong>Abdullah Al Asik</strong>, a developer and designer from Bangladesh with a passion for building things that are both technically sharp and visually striking.
        </p>
        <p>
          My work sits at the intersection of <strong>full-stack engineering</strong>, <strong>AI integration</strong>, and <strong>cinematic design</strong> — I care deeply about every pixel and every line of code.
        </p>
        <p>
          Currently focused on building <strong>free, accessible AI tools</strong> for students and developers worldwide — because powerful technology shouldn't have a price tag.
        </p>
        <p>
          I believe the best software is fast, private, and built for real people. That's the philosophy behind everything I ship.
        </p>
      </div>
      <div class="about-highlights">
        <div class="highlight-item">
          <div class="hi-icon">⚡</div>
          <div><div class="hi-label">Focus</div><div class="hi-val">High-performance web & AI tools</div></div>
        </div>
        <div class="highlight-item">
          <div class="hi-icon">🧠</div>
          <div><div class="hi-label">Philosophy</div><div class="hi-val">Free tech for everyone, no barriers</div></div>
        </div>
        <div class="highlight-item">
          <div class="hi-icon">🎬</div>
          <div><div class="hi-label">Style</div><div class="hi-val">Cinematic precision in every design</div></div>
        </div>
        <div class="highlight-item">
          <div class="hi-icon">📍</div>
          <div><div class="hi-label">Location</div><div class="hi-val">Dhaka, Bangladesh 🇧🇩</div></div>
        </div>
        <div class="highlight-item">
          <div class="hi-icon">🚀</div>
          <div><div class="hi-label">Joined GitHub</div><div class="hi-val">April 2026</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="sec-inner">
    <div class="sec-kicker">02 — Skills</div>
    <h2 class="sec-title">Tech <em>Stack</em></h2>
    <div class="skills-layout">
      <div class="skill-block">
        <div class="skill-block-title">// Languages</div>
        <div class="skill-pills">
          <span class="pill hot">HTML5</span>
          <span class="pill hot">CSS3</span>
          <span class="pill hot">JavaScript</span>
          <span class="pill">TypeScript</span>
          <span class="pill">Python</span>
          <span class="pill">Markdown</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-title">// Frontend</div>
        <div class="skill-pills">
          <span class="pill hot">Tailwind CSS</span>
          <span class="pill hot">Vanilla JS</span>
          <span class="pill">React</span>
          <span class="pill">Responsive Design</span>
          <span class="pill">Animations</span>
          <span class="pill">Figma</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-title">// AI & APIs</div>
        <div class="skill-pills">
          <span class="pill hot">Groq API</span>
          <span class="pill hot">Google Gemini</span>
          <span class="pill">AI Integration</span>
          <span class="pill">REST APIs</span>
          <span class="pill">Prompt Engineering</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-title">// DevOps & Tools</div>
        <div class="skill-pills">
          <span class="pill hot">GitHub Pages</span>
          <span class="pill hot">Git</span>
          <span class="pill">GitHub Actions</span>
          <span class="pill">VS Code</span>
          <span class="pill">Mac Mini M4</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="sec-inner">
    <div class="sec-kicker">03 — Projects</div>
    <h2 class="sec-title">My <em>Work</em></h2>

    <!-- Featured -->
    <div class="featured">
      <div class="feat-card">
        <div class="feat-badge">// Flagship Project</div>
        <div class="feat-name">ASIK AI</div>
        <div class="feat-desc">
          A free personal AI assistant for students and developers. Powered by Groq and Google Gemini. 14,400 requests/day, zero cost, zero signup. Study, code, math, writing — anything.
        </div>
        <div class="feat-tech">
          <span class="feat-pill">HTML</span>
          <span class="feat-pill">Tailwind CSS</span>
          <span class="feat-pill">Vanilla JS</span>
          <span class="feat-pill">Groq API</span>
          <span class="feat-pill">Gemini API</span>
          <span class="feat-pill">GitHub Pages</span>
        </div>
        <div class="feat-links">
          <a href="https://abdullahalasikshadow.github.io/asik.ai/" target="_blank" class="feat-link demo">Live Demo ↗</a>
          <a href="https://github.com/abdullahalasikshadow/asik.ai" target="_blank" class="feat-link">Source Code</a>
        </div>
      </div>
      <div class="feat-card" style="border-color:var(--border)">
        <div class="feat-badge">// Utility Tools</div>
        <div class="feat-name">Routine Apps</div>
        <div class="feat-desc">
          A pair of productivity apps — <strong>routine</strong> and <strong>simpleroutine</strong> — designed to help organize daily schedules with a clean, minimal interface.
        </div>
        <div class="feat-tech">
          <span class="feat-pill">HTML</span>
          <span class="feat-pill">CSS</span>
          <span class="feat-pill">JavaScript</span>
          <span class="feat-pill">GitHub Pages</span>
        </div>
        <div class="feat-links">
          <a href="https://github.com/abdullahalasikshadow/routine" target="_blank" class="feat-link">routine ↗</a>
          <a href="https://github.com/abdullahalasikshadow/simpleroutine" target="_blank" class="feat-link">simpleroutine ↗</a>
        </div>
      </div>
    </div>

    <!-- All repos -->
    <div class="sec-kicker" style="margin-bottom:1rem">// All Repositories</div>
    <div class="proj-controls" id="langFilters">
      <button class="lang-btn on" data-l="all" onclick="setLang('all')">all</button>
    </div>
    <div class="sort-bar">
      <span class="sort-lbl">sort:</span>
      <button class="sort-btn on" id="s-updated" onclick="setSort('updated')">recent</button>
      <button class="sort-btn" id="s-stars" onclick="setSort('stars')">stars</button>
      <button class="sort-btn" id="s-name" onclick="setSort('name')">name</button>
      <input class="proj-search" id="repoSearch" placeholder="search..." oninput="renderRepos()"/>
      <span class="rcount" id="rcount"></span>
    </div>
    <div class="repo-grid" id="repoGrid">
      <div class="repo-loading"><div class="spin"></div>Loading repositories...</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="sec-inner">
    <div class="sec-kicker">04 — Contact</div>
    <h2 class="sec-title">Let's <em>Connect</em></h2>
    <div class="contact-layout">
      <div>
        <p class="contact-intro">
          I'm always open to <strong>collaborations, feedback, and conversations</strong> about tech, AI, or design.<br/><br/>
          Whether you want to build something together or just say hi — reach out. I read every message.
        </p>
        <div class="contact-note">
          <span>// Made in 🇧🇩 Bangladesh</span><br/>
          Free AI for everyone. No barriers. Just pure knowledge.<br/>
          <span>— Abdullah Al Asik</span>
        </div>
      </div>
      <div class="contact-cards">
        <a class="contact-card" href="https://github.com/abdullahalasikshadow" target="_blank">
          <div class="cc-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
          </div>
          <div><div class="cc-label">GitHub</div><div class="cc-val">@abdullahalasikshadow</div></div>
        </a>
        <a class="contact-card" href="https://abdullahalasikshadow.github.io/asik.ai/" target="_blank">
          <div class="cc-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
          </div>
          <div><div class="cc-label">Live Project</div><div class="cc-val">asik.ai — Free AI Assistant</div></div>
        </a>
        <a class="contact-card" href="https://github.com/abdullahalasikshadow/asik.ai/issues" target="_blank">
          <div class="cc-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>
          </div>
          <div><div class="cc-label">Feedback & Issues</div><div class="cc-val">Open a GitHub Issue</div></div>
        </a>
        <a class="contact-card" href="mailto:your@email.com" id="emailCard">
          <div class="cc-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="#c9a84c" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          </div>
          <div><div class="cc-label">Email</div><div class="cc-val">your@email.com</div></div>
        </a>
      </div>
    </div>
  </div>
</section>

<footer>
  <div style="margin-bottom:.5rem">
    <span class="footer-flag">🇧🇩</span>
    Built &amp; designed by <a href="https://github.com/abdullahalasikshadow">Abdullah Al Asik</a> · Hosted on <a href="https://pages.github.com">GitHub Pages</a>
  </div>
  <div style="opacity:.4">Free technology for everyone · No barriers · Just pure knowledge</div>
</footer>

<script>
// Cursor glow
const glow=document.getElementById('glow');
document.addEventListener('mousemove',e=>{glow.style.left=e.clientX+'px';glow.style.top=e.clientY+'px'});

// GitHub API
const LC={JavaScript:'#f1e05a',TypeScript:'#3178c6',Python:'#3572A5',Java:'#b07219','C++':'#f34b7d',C:'#555',CSS:'#563d7c',HTML:'#e34c26',Shell:'#89e051',Vue:'#41b883',Dart:'#00B4AB'};
let allRepos=[],activeLang='all',activeSort='updated';

function setSort(s){
  activeSort=s;
  ['updated','stars','name'].forEach(x=>document.getElementById('s-'+x).classList.toggle('on',x===s));
  renderRepos();
}
function setLang(l){
  activeLang=l;
  document.querySelectorAll('.lang-btn').forEach(b=>b.classList.toggle('on',b.dataset.l===l));
  renderRepos();
}
function renderRepos(){
  const q=(document.getElementById('repoSearch').value||'').toLowerCase();
  let repos=allRepos.filter(r=>(activeLang==='all'||r.language===activeLang)&&(!q||r.name.toLowerCase().includes(q)||(r.description||'').toLowerCase().includes(q)));
  if(activeSort==='stars') repos.sort((a,b)=>b.stargazers_count-a.stargazers_count);
  else if(activeSort==='name') repos.sort((a,b)=>a.name.localeCompare(b.name));
  else repos.sort((a,b)=>new Date(b.updated_at)-new Date(a.updated_at));
  document.getElementById('rcount').textContent=repos.length+' repos';
  const grid=document.getElementById('repoGrid');
  if(!repos.length){grid.innerHTML='<div class="repo-empty">no repos found</div>';return;}
  grid.innerHTML=repos.map(r=>{
    const dot=r.language?`<span class="ldot" style="background:${LC[r.language]||'#5a5560'}"></span><span>${r.language}</span>`:'';
    const topics=(r.topics||[]).slice(0,3).map(t=>`<span class="rc-topic">${t}</span>`).join('');
    const upd=new Date(r.updated_at).toLocaleDateString('en-US',{month:'short',year:'numeric'});
    return`<a class="repo-card" href="${r.html_url}" target="_blank">
      <div class="rc-name">${r.name}</div>
      <div class="rc-desc">${r.description||'— no description'}</div>
      ${topics?`<div class="rc-topics">${topics}</div>`:''}
      <div class="rc-meta">
        ${r.language?`<span class="rc-lang">${dot}</span>`:''}
        <span class="rc-stars">★ ${r.stargazers_count}</span>
        <span class="rc-date">${upd}</span>
      </div>
    </a>`;
  }).join('');
}

async function init(){
  try{
    const[uRes,rRes]=await Promise.all([
      fetch('https://api.github.com/users/abdullahalasikshadow'),
      fetch('https://api.github.com/users/abdullahalasikshadow/repos?per_page=100&sort=updated')
    ]);
    if(uRes.ok){
      const u=await uRes.json();
      document.getElementById('sRepos').textContent=u.public_repos;
      document.getElementById('sFollowers').textContent=u.followers;
      document.getElementById('sFollowing').textContent=u.following;
    }
    if(rRes.ok){
      const repos=await rRes.json();
      allRepos=repos.filter(r=>!r.fork);
      const langs=[...new Set(allRepos.map(r=>r.language).filter(Boolean))].slice(0,8);
      const lf=document.getElementById('langFilters');
      lf.innerHTML=['all',...langs].map(l=>`<button class="lang-btn ${l==='all'?'on':''}" data-l="${l}" onclick="setLang('${l}')">${l}</button>`).join('');
      renderRepos();
    }
  }catch(e){
    document.getElementById('repoGrid').innerHTML='<div class="repo-empty">could not load repos — check connection</div>';
  }
}
init();
</script>
</body>
</html>
