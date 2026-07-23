
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Curious Classroom — Language Educator &amp; Instructional Designer</title>

<!--
  ============================================================
  HOW TO EDIT THIS SITE
  ============================================================
  1. Search for "EDIT:" comments — they mark the spots you'll
     most likely want to change first (name, bio, contact info,
     links, resource items).
  2. Colors, fonts and spacing all live in the :root block below
     under "DESIGN TOKENS" — change a value there and it updates
     everywhere.
  3. Section content lives in plain HTML further down, grouped
     by <section id="..."> — matches the nav links at the top.
  4. Swap the portrait/hero placeholders (marked "PLACEHOLDER")
     for your own photos or artwork when ready.
  ============================================================
-->

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;1,9..144,400;1,9..144,500&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">

<style>
/* ============================================================
   DESIGN TOKENS — edit these to re-theme the whole site
   ============================================================ */
:root{
  --warm-white:  #FBF8F3;
  --ivory:       #F3EDE1;
  --sand:        #E8DFC9;
  --slate:       #4A5560;
  --navy:        #1F3347;
  --teal:        #3E7C74;
  --mustard:     #D9A441;
  --coral:       #E4694F;
  --sage:        #8AA286;

  --ink:         #24303B;
  --paper-line:  rgba(31,51,71,0.14);

  --font-display: 'Outfit', sans-serif;
  --font-accent:  'Fraunces', serif;
  --font-body:    'Inter', sans-serif;

  --radius-sm: 8px;
  --radius-md: 14px;
  --radius-lg: 24px;

  --shadow-soft: 0 10px 30px rgba(31,51,71,0.08);
  --shadow-lift: 0 18px 40px rgba(31,51,71,0.14);

  --maxw: 1180px;
}

*{box-sizing:border-box; margin:0; padding:0;}
html{scroll-behavior:smooth;}
body{
  font-family:var(--font-body);
  color:var(--ink);
  background:var(--warm-white);
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
}
img{max-width:100%; display:block;}
a{color:inherit; text-decoration:none;}
ul{list-style:none;}
button{font-family:inherit; cursor:pointer;}
:focus-visible{outline:3px solid var(--coral); outline-offset:3px;}

.wrap{max-width:var(--maxw); margin:0 auto; padding:0 32px;}
@media(max-width:640px){.wrap{padding:0 20px;}}

h1,h2,h3,h4{font-family:var(--font-display); color:var(--navy); font-weight:700; letter-spacing:-0.01em;}
.eyebrow{
  font-family:var(--font-display);
  font-size:0.72rem;
  font-weight:600;
  letter-spacing:0.14em;
  text-transform:uppercase;
  color:var(--teal);
  display:inline-flex;
  align-items:center;
  gap:8px;
}
.eyebrow::before{content:""; width:18px; height:2px; background:var(--coral); display:inline-block;}

.section{padding:96px 0;}
.section-head{max-width:640px; margin-bottom:56px;}
.section-head h2{font-size:clamp(1.8rem,3.2vw,2.6rem); margin-top:10px;}
.section-head p{color:var(--slate); margin-top:14px; font-size:1.05rem;}

@media(max-width:768px){.section{padding:64px 0;}}

/* subtle "ticket" divider used between major sections — echoes the
   catalog-card motif without becoming a numbered sequence */
.ticket-divider{
  border:none;
  border-top:1.5px dashed var(--paper-line);
  position:relative;
  margin:0;
}
.ticket-divider::before,
.ticket-divider::after{
  content:"";
  position:absolute; top:-9px;
  width:18px; height:18px;
  background:var(--warm-white);
  border-radius:50%;
  border:1.5px dashed var(--paper-line);
}
.ticket-divider::before{left:-9px;}
.ticket-divider::after{right:-9px;}

/* ============================================================
   NAV
   ============================================================ */
header.site-header{
  position:sticky; top:0; z-index:100;
  background:rgba(251,248,243,0.92);
  backdrop-filter:blur(10px);
  border-bottom:1px solid var(--paper-line);
}
.nav-inner{
  display:flex; align-items:center; justify-content:space-between;
  padding:16px 0;
}
.brand{
  font-family:var(--font-display); font-weight:800; font-size:1.15rem;
  color:var(--navy); display:flex; align-items:center; gap:10px;
}
.brand .mark{
  min-width:34px; height:34px; padding:0 7px; border-radius:9px;
  background:linear-gradient(135deg,var(--teal),var(--navy));
  display:flex; align-items:center; justify-content:center;
  color:var(--warm-white); font-family:var(--font-accent); font-style:italic; font-weight:600; font-size:0.85rem;
}
nav.primary-nav ul{display:flex; gap:26px;}
nav.primary-nav a{
  font-size:0.86rem; font-weight:600; color:var(--slate);
  padding:6px 2px; border-bottom:2px solid transparent;
  transition:color .2s, border-color .2s;
}
nav.primary-nav a:hover{color:var(--navy); border-color:var(--coral);}
.nav-cta{
  background:var(--navy); color:var(--warm-white)!important;
  padding:10px 18px; border-radius:999px; font-weight:600; font-size:0.85rem;
}
.nav-toggle{display:none; background:none; border:none; font-size:1.4rem; color:var(--navy);}
@media(max-width:920px){
  nav.primary-nav{
    display:none; position:absolute; top:100%; left:0; right:0;
    background:var(--warm-white); border-bottom:1px solid var(--paper-line);
    padding:18px 0; box-shadow:var(--shadow-soft);
  }
  nav.primary-nav.open{display:block;}
  nav.primary-nav ul{flex-direction:column; gap:0; padding:0 32px;}
  nav.primary-nav li{border-bottom:1px solid var(--paper-line);}
  nav.primary-nav a{display:block; padding:14px 0;}
  .nav-toggle{display:block;}
}

/* ============================================================
   HERO
   ============================================================ */
.hero{
  padding:80px 0 60px;
  position:relative;
  overflow:hidden;
}
.hero::before{
  content:"";
  position:absolute; inset:0;
  background:
    radial-gradient(600px 300px at 85% -10%, rgba(217,164,65,0.18), transparent),
    radial-gradient(500px 260px at -5% 20%, rgba(62,124,116,0.14), transparent);
  pointer-events:none;
}
.hero-grid{
  position:relative;
  display:grid; grid-template-columns:1.1fr 0.9fr; gap:56px; align-items:center;
}
@media(max-width:860px){.hero-grid{grid-template-columns:1fr;}}

.hero-greeting{
  font-family:var(--font-accent); font-style:italic; font-weight:500;
  color:var(--coral); font-size:1.2rem; height:1.6em;
}
.hero h1{
  font-size:clamp(2.1rem,4.4vw,3.4rem); line-height:1.12; margin-top:14px;
}
.hero h1 em{font-style:normal; color:var(--teal);}
.hero .lede{
  margin-top:20px; font-size:1.12rem; color:var(--slate); max-width:52ch;
}
.cta-row{display:flex; flex-wrap:wrap; gap:14px; margin-top:32px;}
.btn{
  display:inline-flex; align-items:center; gap:8px;
  padding:13px 24px; border-radius:999px; font-weight:600; font-size:0.92rem;
  transition:transform .18s ease, box-shadow .18s ease;
  border:1.5px solid transparent;
}
.btn:hover{transform:translateY(-2px);}
.btn-primary{background:var(--navy); color:var(--warm-white); box-shadow:var(--shadow-soft);}
.btn-primary:hover{box-shadow:var(--shadow-lift);}
.btn-secondary{background:transparent; color:var(--navy); border-color:var(--navy);}
.btn-secondary:hover{background:var(--navy); color:var(--warm-white);}
.btn-ghost{background:var(--sand); color:var(--navy);}
.btn-ghost:hover{background:var(--mustard); color:var(--navy);}

.hero-stats{display:flex; gap:32px; margin-top:44px; flex-wrap:wrap;}
.hero-stats div strong{display:block; font-family:var(--font-display); font-size:1.5rem; color:var(--navy);}
.hero-stats div span{font-size:0.8rem; color:var(--slate);}

/* portrait placeholder — swap for a real photo */
.portrait-card{
  position:relative;
  aspect-ratio:4/5;
  border-radius:var(--radius-lg);
  background:linear-gradient(155deg,var(--teal) 0%, var(--navy) 100%);
  box-shadow:var(--shadow-lift);
  display:flex; align-items:center; justify-content:center;
  color:rgba(251,248,243,0.85);
  text-align:center; padding:32px;
  overflow:hidden;
}
.portrait-card::after{
  content:"";
  position:absolute; inset:0;
  background-image: radial-gradient(rgba(251,248,243,0.16) 1.5px, transparent 1.5px);
  background-size:16px 16px;
  opacity:.5;
}
.portrait-card .ph-inner{position:relative; z-index:1;}
.portrait-card .ph-icon{font-family:var(--font-accent); font-style:italic; font-size:3.4rem;}
.portrait-card small{display:block; margin-top:10px; font-size:0.78rem; letter-spacing:0.05em; text-transform:uppercase;}
.stamp{
  position:absolute; top:22px; right:-38px;
  transform:rotate(20deg);
  background:var(--coral); color:var(--warm-white);
  font-family:var(--font-display); font-weight:700; font-size:0.7rem;
  padding:6px 42px; letter-spacing:0.08em;
  box-shadow:0 6px 14px rgba(0,0,0,0.18);
}

/* ============================================================
   ABOUT
   ============================================================ */
.about-grid{display:grid; grid-template-columns:0.85fr 1.15fr; gap:64px;}
@media(max-width:860px){.about-grid{grid-template-columns:1fr;}}
.value-list{display:grid; gap:18px; margin-top:28px;}
.value-item{
  display:flex; gap:14px; padding:16px; background:var(--ivory);
  border-radius:var(--radius-md);
}
.value-item .dot{
  width:10px; height:10px; border-radius:50%; margin-top:6px; flex:none;
  background:var(--mustard);
}
.value-item h4{font-size:0.98rem;}
.value-item p{color:var(--slate); font-size:0.92rem; margin-top:4px;}

.timeline{margin-top:44px; border-left:2px solid var(--paper-line); padding-left:28px; display:grid; gap:30px;}
.timeline .tl-item{position:relative;}
.timeline .tl-item::before{
  content:""; position:absolute; left:-34px; top:4px;
  width:12px; height:12px; border-radius:50%; background:var(--teal); border:3px solid var(--warm-white); box-shadow:0 0 0 2px var(--teal);
}
.timeline .tl-year{font-family:var(--font-display); font-weight:700; color:var(--coral); font-size:0.85rem; letter-spacing:0.04em;}
.timeline h4{margin-top:4px;}
.timeline p{color:var(--slate); font-size:0.92rem; margin-top:4px;}

/* resume card */
.resume-panel{
  margin-top:40px; padding:32px; border-radius:var(--radius-lg);
  background:var(--navy); color:var(--warm-white);
  display:flex; flex-wrap:wrap; gap:24px; align-items:center; justify-content:space-between;
}
.resume-panel h3{color:var(--warm-white);}
.resume-panel p{color:rgba(251,248,243,0.75); margin-top:6px; max-width:44ch; font-size:0.94rem;}
.resume-actions{display:flex; gap:12px; flex-wrap:wrap;}
.resume-panel .btn-primary{background:var(--mustard); color:var(--navy);}
.resume-panel .btn-secondary{border-color:rgba(251,248,243,0.5); color:var(--warm-white);}
.resume-panel .btn-secondary:hover{background:rgba(251,248,243,0.12); color:var(--warm-white);}

/* ============================================================
   TABS (Teaching)
   ============================================================ */
.catalog{
  background:var(--ivory); border-radius:var(--radius-lg); padding:8px;
}
.tab-bar{display:flex; flex-wrap:wrap; gap:8px; padding:14px;}
.tab-btn{
  padding:10px 18px; border-radius:999px; background:var(--warm-white);
  font-weight:600; font-size:0.88rem; color:var(--slate);
  border:1.5px solid var(--paper-line);
}
.tab-btn.active{background:var(--navy); color:var(--warm-white); border-color:var(--navy);}
.tab-panels{padding:8px 14px 22px;}
.tab-panel{display:none;}
.tab-panel.active{display:block; animation:fadein .35s ease;}
@keyframes fadein{from{opacity:0; transform:translateY(6px);} to{opacity:1; transform:none;}}

.subject-grid{display:grid; grid-template-columns:1fr 1fr; gap:24px;}
@media(max-width:760px){.subject-grid{grid-template-columns:1fr;}}
.subject-copy p{color:var(--slate); margin-top:10px;}
.pill-row{display:flex; flex-wrap:wrap; gap:8px; margin-top:16px;}
.pill{
  font-size:0.78rem; font-weight:600; color:var(--teal);
  background:rgba(62,124,116,0.1); padding:6px 12px; border-radius:999px;
}
.include-card{
  background:var(--warm-white); border-radius:var(--radius-md);
  padding:22px; box-shadow:var(--shadow-soft);
}
.include-card h4{font-size:0.9rem; text-transform:uppercase; letter-spacing:0.06em; color:var(--coral); font-family:var(--font-display);}
.include-card ul{margin-top:12px; display:grid; gap:8px;}
.include-card li{font-size:0.92rem; color:var(--ink); padding-left:18px; position:relative;}
.include-card li::before{content:"—"; position:absolute; left:0; color:var(--mustard);}

/* ============================================================
   CARD GRIDS (Curriculum / EdTech / Products / Blog)
   ============================================================ */
.card-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:26px;}
.card{
  background:var(--warm-white); border:1px solid var(--paper-line);
  border-radius:var(--radius-lg); padding:26px; box-shadow:var(--shadow-soft);
  display:flex; flex-direction:column; gap:12px; transition:transform .2s, box-shadow .2s;
}
.card:hover{transform:translateY(-4px); box-shadow:var(--shadow-lift);}
.card .tag{
  align-self:flex-start; font-size:0.72rem; font-weight:700; text-transform:uppercase;
  letter-spacing:0.06em; color:var(--warm-white); background:var(--teal);
  padding:4px 10px; border-radius:6px;
}
.card h3{font-size:1.15rem;}
.card p{color:var(--slate); font-size:0.93rem;}
.card .meta{
  margin-top:auto; display:flex; justify-content:space-between; align-items:center;
  font-size:0.82rem; color:var(--slate); border-top:1px dashed var(--paper-line); padding-top:12px;
}
.card .meta a{color:var(--coral); font-weight:700;}

/* curriculum project detail row */
.curric-card ol{margin-top:10px; display:grid; gap:6px; padding-left:0;}
.curric-card ol li{
  list-style:none; font-size:0.86rem; color:var(--ink);
  display:flex; gap:8px;
}
.curric-card ol li b{color:var(--teal); flex:none; min-width:96px;}

/* edtech tool tiles */
.tool-tile{
  display:flex; flex-direction:column; align-items:flex-start; gap:8px;
  background:var(--ivory); border-radius:var(--radius-md); padding:20px;
}
.tool-tile .tool-icon{
  width:38px; height:38px; border-radius:10px; background:var(--warm-white);
  display:flex; align-items:center; justify-content:center; font-family:var(--font-display); font-weight:800; color:var(--navy);
  box-shadow:var(--shadow-soft);
}
.tool-tile h4{font-size:0.98rem;}
.tool-tile p{font-size:0.85rem; color:var(--slate);}

/* ============================================================
   RESOURCE LIBRARY
   ============================================================ */
.library-controls{
  display:flex; flex-wrap:wrap; gap:10px; align-items:center; justify-content:space-between;
  margin-bottom:28px; padding:16px 20px; background:var(--ivory); border-radius:var(--radius-md);
}
.search-box{
  display:flex; align-items:center; gap:10px; background:var(--warm-white);
  border-radius:999px; padding:10px 16px; flex:1; min-width:220px; border:1px solid var(--paper-line);
}
.search-box input{border:none; outline:none; background:none; width:100%; font-family:inherit; font-size:0.92rem;}
.filter-row{display:flex; flex-wrap:wrap; gap:8px;}
.filter-chip{
  padding:7px 14px; border-radius:999px; font-size:0.8rem; font-weight:600;
  background:var(--warm-white); border:1px solid var(--paper-line); color:var(--slate);
}
.filter-chip.active{background:var(--mustard); border-color:var(--mustard); color:var(--navy);}
.resource-item{
  background:var(--warm-white); border:1px solid var(--paper-line); border-radius:var(--radius-md);
  padding:20px; display:flex; flex-direction:column; gap:10px;
}
.resource-item .cat{font-size:0.72rem; font-weight:700; color:var(--teal); text-transform:uppercase; letter-spacing:0.05em;}
.resource-item .rlinks{display:flex; gap:14px; font-size:0.82rem; margin-top:auto;}
.resource-item .rlinks a{color:var(--coral); font-weight:700;}
.empty-state{text-align:center; padding:50px 20px; color:var(--slate); display:none;}
.empty-state.show{display:block;}

/* ============================================================
   PHILOSOPHY (pull quotes)
   ============================================================ */
.philosophy-wrap{
  background:var(--navy); border-radius:var(--radius-lg); padding:64px 48px; color:var(--warm-white);
}
@media(max-width:640px){.philosophy-wrap{padding:44px 26px;}}
.philosophy-wrap .eyebrow{color:var(--mustard);}
.philosophy-wrap .eyebrow::before{background:var(--coral);}
.philosophy-quote{
  font-family:var(--font-accent); font-style:italic; font-weight:400;
  font-size:clamp(1.3rem,2.6vw,2rem); line-height:1.4; margin:18px 0 40px; max-width:820px; color:var(--warm-white);
}
.philosophy-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:24px;}
.philosophy-grid div h4{color:var(--mustard); font-size:0.98rem;}
.philosophy-grid div p{color:rgba(251,248,243,0.78); font-size:0.9rem; margin-top:6px;}

/* ============================================================
   PROFESSIONAL DEVELOPMENT
   ============================================================ */
.pd-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(240px,1fr)); gap:20px;}
.pd-item{
  border:1px solid var(--paper-line); border-radius:var(--radius-md); padding:20px;
  background:var(--warm-white);
}
.pd-item .pd-year{font-size:0.78rem; color:var(--coral); font-weight:700;}
.pd-item h4{margin-top:4px; font-size:0.98rem;}
.pd-item p{font-size:0.86rem; color:var(--slate); margin-top:4px;}

/* ============================================================
   CONTACT
   ============================================================ */
.contact-grid{display:grid; grid-template-columns:1fr 1fr; gap:56px; align-items:start;}
@media(max-width:860px){.contact-grid{grid-template-columns:1fr;}}
.contact-form{display:grid; gap:16px;}
.contact-form label{font-size:0.82rem; font-weight:600; color:var(--slate); display:block; margin-bottom:6px;}
.contact-form input, .contact-form select, .contact-form textarea{
  width:100%; padding:12px 14px; border-radius:var(--radius-sm); border:1.5px solid var(--paper-line);
  font-family:inherit; font-size:0.94rem; background:var(--warm-white);
}
.contact-form textarea{min-height:120px; resize:vertical;}
.contact-links{display:grid; gap:14px; margin-top:22px;}
.contact-links a{
  display:flex; align-items:center; gap:12px; padding:14px 16px; background:var(--ivory);
  border-radius:var(--radius-md); font-weight:600; font-size:0.92rem; color:var(--navy);
}
.contact-links a:hover{background:var(--sand);}
.form-note{font-size:0.8rem; color:var(--slate); margin-top:6px;}

/* ============================================================
   FOOTER
   ============================================================ */
footer{background:var(--ivory); padding:52px 0 28px; margin-top:40px;}
.footer-grid{display:grid; grid-template-columns:2fr 1fr 1fr 1fr; gap:32px;}
@media(max-width:760px){.footer-grid{grid-template-columns:1fr 1fr;}}
.footer-grid h5{font-family:var(--font-display); font-size:0.82rem; text-transform:uppercase; letter-spacing:0.06em; color:var(--navy); margin-bottom:14px;}
.footer-grid ul{display:grid; gap:8px;}
.footer-grid a{font-size:0.88rem; color:var(--slate);}
.footer-grid a:hover{color:var(--coral);}
.footer-bottom{
  margin-top:40px; padding-top:20px; border-top:1px solid var(--paper-line);
  display:flex; justify-content:space-between; flex-wrap:wrap; gap:10px;
  font-size:0.8rem; color:var(--slate);
}

/* future features strip */
.future-strip{
  display:flex; flex-wrap:wrap; gap:10px; margin-top:20px;
}
.future-chip{
  font-size:0.78rem; padding:7px 14px; border-radius:999px;
  border:1.5px dashed var(--paper-line); color:var(--slate);
}

@media (prefers-reduced-motion: reduce){
  *{animation-duration:0.001ms !important; transition-duration:0.001ms !important;}
  html{scroll-behavior:auto;}
}

/* ============================================================
   TAB-BASED PAGE NAVIGATION
   Only one .page-section is visible at a time; the header nav,
   hero buttons and footer links all switch between them via
   data-target instead of scrolling to an anchor.
   ============================================================ */
.page-section{display:none;}
.page-section.active{display:block; animation:pagefade .3s ease;}
@keyframes pagefade{from{opacity:0; transform:translateY(8px);} to{opacity:1; transform:none;}}
hr.ticket-divider{display:none;} /* not needed once sections are shown one at a time */
main{min-height:60vh;}
nav.primary-nav a.current, nav.primary-nav a.current.nav-cta{color:var(--coral); border-color:var(--coral);}
.nav-cta.current{background:var(--coral);}
</style>
</head>
<body>

<!-- ============================================================
     HEADER / NAV
     ============================================================ -->
<header class="site-header">
  <div class="wrap nav-inner">
    <a href="javascript:void(0)" data-target="home" class="brand">
      <span class="mark">TCC</span>
      <!-- EDIT: your name / brand -->
      The Curious Classroom
    </a>
    <nav class="primary-nav" id="primaryNav">
      <ul>
        <li><a href="javascript:void(0)" data-target="about">About</a></li>
        <li><a href="javascript:void(0)" data-target="teaching">Teaching</a></li>
        <li><a href="javascript:void(0)" data-target="curriculum">Curriculum</a></li>
        <li><a href="javascript:void(0)" data-target="edtech">EdTech</a></li>
        <li><a href="javascript:void(0)" data-target="library">Resources</a></li>
        <li><a href="javascript:void(0)" data-target="products">Products</a></li>
        <li><a href="javascript:void(0)" data-target="philosophy">Philosophy</a></li>
        <li><a href="javascript:void(0)" data-target="blog">Blog</a></li>
        <li><a href="javascript:void(0)" data-target="contact" class="nav-cta">Book a Session</a></li>
      </ul>
    </nav>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">☰</button>
  </div>
</header>

<!-- ============================================================
     HOME / HERO
     ============================================================ -->
<section class="hero page-section active" id="home">
  <div class="wrap hero-grid">
    <div>
      <div class="hero-greeting" id="greetingRotator">Bonjour.</div>
      <h1>Creating engaging language learning experiences through <em>curriculum</em>, technology, and thoughtful instruction.</h1>
      <p class="lede">
        I'm Teacher V, a language educator and instructional designer who
        builds classrooms, instructional resources and learning materials,
        using digital tools, that help students read deeper, speak with
        confidence, and think for themselves in English, French, and Spanish.
      </p>
      <div class="cta-row">
        <a href="javascript:void(0)" data-target="about" class="btn btn-primary">View Professional Experience</a>
        <a href="javascript:void(0)" data-target="teaching" class="btn btn-secondary">Explore Portfolio</a>
        <a href="javascript:void(0)" data-target="library" class="btn btn-ghost">Instructional Resources</a>
        <a href="javascript:void(0)" data-target="contact" class="btn btn-ghost">Book a Session</a>
      </div>
      <div class="hero-stats">
        <div><strong>8+ yrs</strong><span>Instructional design &amp; delivery experience</span></div>
        <div><strong>3</strong><span>Languages taught</span></div>
        <div><strong>100+</strong><span>Original resources curated</span></div>
        <div><strong>40+</strong><span>Curriculum units designed</span></div>
      </div>
    </div>
    <div class="portrait-card">
      <div class="stamp">Est. Learner</div>
      <div class="ph-inner">
        <div class="ph-icon" style="font-size:2.2rem;">TCC</div>
        <small>Portrait placeholder — swap for your photo</small>
      </div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     ABOUT
     ============================================================ -->
<section class="section page-section" id="about">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">About</span>
      <h2>Teaching, designed with intention.</h2>
      <p>My path from the classroom to curriculum design, and the beliefs that guide every lesson I build.</p>
    </div>

    <div class="about-grid">
      <div>
        <!-- EDIT: your bio -->
        <p>
          I started as a volunteer substitute and teacher's assistant of
          secondary English Language and Literature. I quickly became the
          person colleagues asked to help redesign a struggling unit or
          turn a flat lesson into something students actually leaned into.
          That instinct for structure, clarity, and curiosity is now the
          throughline of my work as an instructional designer and
          multimodal language educator.
        </p>
        <p style="margin-top:14px;">
          I have taught ELA and expanded into French and Spanish
          instruction, literacy intervention, and educational technology.
          Today I split my time between tutoring, designing learning
          experiences reaching students and classrooms nationwide, and
          building digital resources that other educators use in their own
          classrooms.
        </p>

        <div class="value-list">
          <div class="value-item">
            <span class="dot"></span>
            <div><h4>Student-centred, always</h4><p>Every unit starts with who the learner is, not what the standard says.</p></div>
          </div>
          <div class="value-item">
            <span class="dot"></span>
            <div><h4>Evidence over opinion</h4><p>Instructional decisions are backed by assessment data and reflection, not habit.</p></div>
          </div>
          <div class="value-item">
            <span class="dot"></span>
            <div><h4>Technology in service of learning</h4><p>Tools are chosen for the outcome they unlock, never used for their own sake.</p></div>
          </div>
        </div>
      </div>

      <div>
        <h3 style="margin-bottom:6px;">My Journey</h3>
        <div class="timeline">
          <div class="tl-item">
            <div class="tl-year">2018 – present</div>
            <h4>Tutoring</h4>
            <p>Launched a private tutoring practice assisting students to pass the CXC/CSEC.</p>
          </div>
          <div class="tl-item">
            <div class="tl-year">2018–2020; 2023</div>
            <h4>In-person Classroom Instruction</h4>
            <p>Managed and curated English Language and Literature learning experiences for secondary school classes averaging 40+ students per class.</p>
          </div>
          <div class="tl-item">
            <div class="tl-year">2020–2022; 2024 – present</div>
            <h4>Online/Virtual Instructor</h4>
            <p>Design and deliver English Language, English Literature, French and Spanish learning experiences for secondary school students.</p>
          </div>
          <div class="tl-item">
            <div class="tl-year">2021</div>
            <h4>TEFL Certification</h4>
            <p>Extended practice into English and French as additional-language instruction.</p>
          </div>
          <div class="tl-item">
            <div class="tl-year">2023 – present</div>
            <h4>Instructional Designer, Virtual Instructor, EdTech</h4>
            <p>Built interactive digital lessons and resources for a virtual academy used by students in over 100 schools across Jamaica.</p>
          </div>
          <div class="tl-item">
            <div class="tl-year">2024</div>
            <h4>BA French; Language Education: English</h4>
            <p>Pursued my first degree while teaching secondary English Language Arts.</p>
          </div>
          <div class="tl-item">
            <div class="tl-year">2025</div>
            <h4>FLE Certification</h4>
            <p>Français Langue Étrangère.</p>
          </div>
          <div class="tl-item">
            <div class="tl-year">Summer 2026</div>
            <h4>Reading, Writing and Story Time Literacy Program</h4>
            <p>Designed and delivered a virtual summer reading program, reaching Primary level students from across the island.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- RESUME -->
    <div class="resume-panel" id="resume">
      <div>
        <h3>Résumé &amp; credentials</h3>
        <p>A one-page snapshot of my teaching experience, certifications, and education — the full CV is one click away.</p>
      </div>
      <div class="resume-actions">
        <a href="javascript:void(0)" class="btn btn-primary">Download CV (PDF)</a>
        <a href="javascript:void(0)" class="btn btn-secondary">View on LinkedIn</a>
      </div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     TEACHING — tabbed by subject
     ============================================================ -->
<section class="section page-section" id="teaching">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Teaching</span>
      <h2>Organised by subject, built for the learner in front of me.</h2>
      <p>Lesson plans, activities, and assessment examples from three areas of classroom practice.</p>
    </div>

    <div class="catalog">
      <div class="tab-bar" id="tabBar">
        <button class="tab-btn active" data-tab="ela">English Language Arts</button>
        <button class="tab-btn" data-tab="reading">Reading</button>
        <button class="tab-btn" data-tab="mfl">Modern Foreign Languages</button>
      </div>

      <div class="tab-panels">

        <div class="tab-panel active" data-panel="ela">
          <div class="subject-grid">
            <div class="subject-copy">
              <h3>English Language Arts</h3>
              <p>Reading, writing, grammar, vocabulary, literature, and critical thinking, taught through
                inquiry and real texts rather than isolated drills.</p>
              <div class="pill-row">
                <span class="pill">Reading</span><span class="pill">Writing</span>
                <span class="pill">Grammar</span><span class="pill">Vocabulary</span>
                <span class="pill">Literature</span><span class="pill">Critical Thinking</span>
              </div>
            </div>
            <div class="include-card">
              <h4>What's included</h4>
              <ul>
                <li>Lesson plans &amp; slide decks</li>
                <li>Student activities &amp; games</li>
                <li>Worksheets &amp; reading passages</li>
                <li>Project-based units</li>
                <li>Learning outcomes &amp; reflection notes</li>
                <li>Assessment examples</li>
              </ul>
            </div>
          </div>
        </div>

        <div class="tab-panel" data-panel="reading">
          <div class="subject-grid">
            <div class="subject-copy">
              <h3>Reading</h3>
              <p>From phonological awareness through comprehension strategy, with an emphasis on
                early intervention and measurable growth.</p>
              <div class="pill-row">
                <span class="pill">Phonics</span><span class="pill">Fluency</span>
                <span class="pill">Comprehension</span><span class="pill">Guided Reading</span>
                <span class="pill">Shared Reading</span><span class="pill">Intervention</span>
              </div>
            </div>
            <div class="include-card">
              <h4>What's included</h4>
              <ul>
                <li>Literacy intervention plans</li>
                <li>Reading strategy posters</li>
                <li>Reading games &amp; centres</li>
                <li>Assessment &amp; running-record examples</li>
                <li>Before / after student growth samples <em>(anonymised)</em></li>
              </ul>
            </div>
          </div>
        </div>

        <div class="tab-panel" data-panel="mfl">
          <div class="subject-grid">
            <div class="subject-copy">
              <h3>Modern Foreign Languages</h3>
              <p>French &amp; Spanish. A communicative approach — speaking and listening first — supported
                by reader-response writing and cultural context. Beginner-friendly resources built around
                conversation and confidence from the very first lesson.</p>
              <div class="pill-row">
                <span class="pill">Speaking</span><span class="pill">Listening</span>
                <span class="pill">Reading</span><span class="pill">Writing</span>
                <span class="pill">Culture</span><span class="pill">CLT</span>
                <span class="pill">Conversation</span><span class="pill">Pronunciation</span>
              </div>
            </div>
            <div class="include-card">
              <h4>What's included</h4>
              <ul>
                <li>Interactive slides, lessons &amp; presentations</li>
                <li>Conversation practice &amp; pronunciation activities</li>
                <li>Vocabulary games &amp; projects</li>
                <li>Reader-response activities</li>
                <li>Assessment samples</li>
              </ul>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     CURRICULUM DESIGN
     ============================================================ -->
<section class="section page-section" id="curriculum">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Instructional and Curriculum Design</span>
      <h2>Instructional design work, from map to classroom.</h2>
      <p>A selection of curriculum projects — each one includes the problem, the design approach, and the outcome.</p>
    </div>

    <div class="card-grid">
      <div class="card curric-card">
        <span class="tag">Backward Design</span>
        <h3>Primary School Summer Reading, Writing and Story Time Program</h3>
        <p>A two-week unit rebuilding literacy and reading comprehension instruction around backward design and UDL.</p>
        <ol>
          <li><b>Learners</b> Grade 1-3 and grades 4-6, mixed proficiency</li>
          <li><b>Standards</b> National Standards Curriculum Literacy Strands</li>
          <li><b>Technology</b> Nearpod, Genially, Zoom</li>
        </ol>
        <div class="meta"><span>Curriculum map · Unit plan · Rubric</span><a href="javascript:void(0)">View project →</a></div>
      </div>

      <div class="card curric-card">
        <span class="tag">Play-Based</span>
        <h3>Early Literacy Foundations (Pre-K)</h3>
        <p>A phonics-through-play curriculum built for homeschool and small-group settings.</p>
        <ol>
          <li><b>Learners</b> Pre-Kindergarten</li>
          <li><b>Design</b> Play-based, inquiry learning</li>
          <li><b>Technology</b> Printables, decodable readers, physical media, language manipulatives</li>
        </ol>
        <div class="meta"><span>Scope &amp; sequence · Activities</span><a href="javascript:void(0)">View project →</a></div>
      </div>

      <div class="card curric-card">
        <span class="tag">Mini Courses</span>
        <h3>CSEC English Literature</h3>
        <p>Poetry, prose and drama units delivered over several weeks as courses within each term.</p>
        <ol>
          <li><b>Learners</b> Secondary – Grades 10-11</li>
          <li><b>Design</b> Reader Response, Critical Reading and Analysis, Socratic Reasoning</li>
          <li><b>Technology</b> Nearpod, Wordwall, Genially</li>
        </ol>
        <div class="meta"><span>Unit plans · Reading lists · Assessment</span><a href="javascript:void(0)">View project →</a></div>
      </div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     EDUCATIONAL TECHNOLOGY
     ============================================================ -->
<section class="section page-section" id="edtech">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Educational Technology</span>
      <h2>Tools I use, and why I choose them.</h2>
      <p>Technology earns a place in my lessons only when it makes the learning better — not just different.</p>
    </div>

    <div class="card-grid" style="grid-template-columns:repeat(auto-fit,minmax(220px,1fr));">
      <div class="tool-tile"><div class="tool-icon">N</div><h4>Nearpod</h4><p>Interactive, branching lessons with real-time formative checks.</p></div>
      <div class="tool-tile"><div class="tool-icon">G</div><h4>Genially</h4><p>High engagement, collaborative, gamified resource creator.</p></div>
      <div class="tool-tile"><div class="tool-icon">C</div><h4>Canva</h4><p>Fast, on-brand visual resources and student-facing materials.</p></div>
      <div class="tool-tile"><div class="tool-icon">K</div><h4>Kahoot!</h4><p>Low-stakes retrieval practice that keeps energy in the room.</p></div>
      <div class="tool-tile"><div class="tool-icon">W</div><h4>Wayground <span style="font-weight:400; color:var(--slate); font-size:0.78rem;">(formerly Quizizz)</span></h4><p>Self-paced formative assessment with instant item analysis.</p></div>
      <div class="tool-tile"><div class="tool-icon">✂</div><h4>Manual Craft Supplies</h4><p>Hands-on project- and play-based learning will never lose its place in the education sphere.</p></div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     RESOURCE LIBRARY
     ============================================================ -->
<section class="section page-section" id="library">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Resource Library</span>
      <h2>Search the catalog.</h2>
      <p>Browse and filter — this is a working demo of the search/filter interaction; connect it to a real
        database of files when you're ready to publish.</p>
    </div>

    <div class="library-controls">
      <div class="search-box">
        <span>⌕</span>
        <input type="text" id="librarySearch" placeholder="Search resources… e.g. “vocabulary”, “French”">
      </div>
      <div class="filter-row" id="filterRow">
        <button class="filter-chip active" data-filter="all">All</button>
        <button class="filter-chip" data-filter="Lesson Plans">Lesson Plans</button>
        <button class="filter-chip" data-filter="Reading">Reading</button>
        <button class="filter-chip" data-filter="Grammar">Grammar</button>
        <button class="filter-chip" data-filter="French">French</button>
        <button class="filter-chip" data-filter="Spanish">Spanish</button>
        <button class="filter-chip" data-filter="Games">Games</button>
        <button class="filter-chip" data-filter="SEL">SEL</button>
      </div>
    </div>

    <!-- EDIT: replace with your real resources -->
    <div class="card-grid" id="libraryGrid">
      <div class="resource-item" data-cat="Lesson Plans" data-title="Story Mountain Narrative Writing Lesson">
        <span class="cat">Lesson Plans</span>
        <h4>Story Mountain: Narrative Writing</h4>
        <p style="color:var(--slate); font-size:0.9rem;">A full lesson plan teaching narrative structure through story-mapping.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
      <div class="resource-item" data-cat="Reading" data-title="Guided Reading Comprehension Bundle">
        <span class="cat">Reading</span>
        <h4>Guided Reading Comprehension Bundle</h4>
        <p style="color:var(--slate); font-size:0.9rem;">Levelled passages with comprehension questions and running-record sheets.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
      <div class="resource-item" data-cat="Grammar" data-title="Parts of Speech Card Sort Game">
        <span class="cat">Grammar</span>
        <h4>Parts of Speech Card Sort</h4>
        <p style="color:var(--slate); font-size:0.9rem;">A hands-on sorting game for identifying nouns, verbs, and adjectives.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
      <div class="resource-item" data-cat="French" data-title="French Conversation Starter Cards">
        <span class="cat">French</span>
        <h4>Conversation Starter Cards</h4>
        <p style="color:var(--slate); font-size:0.9rem;">40 speaking prompts for A1–A2 French learners, with sentence stems.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
      <div class="resource-item" data-cat="Spanish" data-title="Spanish Vocabulary Bingo">
        <span class="cat">Spanish</span>
        <h4>Vocabulary Bingo — Everyday Objects</h4>
        <p style="color:var(--slate); font-size:0.9rem;">A printable and digital bingo set for beginner vocabulary practice.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
      <div class="resource-item" data-cat="Games" data-title="Vocabulary Battleship Game">
        <span class="cat">Games</span>
        <h4>Vocabulary Battleship</h4>
        <p style="color:var(--slate); font-size:0.9rem;">A partner game that turns word review into friendly competition.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
      <div class="resource-item" data-cat="SEL" data-title="Classroom Character Education Posters">
        <span class="cat">SEL</span>
        <h4>Character Education Poster Set</h4>
        <p style="color:var(--slate); font-size:0.9rem;">Eight printable posters supporting respect, empathy, and responsibility.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
      <div class="resource-item" data-cat="Lesson Plans" data-title="5E Science of Reading Lesson">
        <span class="cat">Lesson Plans</span>
        <h4>5E Lesson: Reading for Inference</h4>
        <p style="color:var(--slate); font-size:0.9rem;">An inquiry-based 5E lesson plan for teaching inference skills.</p>
        <div class="rlinks"><a href="javascript:void(0)">Preview</a><a href="javascript:void(0)">Download</a></div>
      </div>
    </div>
    <p class="empty-state" id="emptyState">No resources match your search yet — try another keyword or filter.</p>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     DIGITAL PRODUCTS
     ============================================================ -->
<section class="section page-section" id="products">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Digital Products</span>
      <h2>Resources you can bring straight into your classroom or home.</h2>
      <p>Original curriculum and activity packs, ready to preview and download.</p>
    </div>

    <div class="card-grid">
      <div class="card">
        <span class="tag">Literacy</span>
        <h3>Emily's Amazing Adventures</h3>
        <p>An early-literacy story series pairing decodable text with comprehension activities.</p>
        <div class="meta"><span>Ages 5–7 · Reading, Vocabulary</span><a href="javascript:void(0)">Preview →</a></div>
      </div>
      <div class="card">
        <span class="tag">Homeschool</span>
        <h3>Toddler Routine Cards</h3>
        <p>Visual routine cards to build independence and language around daily habits.</p>
        <div class="meta"><span>Ages 2–4 · Language, Routine</span><a href="javascript:void(0)">Preview →</a></div>
      </div>
      <div class="card">
        <span class="tag">Assessment</span>
        <h3>Reading Assessment Bank</h3>
        <p>A bank of levelled comprehension checks with answer keys and rubrics.</p>
        <div class="meta"><span>Grades 1–6 · Reading</span><a href="javascript:void(0)">Preview →</a></div>
      </div>
      <div class="card">
        <span class="tag">Character Education</span>
        <h3>Growing Good Humans Pack</h3>
        <p>SEL discussion prompts and activities built around eight core character traits.</p>
        <div class="meta"><span>Grades K–5 · SEL</span><a href="javascript:void(0)">Preview →</a></div>
      </div>
      <div class="card">
        <span class="tag">Interactive</span>
        <h3>Grammar Ranch — Interactive Slides</h3>
        <p>A self-paced digital grammar unit with built-in checks for understanding.</p>
        <div class="meta"><span>Grades 3–6 · Grammar</span><a href="javascript:void(0)">Preview →</a></div>
      </div>
      <div class="card" style="border-style:dashed;">
        <span class="tag" style="background:var(--mustard); color:var(--navy);">Coming Soon</span>
        <h3>Online Course: Teaching Reading with Confidence</h3>
        <p>A self-paced course for new teachers building their first literacy program.</p>
        <div class="meta"><span>For educators</span><a href="javascript:void(0)">Join the waitlist →</a></div>
      </div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     TEACHING PHILOSOPHY
     ============================================================ -->
<section class="section page-section" id="philosophy">
  <div class="wrap">
    <div class="philosophy-wrap">
      <span class="eyebrow">Teaching Philosophy</span>
      <p class="philosophy-quote">
        "I teach because I remember what it felt like to finally understand something —
        and I want every student to have that moment, more than once."
      </p>
      <div class="philosophy-grid">
        <div><h4>How students learn</h4><p>Through curiosity, safety, and repeated, low-stakes practice.</p></div>
        <div><h4>Role of curiosity</h4><p>Curiosity is the entry point for every unit I design.</p></div>
        <div><h4>Technology in education</h4><p>A tool for access and engagement, never a replacement for good teaching.</p></div>
        <div><h4>Inclusive education</h4><p>Universal Design for Learning shapes how I plan from day one.</p></div>
        <div><h4>Assessment philosophy</h4><p>Assessment informs instruction — it should never simply sort students.</p></div>
        <div><h4>Growth mindset</h4><p>Mistakes are data, for the student and for me.</p></div>
      </div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     BLOG
     ============================================================ -->
<section class="section page-section" id="blog">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Blog</span>
      <h2>Notes from the classroom and the curriculum table.</h2>
      <p>Short, practical writing on literacy, language learning, and instructional design.</p>
    </div>
    <div class="card-grid">
      <div class="card">
        <span class="tag" style="background:var(--coral);">Literacy</span>
        <h3>How I Teach Reading Comprehension</h3>
        <p>The strategy sequence I return to with every new class, and why it works.</p>
        <div class="meta"><span>6 min read</span><a href="javascript:void(0)">Read →</a></div>
      </div>
      <div class="card">
        <span class="tag" style="background:var(--coral);">Curriculum</span>
        <h3>Designing Better Assessments</h3>
        <p>Moving from "gotcha" tests to assessment that actually informs the next lesson.</p>
        <div class="meta"><span>5 min read</span><a href="javascript:void(0)">Read →</a></div>
      </div>
      <div class="card">
        <span class="tag" style="background:var(--coral);">EdTech</span>
        <h3>Using AI Responsibly in Education</h3>
        <p>Where I let AI tools into my planning process, and where I don't.</p>
        <div class="meta"><span>7 min read</span><a href="javascript:void(0)">Read →</a></div>
      </div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     PROFESSIONAL DEVELOPMENT
     ============================================================ -->
<section class="section page-section" id="pd">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Professional Development</span>
      <h2>Certifications, learning, and involvement.</h2>
    </div>
    <div class="pd-grid">
      <div class="pd-item"><div class="pd-year">2016</div><h4>B.Ed, English &amp; French Education</h4><p>University of the West Indies</p></div>
      <div class="pd-item"><div class="pd-year">2021</div><h4>TEFL Certification</h4><p>120-hour accredited course</p></div>
      <div class="pd-item"><div class="pd-year">2022</div><h4>FLE Certification</h4><p>Français Langue Étrangère</p></div>
      <div class="pd-item"><div class="pd-year">2023</div><h4>Modern Classrooms Project</h4><p>Blended, self-paced instruction certificate</p></div>
      <div class="pd-item"><div class="pd-year">2024</div><h4>Conference Presentation</h4><p>"Designing for Differentiation" — Regional Literacy Conference</p></div>
      <div class="pd-item"><div class="pd-year">Ongoing</div><h4>Professional Membership</h4><p>International Literacy Association</p></div>
    </div>
  </div>
</section>

<div class="wrap"><hr class="ticket-divider"></div>

<!-- ============================================================
     CONTACT
     ============================================================ -->
<section class="section page-section" id="contact">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Contact</span>
      <h2>Let's connect.</h2>
      <p>Tutoring and instructional design consulting all start here.</p>
    </div>

    <div class="contact-grid">
      <form class="contact-form" onsubmit="event.preventDefault(); alert('Thanks for reaching out — I will be in touch soon.');">
        <div>
          <label for="cf-name">Name</label>
          <input id="cf-name" type="text" placeholder="Your full name" required>
        </div>
        <div>
          <label for="cf-email">Email</label>
          <input id="cf-email" type="email" placeholder="you@example.com" required>
        </div>
        <div>
          <label for="cf-reason">I'm interested in</label>
          <select id="cf-reason">
            <option>Private tutoring</option>
            <option>Instructional design consulting</option>
            <option>Something else</option>
          </select>
        </div>
        <div>
          <label for="cf-message">Message</label>
          <textarea id="cf-message" placeholder="Tell me a little about what you need…"></textarea>
        </div>
        <button type="submit" class="btn btn-primary" style="justify-self:start;">Send message</button>
      </form>

      <div>
        <div class="contact-links">
          <a href="mailto:hello@thecuriousclassroom.com">✉ hello@thecuriousclassroom.com</a>
          <a href="javascript:void(0)">in linkedin.com/in/veronae-fh</a>
          <a href="javascript:void(0)">📅 Book a consultation</a>
          <a href="javascript:void(0)">📄 Download CV</a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================
     FOOTER
     ============================================================ -->
<footer>
  <div class="wrap">
    <div class="footer-grid">
      <div>
        <a href="javascript:void(0)" data-target="home" class="brand"><span class="mark">TCC</span>The Curious Classroom</a>
        <p style="color:var(--slate); font-size:0.88rem; margin-top:14px; max-width:34ch;">
          Veronae Findlay — language educator, instructional designer, and
          learning experience designer based in Jamaica, working with
          students and schools nationwide with reach beyond the coast.
        </p>
      </div>
      <div>
        <h5>Explore</h5>
        <ul>
          <li><a href="javascript:void(0)" data-target="about">About</a></li>
          <li><a href="javascript:void(0)" data-target="teaching">Teaching</a></li>
          <li><a href="javascript:void(0)" data-target="curriculum">Curriculum</a></li>
          <li><a href="javascript:void(0)" data-target="library">Resources</a></li>
        </ul>
      </div>
      <div>
        <h5>Work with me</h5>
        <ul>
          <li><a href="javascript:void(0)" data-target="products">Digital Products</a></li>
          <li><a href="javascript:void(0)" data-target="contact">Book Tutoring</a></li>
          <li><a href="javascript:void(0)" data-target="contact">Instructional Design Consulting</a></li>
          <li><a href="javascript:void(0)" data-target="blog">Blog</a></li>
        </ul>
      </div>
      <div>
        <h5>Connect</h5>
        <ul>
          <li><a href="mailto:hello@thecuriousclassroom.com">Email</a></li>
          <li><a href="javascript:void(0)">LinkedIn</a></li>
          <li><a href="javascript:void(0)">Instagram</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 The Curious Classroom. All rights reserved.</span>
    </div>
  </div>
</footer>

<script>
// ---------- tab-based page navigation ----------
const pageSections = document.querySelectorAll('.page-section');
const navLinks = document.querySelectorAll('a[data-target]');

function goToSection(id){
  pageSections.forEach(sec => sec.classList.toggle('active', sec.id === id));
  navLinks.forEach(a => a.classList.toggle('current', a.dataset.target === id));
  window.scrollTo(0,0);
}

navLinks.forEach(a => {
  a.addEventListener('click', (e) => {
    e.preventDefault();
    goToSection(a.dataset.target);
  });
});

// start on Home
goToSection('home');

// ---------- mobile nav toggle ----------
const navToggle = document.getElementById('navToggle');
const primaryNav = document.getElementById('primaryNav');
navToggle.addEventListener('click', () => primaryNav.classList.toggle('open'));
primaryNav.querySelectorAll('a').forEach(a => a.addEventListener('click', () => primaryNav.classList.remove('open')));

// ---------- hero greeting rotator ----------
const greetings = ['Bonjour.', 'Hola.', 'Hello.', 'Welcome.'];
let gi = 0;
const greetEl = document.getElementById('greetingRotator');
setInterval(() => {
  gi = (gi + 1) % greetings.length;
  greetEl.style.opacity = 0;
  setTimeout(() => { greetEl.textContent = greetings[gi]; greetEl.style.opacity = 1; }, 250);
}, 2400);
greetEl.style.transition = 'opacity .25s ease';

// ---------- teaching tabs ----------
const tabBtns = document.querySelectorAll('.tab-btn');
const tabPanels = document.querySelectorAll('.tab-panel');
tabBtns.forEach(btn => {
  btn.addEventListener('click', () => {
    tabBtns.forEach(b => b.classList.remove('active'));
    tabPanels.forEach(p => p.classList.remove('active'));
    btn.classList.add('active');
    document.querySelector(`.tab-panel[data-panel="${btn.dataset.tab}"]`).classList.add('active');
  });
});

// ---------- resource library search + filter ----------
const searchInput = document.getElementById('librarySearch');
const filterChips = document.querySelectorAll('.filter-chip');
const resourceItems = document.querySelectorAll('.resource-item');
const emptyState = document.getElementById('emptyState');
let activeFilter = 'all';

function applyLibraryFilters(){
  const q = searchInput.value.trim().toLowerCase();
  let visibleCount = 0;
  resourceItems.forEach(item => {
    const matchesFilter = activeFilter === 'all' || item.dataset.cat === activeFilter;
    const matchesSearch = item.dataset.title.toLowerCase().includes(q) || item.dataset.cat.toLowerCase().includes(q);
    const show = matchesFilter && matchesSearch;
    item.style.display = show ? '' : 'none';
    if (show) visibleCount++;
  });
  emptyState.classList.toggle('show', visibleCount === 0);
}

searchInput.addEventListener('input', applyLibraryFilters);
filterChips.forEach(chip => {
  chip.addEventListener('click', () => {
    filterChips.forEach(c => c.classList.remove('active'));
    chip.classList.add('active');
    activeFilter = chip.dataset.filter;
    applyLibraryFilters();
  });
});
</script>

</body>
</html>
