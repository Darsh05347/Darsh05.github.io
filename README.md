
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Darshan Vijay Gohil — Naval Architecture & Ocean Engineering</title>
<meta name="description" content="Portfolio of Darshan Vijay Gohil — M.Sc. candidate in Naval Architecture & Ocean Engineering. Ship performance simulation, marine structures (FEM/CFD), and clean hydrogen propulsion.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;600;700;800;900&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --abyss:#071a24;
    --deep:#0b2531;
    --deep-2:#103040;
    --chart:#eef3f4;
    --mist:#e1eaec;
    --line:#b9ccd2;
    --wake:#34cabf;
    --wake-deep:#159b92;
    --steel:#5f7a87;
    --ink:#0c1f29;
    --foam:#ffffff;
    --maxw:1160px;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  @media (prefers-reduced-motion:reduce){html{scroll-behavior:auto}}
  body{
    font-family:"Inter",system-ui,sans-serif;
    background:var(--chart);
    color:var(--ink);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  a{color:inherit;text-decoration:none}
  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 28px}
  .mono{font-family:"JetBrains Mono",ui-monospace,monospace}
  .eyebrow{
    font-family:"JetBrains Mono",monospace;
    font-size:.72rem;letter-spacing:.28em;text-transform:uppercase;
    color:var(--wake-deep);font-weight:500;
  }

  /* ---------- NAV ---------- */
  nav{
    position:fixed;top:0;left:0;right:0;z-index:50;
    display:flex;align-items:center;justify-content:space-between;
    padding:16px 28px;
    background:rgba(7,26,36,0);
    transition:background .4s ease, padding .4s ease, box-shadow .4s ease;
  }
  nav.docked{background:rgba(7,26,36,.92);backdrop-filter:blur(8px);padding:11px 28px;box-shadow:0 1px 0 rgba(255,255,255,.06)}
  .brand{display:flex;align-items:center;gap:11px;color:var(--foam)}
  .brand .mark{
    width:30px;height:30px;border:1.5px solid var(--wake);border-radius:50%;
    display:grid;place-items:center;font-family:"Archivo";font-weight:800;font-size:.78rem;
    color:var(--wake);letter-spacing:-.02em;
  }
  .brand b{font-family:"Archivo";font-weight:700;font-size:.95rem;letter-spacing:.01em}
  .navlinks{display:flex;gap:26px}
  .navlinks a{
    font-family:"JetBrains Mono",monospace;font-size:.74rem;letter-spacing:.12em;
    text-transform:uppercase;color:#a9c2cb;transition:color .2s;
  }
  .navlinks a:hover{color:var(--wake)}
  .nav-cta{
    font-family:"JetBrains Mono",monospace;font-size:.74rem;letter-spacing:.1em;text-transform:uppercase;
    color:var(--abyss);background:var(--wake);padding:8px 15px;border-radius:2px;font-weight:500;
    transition:transform .2s, background .2s;
  }
  .nav-cta:hover{background:var(--foam);transform:translateY(-1px)}
  .menu-btn{display:none;background:none;border:0;color:var(--foam);cursor:pointer}
  @media(max-width:820px){
    .navlinks,.nav-cta{display:none}
    .menu-btn{display:block}
  }

  /* ---------- HERO ---------- */
  header{
    position:relative;background:var(--abyss);color:var(--foam);
    min-height:100vh;display:flex;align-items:center;
    padding:120px 0 70px;overflow:hidden;
  }
  .hero-grid{
    position:absolute;inset:0;
    background-image:linear-gradient(rgba(255,255,255,.035) 1px,transparent 1px);
    background-size:100% 64px;
    -webkit-mask-image:linear-gradient(to bottom,transparent,#000 30%,#000 70%,transparent);
            mask-image:linear-gradient(to bottom,transparent,#000 30%,#000 70%,transparent);
    pointer-events:none;
  }
  #wake{position:absolute;top:50%;right:-8%;transform:translateY(-50%);width:min(70vw,760px);height:auto;opacity:.9;pointer-events:none}
  @media(max-width:820px){#wake{right:-30%;top:62%;width:120vw;opacity:.5}.wktext{display:none}}
  .hero-inner{position:relative;z-index:2;max-width:var(--maxw);margin:0 auto;padding:0 28px;width:100%}
  .hero-inner .eyebrow{display:block;margin-bottom:22px}
  h1{
    font-family:"Archivo";font-weight:900;letter-spacing:-.03em;line-height:.95;
    font-size:clamp(2.7rem,8vw,6rem);color:var(--foam);
  }
  h1 .ln2{color:var(--wake)}
  .role{
    margin-top:26px;max-width:34ch;font-size:clamp(1.05rem,1.7vw,1.32rem);
    color:#c4d6dd;font-weight:400;
  }
  .role b{color:var(--foam);font-weight:600}
  .hero-meta{display:flex;flex-wrap:wrap;gap:12px;margin-top:34px}
  .chip{
    display:inline-flex;align-items:center;gap:8px;
    font-family:"JetBrains Mono",monospace;font-size:.78rem;letter-spacing:.04em;
    padding:9px 14px;border:1px solid rgba(255,255,255,.16);border-radius:2px;
    color:#d2e2e7;transition:border-color .25s,color .25s,background .25s;
  }
  .chip:hover{border-color:var(--wake);color:var(--foam);background:rgba(52,202,191,.08)}
  .chip svg{width:14px;height:14px;flex:none;stroke:var(--wake)}
  .scrollcue{
    position:absolute;bottom:26px;left:50%;transform:translateX(-50%);z-index:2;
    font-family:"JetBrains Mono",monospace;font-size:.66rem;letter-spacing:.3em;text-transform:uppercase;
    color:#6f9099;display:flex;flex-direction:column;align-items:center;gap:9px;
  }
  .scrollcue .bar{width:1px;height:34px;background:linear-gradient(var(--wake),transparent);animation:drop 2.2s ease-in-out infinite}
  @keyframes drop{0%,100%{opacity:.3;transform:scaleY(.6)}50%{opacity:1;transform:scaleY(1)}}

  /* ---------- SECTION SHELL ---------- */
  section{padding:96px 0;position:relative}
  .sec-head{display:flex;align-items:baseline;gap:18px;margin-bottom:46px;border-bottom:1px solid var(--line);padding-bottom:18px}
  .sec-no{font-family:"JetBrains Mono",monospace;font-size:.8rem;color:var(--wake-deep);font-weight:500}
  .sec-head h2{font-family:"Archivo";font-weight:800;font-size:clamp(1.5rem,3.4vw,2.3rem);letter-spacing:-.02em;color:var(--ink)}
  .sec-head .station{margin-left:auto;font-family:"JetBrains Mono",monospace;font-size:.72rem;letter-spacing:.18em;color:var(--steel);text-transform:uppercase}

  /* ---------- ABOUT ---------- */
  .about{display:grid;grid-template-columns:1.55fr .9fr;gap:54px}
  @media(max-width:820px){.about{grid-template-columns:1fr;gap:34px}}
  .about p{font-size:1.08rem;color:#2b4350;margin-bottom:18px}
  .about p strong{color:var(--ink);font-weight:600}
  .specsheet{border:1px solid var(--line);background:var(--foam);border-radius:3px;align-self:start}
  .specsheet .sptop{background:var(--deep);color:#cfe0e5;font-family:"JetBrains Mono",monospace;font-size:.7rem;letter-spacing:.2em;text-transform:uppercase;padding:11px 18px}
  .spec{display:flex;justify-content:space-between;gap:16px;padding:13px 18px;border-bottom:1px solid var(--mist);font-size:.92rem}
  .spec:last-child{border-bottom:0}
  .spec .k{font-family:"JetBrains Mono",monospace;font-size:.74rem;letter-spacing:.06em;color:var(--steel);text-transform:uppercase;padding-top:2px}
  .spec .v{text-align:right;color:var(--ink);font-weight:500}
  .avail{color:var(--wake-deep)!important}

  /* ---------- SKILLS ---------- */
  .skills{background:var(--mist)}
  .skillgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:24px}
  @media(max-width:820px){.skillgrid{grid-template-columns:1fr}}
  .skillcard{background:var(--foam);border:1px solid var(--line);border-radius:3px;padding:26px 24px;position:relative;overflow:hidden}
  .skillcard::before{content:"";position:absolute;top:0;left:0;width:34px;height:2px;background:var(--wake)}
  .skillcard h3{font-family:"Archivo";font-weight:700;font-size:1.06rem;margin-bottom:4px}
  .skillcard .sk-no{font-family:"JetBrains Mono",monospace;font-size:.72rem;color:var(--wake-deep);letter-spacing:.1em}
  .tags{display:flex;flex-wrap:wrap;gap:8px;margin-top:18px}
  .tag{font-family:"JetBrains Mono",monospace;font-size:.74rem;letter-spacing:.02em;padding:6px 11px;background:var(--chart);border:1px solid var(--mist);border-radius:2px;color:#33505d}
  .softlist{margin-top:18px;list-style:none}
  .softlist li{position:relative;padding-left:18px;font-size:.92rem;color:#33505d;margin-bottom:9px}
  .softlist li::before{content:"";position:absolute;left:0;top:9px;width:7px;height:7px;border:1.5px solid var(--wake-deep);border-radius:50%}

  /* ---------- PROJECTS ---------- */
  .proj{border-top:1px solid var(--line)}
  .proj:last-of-type{border-bottom:1px solid var(--line)}
  .projrow{display:grid;grid-template-columns:64px 1fr;gap:0;padding:34px 0;transition:background .3s}
  .projrow:hover{background:var(--foam)}
  .pno{font-family:"JetBrains Mono",monospace;font-size:.82rem;color:var(--wake-deep);padding-top:6px}
  .ptitle{font-family:"Archivo";font-weight:700;font-size:clamp(1.18rem,2.3vw,1.55rem);letter-spacing:-.01em;color:var(--ink);line-height:1.18}
  .pmeta{display:flex;flex-wrap:wrap;gap:7px;margin:13px 0 6px}
  .pmeta span{font-family:"JetBrains Mono",monospace;font-size:.7rem;letter-spacing:.05em;text-transform:uppercase;color:var(--wake-deep);border:1px solid var(--line);padding:4px 9px;border-radius:2px}
  .pbody{list-style:none;margin-top:12px;max-width:74ch}
  .pbody li{position:relative;padding-left:20px;color:#2f4854;margin-bottom:9px;font-size:.99rem}
  .pbody li::before{content:"";position:absolute;left:0;top:11px;width:9px;height:1px;background:var(--wake-deep)}
  .pstat{display:inline-block;margin-top:6px;font-family:"Archivo";font-weight:800;color:var(--wake-deep);font-size:.95rem}
  .pstat b{font-size:1.35rem}
  @media(max-width:560px){.projrow{grid-template-columns:1fr;gap:6px}.pno{padding-top:0}}

  /* ---------- TIMELINE (exp + edu) ---------- */
  .two{display:grid;grid-template-columns:1fr 1fr;gap:54px}
  @media(max-width:820px){.two{grid-template-columns:1fr;gap:46px}}
  .subhead{font-family:"JetBrains Mono",monospace;font-size:.74rem;letter-spacing:.2em;text-transform:uppercase;color:var(--steel);margin-bottom:24px}
  .tl{position:relative;padding-left:26px}
  .tl::before{content:"";position:absolute;left:4px;top:6px;bottom:6px;width:1px;background:var(--line)}
  .tlitem{position:relative;margin-bottom:30px}
  .tlitem:last-child{margin-bottom:0}
  .tlitem::before{content:"";position:absolute;left:-26px;top:5px;width:9px;height:9px;border-radius:50%;background:var(--chart);border:2px solid var(--wake)}
  .tlitem h4{font-family:"Archivo";font-weight:700;font-size:1.08rem;color:var(--ink)}
  .tlitem .org{color:var(--wake-deep);font-weight:500;font-size:.95rem;margin:2px 0 4px}
  .tlitem .when{font-family:"JetBrains Mono",monospace;font-size:.72rem;letter-spacing:.06em;color:var(--steel);text-transform:uppercase}
  .tlitem ul{list-style:none;margin-top:10px}
  .tlitem ul li{position:relative;padding-left:16px;font-size:.92rem;color:#33505d;margin-bottom:7px}
  .tlitem ul li::before{content:"";position:absolute;left:0;top:9px;width:6px;height:1px;background:var(--wake-deep)}

  /* ---------- CERTIFICATES ---------- */
  .certs{background:var(--deep);color:var(--foam)}
  .certs .sec-head{border-color:rgba(255,255,255,.14)}
  .certs .sec-head h2{color:var(--foam)}
  .certs .sec-head .station{color:#7ea0aa}
  .certgrid{display:grid;grid-template-columns:repeat(2,1fr);gap:20px}
  @media(max-width:680px){.certgrid{grid-template-columns:1fr}}
  .cert{
    display:flex;flex-direction:column;
    background:rgba(255,255,255,.035);border:1px solid rgba(255,255,255,.12);border-radius:3px;
    padding:24px 22px;transition:border-color .3s,transform .3s,background .3s;
  }
  .cert:hover{border-color:var(--wake);transform:translateY(-3px);background:rgba(52,202,191,.06)}
  .cert .ctop{display:flex;justify-content:space-between;align-items:center;margin-bottom:14px}
  .cert .prov{font-family:"JetBrains Mono",monospace;font-size:.7rem;letter-spacing:.16em;text-transform:uppercase;color:var(--wake)}
  .cert .hrs{font-family:"JetBrains Mono",monospace;font-size:.7rem;color:#7ea0aa}
  .cert h3{font-family:"Archivo";font-weight:700;font-size:1.12rem;line-height:1.22;color:var(--foam);margin-bottom:8px}
  .cert .inst{font-size:.88rem;color:#9fbac2;margin-bottom:18px}
  .cert .cfoot{margin-top:auto;display:flex;justify-content:space-between;align-items:center;border-top:1px solid rgba(255,255,255,.1);padding-top:13px}
  .cert .cfoot .date{font-family:"JetBrains Mono",monospace;font-size:.72rem;color:#7ea0aa}
  .cert .verify{font-family:"JetBrains Mono",monospace;font-size:.72rem;letter-spacing:.08em;text-transform:uppercase;color:var(--wake);display:inline-flex;align-items:center;gap:6px;transition:gap .2s}
  .cert .verify:hover{gap:10px}
  .cert .verify svg{width:12px;height:12px;stroke:var(--wake)}

  /* ---------- CONTACT ---------- */
  .contact{background:var(--abyss);color:var(--foam);text-align:center;padding:110px 0 64px;position:relative;overflow:hidden}
  .contact .hero-grid{ -webkit-mask-image:linear-gradient(to bottom,#000,transparent);mask-image:linear-gradient(to bottom,#000,transparent)}
  .contact .eyebrow{display:block;margin-bottom:20px}
  .contact h2{font-family:"Archivo";font-weight:900;font-size:clamp(2rem,5.5vw,3.6rem);letter-spacing:-.03em;line-height:1.02;max-width:16ch;margin:0 auto 16px}
  .contact h2 em{font-style:normal;color:var(--wake)}
  .contact p{color:#9fbac2;max-width:48ch;margin:0 auto 38px}
  .contact-actions{display:flex;flex-wrap:wrap;gap:14px;justify-content:center;position:relative;z-index:2}
  .btn{font-family:"JetBrains Mono",monospace;font-size:.8rem;letter-spacing:.08em;text-transform:uppercase;padding:14px 22px;border-radius:2px;display:inline-flex;align-items:center;gap:9px;transition:transform .2s,background .2s,border-color .2s}
  .btn svg{width:15px;height:15px}
  .btn-primary{background:var(--wake);color:var(--abyss);font-weight:500}
  .btn-primary svg{stroke:var(--abyss)}
  .btn-primary:hover{background:var(--foam);transform:translateY(-2px)}
  .btn-ghost{border:1px solid rgba(255,255,255,.22);color:var(--foam)}
  .btn-ghost svg{stroke:var(--wake)}
  .btn-ghost:hover{border-color:var(--wake);transform:translateY(-2px)}
  footer{position:relative;z-index:2;margin-top:70px;padding-top:26px;border-top:1px solid rgba(255,255,255,.1);display:flex;flex-wrap:wrap;justify-content:space-between;gap:12px;font-family:"JetBrains Mono",monospace;font-size:.72rem;letter-spacing:.06em;color:#6f9099}
  footer a:hover{color:var(--wake)}

  /* ---------- REVEAL ---------- */
  .reveal{opacity:0;transform:translateY(26px);transition:opacity .7s ease,transform .7s ease}
  .reveal.in{opacity:1;transform:none}
  @media (prefers-reduced-motion:reduce){
    .reveal{opacity:1;transform:none;transition:none}
    .scrollcue .bar{animation:none}
    .wkanim{animation:none!important}
  }
</style>
</head>
<body>

<nav id="nav">
  <a class="brand" href="#top">
    <span class="mark">DG</span>
    <b>Darshan&nbsp;Gohil</b>
  </a>
  <div class="navlinks">
    <a href="#about">About</a>
    <a href="#skills">Capabilities</a>
    <a href="#projects">Projects</a>
    <a href="#record">Record</a>
    <a href="#certs">Certificates</a>
  </div>
  <a class="nav-cta" href="#contact">Get in touch</a>
  <button class="menu-btn" aria-label="Jump to contact" onclick="location.href='#contact'">
    <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="4" y1="7" x2="20" y2="7"/><line x1="4" y1="12" x2="20" y2="12"/><line x1="4" y1="17" x2="20" y2="17"/></svg>
  </button>
</nav>

<header id="top">
  <div class="hero-grid"></div>
  <!-- Signature: a Kelvin wake — the V-pattern that trails every moving hull (half-angle ~19°28') -->
  <svg id="wake" viewBox="0 0 760 620" fill="none" aria-hidden="true">
    <defs>
      <linearGradient id="wg" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0" stop-color="#34cabf" stop-opacity=".9"/>
        <stop offset="1" stop-color="#159b92" stop-opacity=".15"/>
      </linearGradient>
    </defs>
    <g class="wkanim" stroke="url(#wg)" stroke-width="1.2">
      <!-- transverse waves: arcs expanding behind the ship at the cusp (right side) -->
      <path d="M690,310 q-90,-150 -250,-200" stroke-opacity=".55"/>
      <path d="M690,310 q-90,150 -250,200" stroke-opacity=".55"/>
      <g stroke-width="1">
        <path d="M640,310 a150,150 0 0 0 -150,-150" stroke-opacity=".4"/>
        <path d="M640,310 a150,150 0 0 1 -150,150" stroke-opacity=".4"/>
        <path d="M560,310 a120,120 0 0 0 -120,-120" stroke-opacity=".32"/>
        <path d="M560,310 a120,120 0 0 1 -120,120" stroke-opacity=".32"/>
        <path d="M488,310 a92,92 0 0 0 -92,-92" stroke-opacity=".26"/>
        <path d="M488,310 a92,92 0 0 1 -92,92" stroke-opacity=".26"/>
        <path d="M426,310 a66,66 0 0 0 -66,-66" stroke-opacity=".2"/>
        <path d="M426,310 a66,66 0 0 1 -66,66" stroke-opacity=".2"/>
      </g>
      <!-- divergent feathering lines -->
      <g stroke-width=".8" stroke-opacity=".3">
        <path d="M690,310 L300,150"/><path d="M620,260 L320,150"/><path d="M560,225 L340,158"/>
        <path d="M690,310 L300,470"/><path d="M620,360 L320,470"/><path d="M560,395 L340,462"/>
      </g>
    </g>
    <!-- the hull marker at the cusp -->
    <circle class="wkanim" cx="700" cy="310" r="5" fill="#34cabf"/>
    <circle cx="700" cy="310" r="11" fill="none" stroke="#34cabf" stroke-opacity=".5"/>
    <text class="wktext" x="312" y="146" fill="#5f8b94" font-family="JetBrains Mono, monospace" font-size="13" letter-spacing="1">19°28′ KELVIN ANGLE</text>
  </svg>

  <div class="hero-inner">
    <span class="eyebrow reveal">Naval Architecture · Ocean Engineering</span>
    <h1 class="reveal">Darshan<br>Vijay <span class="ln2">Gohil</span></h1>
    <p class="role reveal">M.Sc. candidate applying <b>simulation, FEM and CAD</b> to solve complex engineering problems — across mechanical, structural and marine systems.</p>
    <div class="hero-meta reveal">
      <a class="chip" href="#record"><svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M12 2 4 6v6c0 5 8 8 8 8s8-3 8-8V6z"/></svg>M.Sc. · Hochschule Bremen</a>
      <span class="chip"><svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M21 10c0 7-9 12-9 12s-9-5-9-12a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>Bremen, Germany</span>
      <span class="chip"><svg viewBox="0 0 24 24" fill="none" stroke-width="2"><circle cx="12" cy="12" r="9"/><path d="M3 12h18M12 3a14 14 0 0 1 0 18M12 3a14 14 0 0 0 0 18"/></svg>EN C1 · DE A2</span>
    </div>
  </div>
  <div class="scrollcue"><span>Scroll</span><span class="bar"></span></div>
</header>

<!-- ABOUT -->
<section id="about" class="wrap">
  <div class="sec-head reveal"><span class="sec-no">01</span><h2>Profile</h2><span class="station">Station 01</span></div>
  <div class="about">
    <div class="reveal">
      <p>I'm a Master's student in <strong>Naval Architecture and Ocean Engineering</strong> at Hochschule Bremen, building on a Bachelor's in Mechanical Engineering. My work centres on <strong>hydrogen technologies and maritime energy systems</strong> — and on the structures that have to survive the sea state around them.</p>
      <p>Through coursework and projects I've gained hands-on experience in <strong>structural analysis, material behaviour, and design under marine loading</strong>, including FEM-based stress and pressure analysis with ANSYS and STAR-CCM+. I'm especially drawn to fatigue, fracture mechanics, and the <strong>structural integrity of pressure-bearing components</strong> — the parts that fail quietly if you get the numbers wrong.</p>
      <p>Alongside the simulation side, I work in CAD, literature review, and data evaluation, with working knowledge of Python and MATLAB. I'm structured, dependable, and happy to relocate or commute to take on impactful work. Available to start immediately.</p>
    </div>
    <aside class="specsheet reveal">
      <div class="sptop">Spec Sheet</div>
      <div class="spec"><span class="k">Discipline</span><span class="v">Naval Arch. &amp; Ocean Eng.</span></div>
      <div class="spec"><span class="k">Degree</span><span class="v">M.Sc. (in progress)</span></div>
      <div class="spec"><span class="k">Base</span><span class="v">Bremen, DE</span></div>
      <div class="spec"><span class="k">Languages</span><span class="v">English C1 · German A2</span></div>
      <div class="spec"><span class="k">Status</span><span class="v avail">Available immediately</span></div>
    </aside>
  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="skills">
  <div class="wrap">
    <div class="sec-head reveal"><span class="sec-no">02</span><h2>Capabilities</h2><span class="station">Station 02</span></div>
    <div class="skillgrid">
      <div class="skillcard reveal">
        <span class="sk-no">A —</span>
        <h3>Numerical Methods</h3>
        <div class="tags">
          <span class="tag">CFD · STAR-CCM+</span><span class="tag">FEM / FEA · ANSYS</span><span class="tag">ANSYS Workbench</span>
          <span class="tag">Stress &amp; pressure analysis</span><span class="tag">Fatigue &amp; fracture</span><span class="tag">Ship resistance</span><span class="tag">Motion / sea-state</span>
        </div>
      </div>
      <div class="skillcard reveal">
        <span class="sk-no">B —</span>
        <h3>Software &amp; CAD</h3>
        <div class="tags">
          <span class="tag">Python</span><span class="tag">MATLAB</span><span class="tag">CAESES</span>
          <span class="tag">AutoCAD</span><span class="tag">Rhino · Grasshopper</span><span class="tag">Autodesk Inventor</span><span class="tag">Office 365</span>
        </div>
      </div>
      <div class="skillcard reveal">
        <span class="sk-no">C —</span>
        <h3>Working Strengths</h3>
        <ul class="softlist">
          <li>Structured, dependable problem-solving</li>
          <li>Cross-functional communication &amp; coordination</li>
          <li>Strong documentation &amp; requirement handling</li>
          <li>Literature review &amp; data evaluation</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="wrap">
  <div class="sec-head reveal"><span class="sec-no">03</span><h2>Selected Projects</h2><span class="station">Station 03</span></div>
  <div class="proj">

    <div class="projrow reveal">
      <div class="pno">P-01</div>
      <div>
        <div class="ptitle">Numerical Simulation of Hydrodynamic Resistance — Post-Panamax Container Ship</div>
        <div class="pmeta"><span>CFD</span><span>Ship performance</span><span>STAR-CCM+</span></div>
        <ul class="pbody">
          <li>Ran CFD simulations to analyse ship resistance and visualise Kelvin wake patterns, supporting early-stage prototype validation and performance screening under varying hydrodynamic conditions.</li>
          <li>Evaluated vessel trim and heel behaviour across speeds to confirm stability and reliability, feeding design-to-production workflows and cross-functional engineering reviews.</li>
        </ul>
      </div>
    </div>

    <div class="projrow reveal">
      <div class="pno">P-02</div>
      <div>
        <div class="ptitle">Motion Prediction for the Keppel Fels Platform</div>
        <div class="pmeta"><span>Motion sim</span><span>Sea state</span><span>Statistical analysis</span></div>
        <ul class="pbody">
          <li>Scaled the platform in CAD and imported it into STAR-CCM+ for motion simulations, analysing dynamic behaviour for design validation.</li>
          <li>Applied statistical analysis to quantify risk and pinpoint design improvements; benchmarked against experimental wave-tank data to strengthen the chain from testing to analysis.</li>
        </ul>
      </div>
    </div>

    <div class="projrow reveal">
      <div class="pno">P-03</div>
      <div>
        <div class="ptitle">Master's Project — Liquid-Hydrogen / Electric Inland Tanker “HS Bremen”</div>
        <div class="pmeta"><span>Clean propulsion</span><span>Energy transition</span><span>Regulatory design</span></div>
        <ul class="pbody">
          <li>Designed a zero-emission, hydrogen-powered inland tanker for ammonia, methanol and liquid CO₂ on the Rhine — compliant with ADN, CCNR and Lloyd's Register standards. Produced detailed line plans in AutoCAD.</li>
          <li>Designed energy-efficient HVAC and air-exchange systems, and developed fire-safety plans with equipment and extinguisher calculations, navigating concept-to-readiness through iterative, cross-functional work.</li>
        </ul>
      </div>
    </div>

    <div class="projrow reveal">
      <div class="pno">P-04</div>
      <div>
        <div class="ptitle">Anisotropic Hyperelastic Material Calibration in ANSYS</div>
        <div class="pmeta"><span>FEM</span><span>Material modelling</span><span>ANSYS Workbench</span></div>
        <ul class="pbody">
          <li>Calibrated an anisotropic hyperelastic model for fibre-reinforced rubber from experimental stress–strain data, optimising parameters and validating accuracy through iterative simulation.</li>
          <li>Integrated the calibrated model into ANSYS Workbench for structural analysis and design validation.</li>
        </ul>
      </div>
    </div>

    <div class="projrow reveal">
      <div class="pno">P-05</div>
      <div>
        <div class="ptitle">Ship-Design Optimisation Tool in the CAESES Environment</div>
        <div class="pmeta"><span>Python</span><span>Automation</span><span>Design optimisation</span></div>
        <ul class="pbody">
          <li>Built a Python program coupled to CAESES that automatically evaluates alternative hull designs, making it fast to test many variants.</li>
          <li>Wrote routines to read ship geometry from CAESES, run calculations, post-process simulation results and suggest improvements — streamlining the design loop.</li>
        </ul>
      </div>
    </div>

  </div>
</section>

<!-- RECORD: experience + education -->
<section id="record" class="wrap">
  <div class="sec-head reveal"><span class="sec-no">04</span><h2>Track Record</h2><span class="station">Station 04</span></div>
  <div class="two">
    <div class="reveal">
      <div class="subhead">Experience</div>
      <div class="tl">
        <div class="tlitem">
          <h4>Production Engineer</h4>
          <div class="org">Krystal Global Engineering Ltd.</div>
          <div class="when">Vadodara, India</div>
          <ul>
            <li>Supported technical teams and enforced QA protocols for high-standard production of mechanical systems.</li>
            <li>Streamlined workflows through systematic testing and documentation, improving reliability and efficiency.</li>
            <li>Coordinated across departments to hit operational and customer goals; applied 5S, Kaizen and continuous improvement.</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="reveal">
      <div class="subhead">Education</div>
      <div class="tl">
        <div class="tlitem">
          <h4>M.Sc. Naval Architecture &amp; Ocean Engineering</h4>
          <div class="org">Hochschule Bremen — City University of Applied Sciences</div>
          <div class="when">Bremen, Germany · Present</div>
        </div>
        <div class="tlitem">
          <h4>B.E. Mechanical Engineering</h4>
          <div class="org">Gujarat Technological University</div>
          <div class="when">Vadodara, India · GPA 2.1</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATES -->
<section id="certs" class="certs">
  <div class="wrap">
    <div class="sec-head reveal"><span class="sec-no">05</span><h2>Certifications</h2><span class="station">5 verified · Udemy</span></div>
    <div class="certgrid">

      <a class="cert reveal" href="https://ude.my/UC-280f4ea1-845e-490e-b90b-858fcd7f58a7" target="_blank" rel="noopener">
        <div class="ctop"><span class="prov">Udemy</span><span class="hrs">34 hrs</span></div>
        <h3>The Finite Element Method (FEM / FEA)</h3>
        <div class="inst">Engineer Renato C.</div>
        <div class="cfoot"><span class="date">Jun 26, 2025</span><span class="verify">Verify<svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M5 12h14M13 6l6 6-6 6"/></svg></span></div>
      </a>

      <a class="cert reveal" href="https://ude.my/UC-d2c35e0b-83a8-484b-923b-4200f1669a35" target="_blank" rel="noopener">
        <div class="ctop"><span class="prov">Udemy</span><span class="hrs">8.5 hrs</span></div>
        <h3>Learn Python Programming: Step-By-Step Guide</h3>
        <div class="inst">Dr. Rakesh Roshan</div>
        <div class="cfoot"><span class="date">Jun 17, 2026</span><span class="verify">Verify<svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M5 12h14M13 6l6 6-6 6"/></svg></span></div>
      </a>

      <a class="cert reveal" href="https://ude.my/UC-6b7e814e-72db-438d-9bfb-3a783b96b8b0" target="_blank" rel="noopener">
        <div class="ctop"><span class="prov">Udemy</span><span class="hrs">13 hrs</span></div>
        <h3>Learn AutoCAD 2D &amp; 3D: From Zero to Hero</h3>
        <div class="inst">Ashish Pandit</div>
        <div class="cfoot"><span class="date">Jul 25, 2025</span><span class="verify">Verify<svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M5 12h14M13 6l6 6-6 6"/></svg></span></div>
      </a>

      <a class="cert reveal" href="https://ude.my/UC-cedeb8a6-a3cf-407b-bc93-202d871c35cc" target="_blank" rel="noopener">
        <div class="ctop"><span class="prov">Udemy</span><span class="hrs">3.5 hrs</span></div>
        <h3>The Ultimate Rhino Grasshopper Guide to Parametric Design</h3>
        <div class="inst">Brandon Aaron Gibbs</div>
        <div class="cfoot"><span class="date">Jun 22, 2025</span><span class="verify">Verify<svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M5 12h14M13 6l6 6-6 6"/></svg></span></div>
      </a>

      <a class="cert reveal" href="https://ude.my/UC-881fd227-790e-4244-adbd-eeaff82afcb5" target="_blank" rel="noopener">
        <div class="ctop"><span class="prov">Udemy</span><span class="hrs">4.5 hrs</span></div>
        <h3>Microsoft Excel — Basic &amp; Advanced Formulas</h3>
        <div class="inst">Yassin Marco, MBA</div>
        <div class="cfoot"><span class="date">Jun 27, 2025</span><span class="verify">Verify<svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M5 12h14M13 6l6 6-6 6"/></svg></span></div>
      </a>

    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="contact">
  <div class="hero-grid"></div>
  <div class="wrap">
    <span class="eyebrow reveal">Open to internship, working-student &amp; thesis roles</span>
    <h2 class="reveal">Let's build something that <em>floats</em>.</h2>
    <p class="reveal">I'm looking for hands-on roles in engineering simulation, design and analysis. If that's your world, I'd love to talk.</p>
    <div class="contact-actions reveal">
      <a class="btn btn-primary" href="mailto:darshangohiljob@gmail.com">
        <svg viewBox="0 0 24 24" fill="none" stroke-width="2"><rect x="3" y="5" width="18" height="14" rx="2"/><path d="m3 7 9 6 9-6"/></svg>
        darshangohiljob@gmail.com
      </a>
      <a class="btn btn-ghost" href="https://www.linkedin.com/in/darshan-vijay-gohil-18a69a259/" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" fill="none" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M8 11v5M8 8v.01M12 16v-3a2 2 0 0 1 4 0v3"/></svg>
        LinkedIn
      </a>
      <a class="btn btn-ghost" href="tel:+4917687321722">
        <svg viewBox="0 0 24 24" fill="none" stroke-width="2"><path d="M5 4h4l2 5-3 2a12 12 0 0 0 5 5l2-3 5 2v4a2 2 0 0 1-2 2A16 16 0 0 1 3 6a2 2 0 0 1 2-2z"/></svg>
        +49 176 8732 1722
      </a>
    </div>
    <footer>
      <span>© 2026 Darshan Vijay Gohil</span>
      <span>Bremen, Germany · 53.08°N 8.81°E</span>
      <a href="#top">Back to top ↑</a>
    </footer>
  </div>
</section>

<script>
  // Nav dock on scroll
  const nav=document.getElementById('nav');
  const onScroll=()=>{nav.classList.toggle('docked',window.scrollY>40)};
  onScroll();window.addEventListener('scroll',onScroll,{passive:true});

  // Scroll reveal
  const reduce=window.matchMedia('(prefers-reduced-motion:reduce)').matches;
  const items=document.querySelectorAll('.reveal');
  if(reduce||!('IntersectionObserver'in window)){
    items.forEach(el=>el.classList.add('in'));
  }else{
    const io=new IntersectionObserver((es)=>{
      es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target);}});
    },{threshold:0.12,rootMargin:'0px 0px -40px 0px'});
    items.forEach(el=>io.observe(el));
  }
</script>
</body>
</html>
