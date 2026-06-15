<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LIA VIA – Yoga2go | Gesundheitstraining in Köln, drinnen, draußen &amp; online</title>
<style>
  :root{
    --cream:#F5F8F6;
    --moss:#2F7A6B;
    --terracotta:#3FA89C;
    --ink:#243433;
    --line:#D7E6E2;
    --gold:#7FB8AE;
  }

  *{margin:0;padding:0;box-sizing:border-box;}

  html{scroll-behavior:smooth;}

  body{
    font-family:'Georgia', 'Iowan Old Style', serif;
    background:var(--cream);
    color:var(--ink);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }

  .eyebrow{
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-size:0.75rem;
    letter-spacing:0.28em;
    text-transform:uppercase;
    color:var(--moss);
    font-weight:600;
  }

  /* NAV */
  nav{
    position:sticky;top:0;z-index:50;
    background:rgba(246,241,231,0.9);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
    padding:1rem 6vw;
    display:flex;
    justify-content:space-between;
    align-items:center;
  }
  .logo{
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-weight:700;
    font-size:1.1rem;
    letter-spacing:0.18em;
    text-transform:uppercase;
  }
  .logo span{color:var(--terracotta);}
  nav ul{
    display:flex;
    gap:2rem;
    list-style:none;
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-size:0.85rem;
    letter-spacing:0.04em;
  }
  nav a{
    color:var(--ink);
    text-decoration:none;
    transition:color 0.2s;
  }
  nav a:hover, nav a:focus-visible{color:var(--terracotta);}

  @media (max-width:700px){
    nav ul{display:none;}
  }

  /* HERO */
  .hero{
    padding:6rem 6vw 4rem;
    display:grid;
    grid-template-columns:1.2fr 1fr;
    gap:3rem;
    align-items:center;
    border-bottom:1px solid var(--line);
  }
  .hero h1{
    font-size:clamp(2.4rem, 5vw, 4rem);
    font-weight:400;
    line-height:1.15;
    margin:1rem 0 1.5rem;
  }
  .hero h1 em{
    font-style:italic;
    color:var(--terracotta);
  }
  .hero p.lead{
    font-size:1.15rem;
    max-width:32ch;
    color:#4E6360;
  }
  .hero-cta{
    margin-top:2rem;
    display:flex;
    gap:1rem;
    flex-wrap:wrap;
  }
  .btn{
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-size:0.85rem;
    letter-spacing:0.08em;
    text-transform:uppercase;
    padding:0.9rem 1.8rem;
    border-radius:999px;
    text-decoration:none;
    border:1px solid var(--ink);
    transition:all 0.2s ease;
    display:inline-block;
  }
  .btn-primary{
    background:var(--moss);
    color:var(--cream);
    border-color:var(--moss);
  }
  .btn-primary:hover{background:#4A5740;}
  .btn-outline{
    background:transparent;
    color:var(--ink);
  }
  .btn-outline:hover{background:var(--ink);color:var(--cream);}

  /* hero visual: root/path motif */
  .hero-visual{
    aspect-ratio:1/1;
    border-radius:50%;
    background:linear-gradient(135deg, #E1F0EB, #C9E4DC);
    position:relative;
    display:flex;
    align-items:center;
    justify-content:center;
    overflow:hidden;
  }
  .hero-visual svg{width:80%;height:80%;}

  @media (max-width:850px){
    .hero{grid-template-columns:1fr;padding-top:3rem;}
    .hero-visual{max-width:280px;margin:0 auto;}
  }

  /* SECTION GENERAL */
  section{padding:5rem 6vw;}
  section h2{
    font-size:clamp(1.8rem,3.5vw,2.6rem);
    font-weight:400;
    margin:0.6rem 0 2rem;
    max-width:22ch;
  }
  .section-head{margin-bottom:2.5rem;}

  /* INTRO / WHY */
  .intro{
    background:#EEF6F3;
    border-bottom:1px solid var(--line);
  }
  .intro-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:2.5rem;
    margin-top:2rem;
  }
  .intro-card{
    border-top:2px solid var(--gold);
    padding-top:1.2rem;
  }
  .intro-card h3{
    font-size:1.2rem;
    margin-bottom:0.6rem;
    font-weight:600;
  }
  .intro-card p{font-size:0.96rem;color:#4E6360;}

  @media (max-width:800px){
    .intro-grid{grid-template-columns:1fr;gap:2rem;}
  }

  /* FORMATS */
  .formats-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:1.5rem;
  }
  .format-card{
    background:#fff;
    border:1px solid var(--line);
    border-radius:18px;
    padding:2rem;
    display:flex;
    flex-direction:column;
    gap:0.8rem;
  }
  .format-card .tag{
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-size:0.7rem;
    letter-spacing:0.2em;
    text-transform:uppercase;
    color:var(--terracotta);
  }
  .format-card h3{font-size:1.4rem;font-weight:600;}
  .format-card .price{
    font-size:2.2rem;
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-weight:700;
    margin-top:0.5rem;
  }
  .format-card .price small{
    font-size:1rem;
    font-weight:400;
    font-family:'Georgia',serif;
    color:#7A938E;
  }
  .format-card p.desc{font-size:0.95rem;color:#4E6360;flex-grow:1;}
  .format-card .note{
    font-size:0.82rem;
    color:#7A938E;
    font-style:italic;
  }

  @media (max-width:850px){
    .formats-grid{grid-template-columns:1fr;}
  }

  /* WHO IT'S FOR */
  .for-whom{
    background:var(--moss);
    color:var(--cream);
  }
  .for-whom .eyebrow{color:var(--gold);}
  .for-whom h2{color:var(--cream);}
  .who-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:1.2rem 2.5rem;
    margin-top:1rem;
  }
  .who-item{
    display:flex;
    gap:0.9rem;
    align-items:flex-start;
    padding:0.8rem 0;
    border-bottom:1px solid rgba(246,241,231,0.18);
  }
  .who-item span.mark{
    font-family:'Georgia',serif;
    font-style:italic;
    color:var(--gold);
    font-size:1.3rem;
    line-height:1;
  }
  .who-item p{font-size:0.98rem;}

  @media (max-width:800px){
    .who-grid{grid-template-columns:1fr;}
  }

  /* ABOUT */
  .about{
    display:grid;
    grid-template-columns:0.9fr 1.4fr;
    gap:3rem;
    align-items:start;
  }
  .about-portrait{
    aspect-ratio:3/4;
    background:#E1F0EB;
    border-radius:18px;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#8FB3AC;
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-size:0.85rem;
    letter-spacing:0.1em;
    text-transform:uppercase;
    text-align:center;
    padding:1rem;
  }
  .about-text p{margin-bottom:1.1rem;font-size:1.02rem;color:#4E6360;}
  .about-text p.signature{
    font-style:italic;
    color:var(--terracotta);
    margin-top:1.5rem;
  }
  .book-pill{
    display:inline-flex;
    align-items:center;
    gap:0.6rem;
    margin-top:1rem;
    padding:0.7rem 1.3rem;
    border:1px solid var(--line);
    border-radius:999px;
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-size:0.85rem;
    text-decoration:none;
    color:var(--ink);
    transition:border-color 0.2s, color 0.2s;
  }
  .book-pill:hover{border-color:var(--terracotta);color:var(--terracotta);}

  @media (max-width:850px){
    .about{grid-template-columns:1fr;}
    .about-portrait{max-width:280px;margin:0 auto;}
  }

  /* CTA / BOOKING */
  .cta{
    background:#EEF6F3;
    border-top:1px solid var(--line);
    border-bottom:1px solid var(--line);
    text-align:center;
  }
  .cta h2{margin:0.6rem auto 1rem;max-width:24ch;}
  .cta p.lead{max-width:42ch;margin:0 auto 2rem;color:#4E6360;}
  .cta-buttons{
    display:flex;
    gap:1rem;
    justify-content:center;
    flex-wrap:wrap;
  }

  .price-note{
    margin-top:2.5rem;
    font-size:0.85rem;
    color:#7A938E;
    font-family:'Helvetica Neue', Arial, sans-serif;
  }

  /* FOOTER */
  footer{
    padding:3rem 6vw;
    display:flex;
    justify-content:space-between;
    align-items:center;
    flex-wrap:wrap;
    gap:1.5rem;
    font-family:'Helvetica Neue', Arial, sans-serif;
    font-size:0.85rem;
    color:#7A938E;
  }
  footer .footer-links{
    display:flex;
    gap:1.5rem;
  }
  footer a{color:#7A938E;text-decoration:none;}
  footer a:hover{color:var(--terracotta);}

  /* Focus visibility */
  a:focus-visible, .btn:focus-visible{
    outline:2px solid var(--terracotta);
    outline-offset:2px;
  }

  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    *{transition:none !important;}
  }
</style>
</head>
<body>

<nav>
  <div class="logo">LIA <span>VIA</span></div>
  <ul>
    <li><a href="#angebote">Angebote</a></li>
    <li><a href="#workshops">Workshops</a></li>
    <li><a href="#fuer-wen">Für wen</a></li>
    <li><a href="#ueber-mich">Über mich</a></li>
    <li><a href="#buchen">Buchen</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div>
    <p class="eyebrow">Yoga2go · Köln &amp; Online</p>
    <h1>Wieder in <em>Bewegung</em> kommen – ganz ohne Druck.</h1>
    <p class="lead">Sanftes Gesundheitstraining für alle, die gesund bleiben, Steifigkeit loswerden und wieder in Bewegung kommen wollen. Yoga für Anfänger, draußen, drinnen oder online.</p>
    <div class="hero-cta">
      <a href="#angebote" class="btn btn-primary">Angebote ansehen</a>
      <a href="#buchen" class="btn btn-outline">Kontakt &amp; Buchung</a>
    </div>
  </div>
  <div class="hero-visual">
    <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAgAAAAIACAYAAAD0eNT6AAAABmJLR0QA/wD/AP+gvaeTAAAgAElEQVR4nOzdeXgV5dk/8O/9nHOysYR9VXEJagWSQFAWrYJareBaX/r+WltrWwmSQOtWhcS205bNpVXLIkTtoq3v+0rrDta6gFZZ1BjCYlXibtkChADZzjL3748TF0Igc5IzZ8v3c11cvTp5ZuY2OTNzn2ee534AIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIi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" alt="LiaVia Logo – Kintsugi-Schale" style="width:70%;height:auto;">
  </div>
</section>

<!-- INTRO / WHY -->
<section class="intro">
  <div class="section-head">
    <p class="eyebrow">Warum Yoga2go</p>
    <h2>Bewegung, die zu deinem Körper passt – nicht umgekehrt.</h2>
  </div>
  <div class="intro-grid">
    <div class="intro-card">
      <h3>Sanfter Einstieg</h3>
      <p>Kein Vorwissen nötig. Jede Übung lässt sich an deine Tagesform und Beweglichkeit anpassen – egal ob du zum ersten Mal eine Matte ausrollst oder lange pausiert hast.</p>
    </div>
    <div class="intro-card">
      <h3>Für den Alltag gedacht</h3>
      <p>Health Yoga, leichte Tanzbewegung zu Musik, Atemtechniken, Shaking und progressive Muskelentspannung – Methoden, die Beweglichkeit, Haltung und Gelassenheit fördern.</p>
    </div>
    <div class="intro-card">
      <h3>Drinnen, draußen, online</h3>
      <p>Im Park bei gutem Wetter, im warmen Raum oder bequem von zu Hause online – du entscheidest, was gerade passt.</p>
    </div>
  </div>
</section>

<!-- FORMATS / PRICING -->
<section id="angebote">
  <div class="section-head">
    <p class="eyebrow">Angebote &amp; Preise</p>
    <h2>Gruppentraining oder 1:1 – du entscheidest.</h2>
  </div>

  <h3 style="font-family:'Helvetica Neue', Arial, sans-serif; font-size:1rem; letter-spacing:0.08em; text-transform:uppercase; color:var(--moss); margin-bottom:1rem;">Gruppentraining</h3>
  <div class="formats-grid">
    <div class="format-card">
      <span class="tag">Outdoor</span>
      <h3>Yoga im Freien</h3>
      <p class="desc">Gemeinsames Training an der frischen Luft – wetterabhängig, in Parks oder Grünanlagen in Köln. Begrenzt auf 8–10 Personen. Ort &amp; Termin werden rechtzeitig mitgeteilt.</p>
      <p class="price">15&nbsp;€ <small>/ Person</small></p>
      <p class="note">Bitte Matte &amp; wettergerechte Kleidung mitbringen.</p>
    </div>
    <div class="format-card">
      <span class="tag">Indoor</span>
      <h3>Yoga im Raum</h3>
      <p class="desc">Geschützte Atmosphäre, gleichmäßige Temperatur, feste Unterlage – ideal für Anfänger und alle, die mehr Ruhe und Kontinuität suchen. Begrenzt auf 8–10 Personen.</p>
      <p class="price">18&nbsp;€ <small>/ Person</small></p>
      <p class="note">Matten &amp; Hilfsmittel vor Ort vorhanden.</p>
    </div>
    <div class="format-card">
      <span class="tag">Online</span>
      <h3>Live online</h3>
      <p class="desc">Kleine Gruppe – von überall aus, mit persönlicher Anleitung und Raum für deine Fragen.</p>
      <p class="price">12,50&nbsp;€ <small>/ Person</small></p>
      <p class="note">Den Link für die Online-Stunde erhältst du nach der Buchung.</p>
    </div>
  </div>

  <h3 style="font-family:'Helvetica Neue', Arial, sans-serif; font-size:1rem; letter-spacing:0.08em; text-transform:uppercase; color:var(--moss); margin:3rem 0 1rem;">Personaltraining (1:1)</h3>
  <div class="formats-grid">
    <div class="format-card">
      <span class="tag">Outdoor / bei dir</span>
      <h3>1:1 im Freien oder bei dir</h3>
      <p class="desc">Individuelles Training an der frischen Luft oder bei dir vor Ort – ganz auf dich abgestimmt, Ort nach Absprache.</p>
      <p class="price">55&nbsp;€ <small>/ Einheit</small></p>
      <p class="note">Bitte Matte &amp; wettergerechte Kleidung mitbringen.</p>
    </div>
    <div class="format-card">
      <span class="tag">Indoor</span>
      <h3>1:1 im Raum</h3>
      <p class="desc">Geschützte, ruhige Atmosphäre für deine persönliche Einheit – ganz in deinem Tempo.</p>
      <p class="price">35&nbsp;€ <small>/ Einheit</small></p>
      <p class="note">Matten &amp; Hilfsmittel vor Ort vorhanden.</p>
    </div>
    <div class="format-card">
      <span class="tag">Online</span>
      <h3>1:1 online</h3>
      <p class="desc">Persönliches Coaching von überall aus – mit voller Aufmerksamkeit für deine Anliegen.</p>
      <p class="price">25&nbsp;€ <small>/ Einheit</small></p>
      <p class="note">Den Link für die Online-Stunde erhältst du nach der Buchung.</p>
    </div>
  </div>
</section>

<!-- WORKSHOPS & EVENTS -->
<section id="workshops">
  <div class="section-head">
    <p class="eyebrow">Workshops &amp; Events</p>
    <h2>Besondere Termine zum Reinschnuppern.</h2>
  </div>
  <div class="formats-grid">
    <div class="format-card">
      <span class="tag">PLATZHALTER</span>
      <h3>Workshop-Thema folgt</h3>
      <p class="desc">Hier erscheinen demnächst Infos zu kommenden Workshops und Events – Datum, Ort und Thema werden noch ergänzt.</p>
      <p class="note" style="color:var(--terracotta);">Datum &amp; Ort: noch offen</p>
    </div>
  </div>
</section>

<!-- FOR WHOM -->
<section id="fuer-wen" class="for-whom">
  <div class="section-head">
    <p class="eyebrow">Für wen ist Yoga2go</p>
    <h2>Für alle, die gesund bleiben und wieder in Bewegung kommen wollen.</h2>
  </div>
  <div class="who-grid">
    <div class="who-item"><span class="mark">·</span><p>Du willst Steifigkeit loswerden und beweglicher werden</p></div>
    <div class="who-item"><span class="mark">·</span><p>Du möchtest gesund bleiben oder wieder in Bewegung kommen</p></div>
    <div class="who-item"><span class="mark">·</span><p>Verspannungen in Rücken, Schultern oder Hüfte</p></div>
    <div class="who-item"><span class="mark">·</span><p>Vorbeugung &amp; sanfte Begleitung bei Osteoporose</p></div>
    <div class="who-item"><span class="mark">·</span><p>Wiedereinstieg in Bewegung nach längerer Pause</p></div>
    <div class="who-item"><span class="mark">·</span><p>Yoga für Anfänger – kein Vorwissen nötig, alle Levels willkommen</p></div>
  </div>
</section>

<!-- ABOUT -->
<section id="ueber-mich" class="about">
  <div class="about-portrait">
    <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAgAAAAIACAYAAAD0eNT6AAAABmJLR0QA/wD/AP+gvaeTAAAgAElEQVR4nOzdeXgV5dk/8O/9nHOysYR9VXEJagWSQFAWrYJareBaX/r+WltrWwmSQOtWhcS205bNpVXLIkTtoq3v+0rrDta6gFZZ1BjCYlXibtkChADZzjL3748TF0Igc5IzZ8v3c11cvTp5ZuY2OTNzn2ee534AIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiIiSmIS7wCIOpuCwkIfBiG7KZieLcFgDzGmh6hmQ8QrIj1sWz0i6A6FD4KuqkgXQRYEmVBkqKALbE0TkW4i4rVVswRIb+VU3QB4W9neA4df+wpgXyttgwAOtNyoQJMRqVfVoKoegBG/KOogaISiQRX1ImiC4iAEAVXsN0ZCAGrUtkMqUqu2vU+93n3BkL1vQHrf2tWWFYzwV0lEHcAEgKidCm4tzA74PANMyNMHQF+F3V8hvcVoNlR6IPygzQY0WyHZAukBaDaArPhGnrDqANQqUCvQWkBqAdQC2AfRfWpLrUD3CMxOANUKrfbagZ3lt5fVxjdsouTEBIDoK0bMmt5TjA42kCGA9IWafgrtD4O+APoC2h8q/QD0Qevfuin2mgDshuguUexQkd2wUS2QnRB7F1R22RL6xKRlfLbBuqe1Xg6iTokJAHUa4264IfNgeuNAr9d7YsgODRLIQAAnQjBIIANV9SSEv7VT6moEsA3A9ub//UAh241gWygU+sBre7ZX3LFoW3xDJIoNJgCUOizLFDTUHBPwhXKMIge2PVQFOYDJAXQIwu/EidpyAIqPIKhSoMqIVNmCKl/AU1We2fMzWJYd7wCJooEJACWdkaXFQyBmqK2aA9UcBXIEGArgJLBbntzVBOB9BbYKUAWRKiNSBbW3Vsxd/HG8gyOKBBMASlj51vU9NOAfLjCnqa3DFHqaiOQj/P6dKNHsF5GtCn0bii0q+nbIjze23LlkR7wDI2oNEwCKu+OtazJ6BroOt1VzoRgGwQhAhgM6MN6xEXWcbAd0MxSbANlsDDYd2C+bqhYubIp3ZNS5MQGgmBt5y4xB6sOZautZEBQAKACQEe+4iGIoCOA9CMoF8qoafa3S0/ffHF9AscQEgFxVUFI4MCDe0UZNgYoWqGKcAL3jHRdRAjoAYCMU5SpaDmP+tXHOog/jHRSlLiYAFFXDS4uONYqJEDlXFBMADIl3TAlqH4BaAWoVWguRWigaEH4IBBWoFZEQVPepSsgY7FcbATE4aNto8nikXkPaENJQI3wePwKhupYnUJNWJ7bf33L7poz+tYd907QsM6JxZ3bLtnZI0o1HDy9c5PN0QSCU5hFPhngkMxTSLGOQrja6ioHPttFdRD0AeipgBMhGuCpht3BFQ80WSLaGt2eD0y+P5GMAqxS6yhas2jx3yafxDohSBxMA6pBhPysa4EnDRMBMFNWJAHLiHVMMtVqARgW7jWgtgFq1pVZham0J1vrE1KrPV8tiNK3Lt67vIYFAdkDtbKPebJhQD1GTLdBsW5EtQO8vCjIpBgDoi05XkEm3ArJKgVWhgK7mAEPqCCYAFJHjrWsyspu6nA/BNwFMBHBavGOKsiCAHQA+AfAZgJ2AVkOxiyVoE1NrJZkh6AdIXwD9ARwD4DgAA9D62gjJ7G0Aq6D4R2163QsfWX9qjHdAlDyYAFCbRsya3tPj8Zyv0EuguAxA93jH1AE1IvKBQrdDP68Ep9s9xrMtGAx+0Duj/ydclCZ1jZg1vSeAE8UjgwzMQFU9EYJBautAETkR4UQhWZOEBgheFMjTti/4xEZr6a54B0SJjQkAtarg1p8eF/SELoPq5RCcjeS5KTYp8IEBtqp+XskNVbaRql7ePp/y4U5HM8GyvHsadx5nIDniQY6qyQE0B+FCUycgeV43BAC8AtEnQsCTHDtArWECQF8osAr7BPxpVwn0agCj4h3PUYQA/QDAFml+yKtIlUdQVeHr+ymnUpEbpkyZ4tl6Uu9jxevLaVGFchiAEwGYeMd4BKpAOQQP+2389Z35i/fEOyBKDEwAOjvLMiODe8611b4aiv8CkBnvkFqoAfA2FOViZIvCflubsio23nXXYaPeieJlmGWleUPVQ8WW06AYpqIFUJyGcK9BIt1n/RD8UyAP9fD1eZw9Yp1bIn0wKYZGzSrKCRpcI5BrAAyOdzwA/AA2AKgQYJOovdmfnrFpi3X33ngHRtRew6wbevmCgVzYOkyBEQj3rOUBSItzaADwGQR/Con50+Y5C9+PdzAUe0wAOhfJn118kQpuBHAu4vf3VwBbAX0dMK+r6uv1B80GlkalziBn5sz0rK52voicAdhnAHIGwmMM4nY9quqLUPx244IlzyF8fVInwASgEygoLPQF+/i+D8WNEAyLQwi7IVgHDT/wbTv0+qYF99XEIQ6ihDRi1vSexng+TwhOBzAOcVn0SjaL6l090vv+la8HUh8TgFRmWSY/sPtKVXsuIENjeOaDqrpORF6wbfuFTRn9KzgwjygyI2ZNP9Hj8ZyvqucDOA9Arxie/mMRmTf0vZ0PLl++PBTD81IMMQFIUfmziyep4E7EplDPQYH+C5BVIrIq572dFbxpEEVPeAZC31EQM1GNToTiLABdY3Dqt23IzZvmLXo2BueiGGMCkGJGzSrKCXnkbigudvlUVaL6hA3PU73Se69ldyFR7BQUFvr8fX3jjOJSAS5X4CSXT/l0yJgbOFgwtTABSBWWZXKbdt8oor+BO0vrqgLlBvKEevSJyt8s3uLCOYioHUb8fMYIE9TLVHCZhJfXduPe3gjobZVp/e7mK73UwAQgBeTPuu54GM+fFTg7yoe2oVgtRv9uBzxPbbxj4WdRPj4RRdnw0qJjvSqXKnAlgHMQ5QJFCnnZI/qDirmLP47mcSn2mAAkuRGlxWcbxd8QXhktWj4D8Ffbtss2Lbjvgygel4hiKPeWmceI174KQCHC1QqjZa8C3944b/GLUTwmxRgTgCSWV1o0Ayp3Izp1+hugeEwFf9yY1ncVu/iIUohlmXx/9XlQ+aGKXoHovCYMiuhPN8xdsiQKx6I4YAKQpPJKim8FsKCjxxHgfRW9R3xpf+E69USpb8Ss6T3FY74vip8iCr0CAtyyYd7iO6MQGsUYE4AklFdSdBMgd3XwMG+o6h0b0/s9xm/7RJ3PlClTPO8N7XeliNyiqgUdO5reWDlvyd3RiYxihQlAksmbXXwxBE+hvX87xRYx8qsNcxf9DSz5SUQARt4283zbtm9H+1cBVVH51ob5i56IZlzkLiYASWTErOknGmPeBNAz8r1lO1RvrZy/+C/gg5+IWrIsk99U/X01WADFgHYcYa/YoYINC5Z+FO3QyB2Jun41tcIYU4bIH/42FL9rDNafUjl/8cPgw5+IWmNZ9ob5i/+c4TOnqOIeAJG+GuylxrPUjdDIHewBSBJ5JTMuBPQfEe72oar5wcb5C//lSlBElLJGzp5+ji3mTwCOj2Q/Y8w3KuYsfMGVoCiq2AOQJBQ6J6L2qi8E09JG8+FPRO1RMf++l5sUo6F4KZL9bNue61ZMFF3sAUgCI2bPONWI/jvecRAROSHGc/KGOb/fGu846OjYA5AEBPqteMdAROSUhoJXxjsGals0KsiRy0QwJd4xOOEVxRU9azCu60EAwNqDXfHUvh5osplnJpLW/k6P1/REUNkhSFEiMgVRKFRG7mICkBxOjncATnyrZw3O7b7/i/9/Xvf9GJbZgAeq++Ezvy9ucflEMTjNjx6eELI9IXT1hNDV2PBKeEJECMC+oBd7g15sC/iwze+DncJvx1r7OwmAR/f2il9QlGpOiXcA1DYmAElAFZmSBM+jMV3rDts2wBfArQO3YcW+Hnhhf3fXv2WKAIO8fpyS0Yjj0ptwXJofA9KCMBHMfgyo4CN/OjbWZ6KyLgu7gvFLXtzQ2t9pTNc6JgAUNarIincM1DYmAElAJLm/jvpEcXnPGoztehCP1/TExoYsaBSrEfTxBnFqRgNOyWzEKRmN6O4Jdeh4PlEMTW/E0PRGXNmzBh82pWPV/u54qz4rJbrJu5jDfz+tbSNqr2S/Z3UWTACSgCo0GS6o9Qe7HNK13NIAXwDT++3CfwJpWL2/G96s64KGdowP6OkNIie9CadkNOCUjEb09QU7EnabTkhvwgl9q3Fl0INnantgzcGuCKVAIkDknmim+OQWJgBJQMIVuTzxjqMtj9X0RLoozux24KjtBvv8uKr3Hny7116835SBdxsz8FlTGqqDXhwIeRBQgVcUaaLo4w2ity+AXp4ghqT7cUJ6E7I7+A2/vbK9IVzVew++kb0fj+7thc31mXGJgyjRiUZcRZDigAlAMhA0AYn/Ti2ogof39MbbjZn4Xu/dyDRHvwf4RHFqRgNOzWiIUYTR0c8bwIx+O/FWfRc8srs3DnKWA9EhVKQp3jFQ25gAJIcaJEEC8Lnyuix84h+E/9drD4ZlJsbDvSboxWcBH2qDHuwPeVFnG/ibu/HTRdHLF8QArx9D0gOO34ePyqrDSYMb8WB1X7zXmOFm+ETJpibeAVDbmAAkA8U+CAZHuM9qb3pgSrlVttulqNr0AoC190/+FhR3ATghhqcOAFgPlRchofUivrcmFT250+nOa5ddMkqNfbkovo826qBne0K4ccCOIIDbxk5dcYdIEiy2VDa51Rgr5y3mwAY6RIFV2CfgT/ubQM+JbE9hApAEeMEngbySorWAjI10PwU+gZEfbpyzKKJa3tG2yprgzRjY5SqBzFZRN+YHK4CNgL4oYl5s8Ge+MrF4+cEOH9SyzLpBb1wMoBTAGQ52ebSm0b560k+eTejuz7VHSADGFa7g/YC+kFtSfJ4AfwRwbKT7KrB247zF410Ii6KIF3wSyJ1d9LyInN/O3RXAIm8o8PPy28tqoxlXxIEoZM2ySV/3GPmBApcDaO/E8yCASlVZJ2K/EvDqqrN/9Gx1FEM9hCpk3QOTr3DYk7G60ee7YuIPn9jnVjwdxQSAjibfur6H+gNzABSh/c+I5yvnLb4gimGRC/gKIAmIoCPfZgXAzKDH9+38kqJZG9L6PQTLissI3XD3+MpXALyiljV13cDyfCB0DkSGAfiaKgaIoCeADACNgAQA/QyKjyD4GMCHRrDBY5vy0dOero9t3Cseq3zogufqGr1zBTITR15HY0JGIPDK64snXXBG8codsYqRqMMsy+Q17f6BNgUWQNAv0t0Vh2QLHe6BI/cx408CeaXFDyH8Pjoa3hYRa8PcRX8DkuB9dQJaU3bJOSL2/0Ix4EhtROVdE7QnJGISwB4AakFyS4suFuBXUBkZlQNCHtowb9EPonEscg97AJKAKA5G8Ul9mqo+mldaVKHAnb18/Zavtix3K+mkmPGFT7+87v6LTld4lgPa6tgMFT0l5MNz6xddce6YGY/viXWMRG0pKCz0hfqkTVHRW6DIi+axbfYAJAVOYE4CKnr0yjrtO+hIUXmkxl9dlVdafOOps4t7R/0cKWzs1Gc/04OZ5wJ4/MitJNdO8//z1Qcv7RazwIjaUGAV9skrKbop0MdXpdC/RvvhDwAiNhOAJMAEIAmoipsDyoZA8dt0wX/ySoofzZ1V9E1YFj8XDoy/cXnDpz2ypgBYcpRmozx26NFV1gT2tlHcTJkyxTOiZMZF+SXFy4N+338AuUuA41w7oc06AMmAN6UkYFR3q/vLAaYDmCJGpuT5q7ehpPhhj60PvLVgSZXbJ05m3/728hCA4rVlkw8AuLXVRopvZgzqshTAtbGMjWh4adGxHpXvvgdcZ6DHR+tVYosBf4f/XCRu9UfIOSYASUCBWL9DHgTg1pCRW3JLZrwC0cc8wJMVcxd/HOM4ksbYqStmr7t/chcAM47Q5Mdryi5+f3zhM/NjGRd1PiNLi4eEgMuM4kpVfB0uDPZu64AiMb9nUTswAUgCBrrHdnANC/CxAv0ARGuVGhHoOVCcYwP35pUWVajiSQM8uWHekg1ROkdKEIGqrvjJuvsnZwL4cattoHPWLJ1UMf66lf+IcXiU4vJLivJt4DIRXGYrRgpcmeLTAMEuKIa01VBtwx6AJMAEIAnYXrMbDsrTK9SvxgwT2/4dIJdHPRCVkQKMVMDKKyn+SKBPKvBkMK3fa1ssyx/18yUZEeijj2ZNO3ZffV8Al7bSxIiRlWvKJr/ohbn+jMKnt8Q6RkoNOTNnpmdl65kS0ssguFSB4wVwc2Lv42KHboTxvODkFJ7Y91pSO3DebxIY9rOiAV6fbHfQtLZy3uIeAJBXMuNCAHcBOtzd6AAA9QBeg+pLClnVK71veWeeWvjqg5d28wTtlyF6tDnVjWrknPHXPvN6zAJrxjoAyWeCZXn3BnaOhpqJAkwEcCZiskCYbIZt31S5YMk/ASCvpLgWQPe29grBO2DzvHsdr79B8cELPglMsCxvjb+6EYCnrbbqz+y68a676gAAlmXyA7uvVNXfAHCjBv+R1KnqWhF5wbbtFzZl9K+IV/XBeHn1wUsHmVDoTQEGHrGR4oVx01Z8I4ZhAWACkCxGzJp+osfjOV9VzwdwPoCeMTz9hyKyYOh7Ox9cvnx5CAByb765i6Q1OJneFzp56670z/ejxMULPknklRTvANC/rXYhY3I2z1n4/le3TbAsb01T9XdgcJMbc37bosAeEayFjTdU9fVQRvrrW6y798Y6jlhb+8BFZ8KWV498mWlgXOHKtJgGBSYAiejU2cW901RPF5EzYHC6KsYJEPvaHKIVouauoVt3/l/LB/ioWUU5ISNbHRxke+W8RYPcCpGih2MAksd2OEgAPBoaCOCQBKC5O/5hAA/nlxR/Q4GbAHwDMaoDIUBvKC6G4GIRgdfvR15JcZUCrwPyuhH7jcz69Iq1d9/dEIt4YmXctc++trZschPCUyxbIb51ZZN/NbZwxS9jGlg7rF90Re9ghn+gBKW/GBWBZttAk9rYD4P9YkKfjL/2uZRP6qJh3A03ZDZkNY0E5AzYcoaKng4gB59P9dWYfzOzBfqcDfntxrlLXgSA1kb4BsUzUOCkI0+dvK6kBMAEIEmoYJso8ttqJzBH7nIGsGHe4ucBPJ8/67rjYbzX2NAfuloQ5MhyBMgB9LuqgvpMfyCvpHiTAG/ZkM2AbkZaaNNGa+muOMQWNQKsVuDCI/1cgV+sLZvcbezUFTeFFx2Kr1V/nJCR1ZQ1XD0ySoH8cG14zbXhzzI2ABMOUSEQAPJ5Cml7sfb+yXugeFcUr9swL3sC3n919jLIudZ1/eD3jDCCEVAMU9GCevWPgEr43itx/ZN/pNA/eUT+VDF3SZtTfEXso95bvtKSCUCSYAKQJAS63cn3Ahvq6CLdsGDpRwAsWNav8wK7xkPl+wC+h5gMLGqVD8AoBUZ98Rz0e5BXUlwD4G0AWxTytohd3hhorHz3jj9EvzyyGwSlUJyNo0/NvGFd2eS+a36XVTj+xuVx6wVZd//klzWAcbaB78tUJIIHlKI3gPEqGC+wr7fT/Pbaskn/EpFHbAn+LZV7CIZZVpo3VD1UQ1ogkNMgGAaVAvjD16N+/mvUuL9laQLwlIo+fMp71SsjeU+vkIFOclRhD0DSYAKQNJxl1QJxmKU3syy7EngVwKvDrBtmewNN34XK1QBGIzHGiPREeMTzmQIFVJDhzdS8kuKPVPBvo7pVBVUaQpUXqOqe0e+jRJqBMHbqivI1yy4ZJQjdAeAiiLR+zQm+J13rcteXTZoypnDle7GNMkzDiUo0GUDOUcU5ot6F68om/W/IyJ1nXrtic5TPExMFhYU+7eUdEgRyxIMc2DJUDXJE8TX4q48HIIIvu/ETaLFNBfC6AA+HbPuRTQvuqwGAjREeRAQDnPwnqSDhVsCk1iXCDZ4cyC8tKlKVxW21U+CRjfMWX9XR8+XeMvMY4wtdqiqXA5iA8Df0ZBAA8DEEVbClSo1uNTaqFKiqO2g+rlq4sClegb364KWDPKHQqwBOOEqzOoXMze6R+dth314etdoK6++/5ATbDl0CI5dCcV60jtsOqsBKGPvn4699tiKOcbQqZ+bM9C5d7SEC5NgiQ0WRA6M5UOQAOB7J86XJD5HVAB4Hgk9Xzl36n44eMLek+K8CfLetdiJavGHukqOtj0EJgglAksgtLbpEVJ5y0PS1ynmLz4rquW++uQvS688VyBQoLgWQHc3jx1gNgO2quk1EPhDIdgi2icgHwWDwg7S9oU/Ly8oCbp18zX0XD4ZHnxNgWBtN31fVO1HX5aH2vBZY9ccJGZn+bmer2N8UlUkqGstpoE7Yqngg6LNvO/tHz1bH6qQjZk3vCeBEj8dzoq0YJOFXZiciXP56IMIP+WRdDKsegpdUdblJS3tqg3VPVBcRyyspfg3A+DYbKi6pnL/4mWiem9zBBCBJDC+ZnuuBqXTQ9LPKeYuPdSuOnJkz07O6hCaKyEUQORfQYUitz5ENYAegnwDyH6hsV7F3G0G12tih8FQrtDoArX5n/uJ2DXBbv+iK3naafyWAMxw0r1HIMwa6EraUj9kx+n1pUVNh1R8nZGQ2ZZ5oezyjRXU0gAIAIxG9ktAAUC8qn6rYOwDxi2CfKroo0E2APgBOAhDxlEYB9inklnGFz9zf3sBOnV3cO8uj/YIhTx9BqK8YDLAVfUVNH4gOBHQwIMcBGIDkfbi3RqHYLKIvKcyzwbQ+q9ysyJlXUvwfhBOlo7I9krvpN4s2uRUHRU8q3bhT2hhrZvdGv13roKkdTOubGavSvLnWdf3E75kA6ERAzgVwcizO67YuJoTRXeoBAG/WZaHObrUGUwCQ3QKtVmAnFLsUqBbRvSpSC9V9RqQWIrUalFobwVoANZsy+te+ObA8Iyih+xRydYSh+QHsVkUjAIigG4C+HfhPbYXsUugbAqmAaIXXgw2n/2jFB0fb49FHp3iO2d90grGD4xRyDsIzH45xeka19ZnVe9Nv+p/9A4IG3mzxajZC6AFotm2QLarZAvRWlT4K7W9E+imkL6B90Y5ueYd/30T0LqCrRMxLYsvqivkLY9J7Msyy0rz+6gY4SKAy0kz2emvh/hiERR3EBCCJ5JUU74WDamCtFQOKlbzS6wbD9pwLg4lQTES4SzWpdDE2SgdtQy9veCzh3qAXc7cNjPZD4gCA2vO61Zoreu0b4BWN+zfT+pDnV/8JeFbdt7fXpoONaQoAaZrWzS/+Qx6w4oVPg+gKAF5BV3i8PjsU6i7GeGDbPRQwXmN6ju+6/6TRXepOPym9cZhH2n5IH7A9+HN1b2xucHciShcTQumg7S3+voNQZ8f9T9CaDyFYDRurTEherLhj0bZ4BJF/20+Gqh1yMjh1b+W8xbEvYETtkiwDWijsYzhIAAx0CFoUA4qV5sFGDzf/Q751fQ8JhkarrWepaAEUYxHuMk5YE7vv/+LhAAC9vEGM7lKPlw90i+ZpugHo9uKBbGxs7IL/7rUXwzPro3n8iN346bG/BPBLADDNz8IggjAtv/TZX87/twHAtj9fDhGfF7MJquKVA93wyoFu6GZCmNj9ACZ2349Mc+RCMt1MCMX9duGxfT3xfK17w0xGd6k/7O87sft+PLOvh2vndGg/gE1QlIuRVwN++19b7lySECPqBTrE4ZyGj1wNhKKKCUASUeBjgYNiQLYeH4NwHGkeiPRC8z8AwMhbZgwK+ewCUTkTwFkARiG676vbzSOKr3eNbYmB6oAXi3b2Q15WPS7psQ/HpLnz9uYzvw9vN2Thgmwnb5Ki54DtwVP7euCl/d1xSc8anN31wBdF71oSAa7sWYPBvgD+uqc3AjGaN//1rgfwbG02QrGbpx8AsBXAqwp9TTxSXunp++9EXTMjZNvHO/zNtFlQiBIHE4AkYqAfqYO3Ngo9MQbhtFtzN+Y2AE8D4fnVwV7pwyH2cBgdDmJ2fugAACAASURBVEguFMMAuDaY8UjyMuuR7T20NkpIBRvq3a+PVFmfhcr6LJya0YiJ3ffjtMwG+DpQKa7O9uDdxgy8XZ+BLY2ZqAmGL/dYJwCfO2gb/M+e3vjXge74fp/dGJJ25BmZY7seRD9fAAt39kdDlLvmN9Rn4du99sLzld9ttjeEvMx6vFXfJarnavapQDerYBNs2Qw1m717mza7Odsk2ozgBHVSA0CZACQTJgBJxIb50EklLgNJtClfR9V8I6xo/veFglsLs/3iyREjw0SlQKGnCSQXgn5uxTKx++FjlzbUZ6E2FLtBYu80ZuCdxgykGxvDMxuRk96IY9ObcExaABly+BdEG4L9IYMdgTR80pSGj/1p+MSfjupAYl7en/l9uGP7AEzOrsVF2fuO2BtwYnoTbhqwA/fu6I8DURx/URvyoLIhC6Oy6g7ZPrH7/o4mALUiUqXQt1Wl3GNkS8gb2BhpOWtVyNqyS04RCeWqyHCBnARofyj6qaKLCBoBNADYC+ATQD8CtNyngTWjp73gSnan6nA1UZGP3Dg/uSMx7xDUquaqd06kxEj88tvLagGUN/976PPteaXXDYaak0WRowY5UJMj0BwFctCBUsYDfX7kpB/+rXT1gTaXP3dFk21QXpeF8rov/5N8oujqCcHb/Dnw24L9tgdOvp0lkpAKntrXA1saM1DYtxrZntYr0h6T5sdNA3fgnh0DsC+KSdjq/d0OSwCGZjRhsM+P/wSOOpuxDoIqKKqAcIEpY6RKNbi1I8V2Xrvvgn7Gk3aZQi9Yd7+cLWL3A6R5qYAv/7itJ0sCQBCQdHtt2eRNovh7CPYjZ057NorjgOQUJ5UNFYhLFUtqH84CSCLOl+NEQ2Va366J+j7RTSNvmTEo6NMco+HFhhTIgWgOVIYA6HW0fb/Tew/O6Xbo+//tgTT8etugpHvAHs3S4z9qdft1Hx0f0zg+19MbxHV9d2FI+pHHPlQHvPjdzgFfvMaIhp8P3obBvkPP+fKBbnhkT+89IvoJVKqk+SFvC6q8AamK5ij8Nb+bkild6r8N0R8CchaAqHYziWAtIL8b85/Rj7WsHRERyzJ5/uo6ABltNbVt+6RNC+476pRRShzsAUgiJ71f/eF7Q/sdZXnZL2SODFQfW9EJB+R8ZXzBKy1/ljNzZnpml+Bg45FBAjNQVU+EYhAEA7OMDh3T9WAeWiTFq/d3S6mHfyKqCXrx2x0D8YM+u1HQpa7VNn19Qfy0/07ctX0gDnZsTEAjgG2q+sHmhszug33+Q4oxndNtf90EX+2JY3/yrGvz2F998JuneEKeaUD9DwD0cut7mCrGAbp8/cA3311bNmnB2G1nPNSeRCA3uHsIHDz8AfhPfX/3x6wAlDyYACSR5cuXh3JLij8Q4GtttbVDego6YQJwNM3rAHzQ/O8Qa+6fVCwqi766LaRo3FiXMUdUe9hG+gLoC0U/AfojXHzHyU2RHPCr4MHqvqizDc7u1vosjAG+AO449lNsacjE4zU9sS3wxfIUDQB2A9ihgmoA1cbWahXsUKAaNnaJTz5tbGr45KurSN67eEpXAP8B8JV3PNLFzsT3AbS57kYkVCHrH7j4Iltxk4R0ImLY+xouAy1/XDfo9aL1SycVjblu5ZuR7C+2w1eKiq2RrC5I8ccEIMkI9F1A2kwAYMwpAP7pfkSpQWy5ruUt2UAeXD2nbO6R9hlmFXWVoKe/L2T3CyGcIIhoHwA9Ac0WNdm20WxR9IAiG4JshNdRiGpBgVRhAwf+p6Z3LYCMs7sdaLVWhBHFiKx6jMhq8L9R1+U7y2p7/3OLteRge843sXj5wbVlk/8CoOir20WlWBVLxMmI2zaoZZn1g9/81roylEB0ZHzfucrptsH6Ncsuvi+7Z+aNThebUtFTHE1GEb7/TzZMAJKN4D1nt6WEW/wlYa1bNnmiCoa33K4eXXq0/ZofPAcRadElyzIjGndmA+j5Rdlb1WxA0mwb3Y2BBzZ6KGwDkR6i6lGR7hD4oOgqQLqtmiUiWSISfh2k2kMP/1aZBqC1Ye1HKiZV08q2OoTLD39BAIXIvvBptVFVG4xIvQJNEByEIiCq+1UkBNV9AmPDYJ9tI2QM9gPqb6088udjVjYAWLvsYguivzzyL1HTTs86OOMnN/zfY0du44BgERTTcejv7mvrHrj4HOCZ1e097CprgjdjYJer1skbs6A4tR3f9/0AXgdQIYLNdkg/UYMdaV7ZDwC2X7rZwHEQ+wQVM1qg4xFej6EtRkSLD9TUBwDc4CgSdTYAECLvOjoeJQwmAMlGHV5k2vZrAgqzBUWt3J9Xu7ZuvWXZm8IP29YeuO4rm9zq3bxy3uKjDpKMpXHTnrHWlk3qBsiNR2wkOGf9oit6j5nxeLsWZQKAcVNX/Htt2eSXEV7y+iuH1iIAqyM93qOPTvEcU9twlaj+HOFZKZHYBuAJEX3Ca3teGz3t6bZKQx6yONiaZZecasT+jgJXo40S3Cq4Gg4TAFF1lsDY7AFINglZ/JqOTBwmACrIczuWVPDmsgsHCnBZy+0iEtV3wBS5sVNX3iyiRyuWY+w0/6uvPvjNDvV2qeKwtetVccWa+y4e7PQYjz46xbO27OKrjt1X/7ao/hnOH/4hAE8B9qSx204/dlzhiuKxU1c+7+Dhf5jx055+Z2zhil82bqsbqqpXAYjKeDyn9xLhFMCkwwQg2aR7t8BBf5wAvfNKr3N8A+usAvBNA+D76jYFtnvt7U/GKSRqJgKFYlUbzU71hDyvr1l2yeXtPU/T9rrHER4M+FVeMZja1r5vLivwrS2bdM1xNQ1bAP0LHNbgUGC7Cn7j8XpPGFe44rJxhc8+26Gpel8x0VodHD9t5SNjt52eD9WpCA+QPITol3U1jmZ4adGxAjhZ3Eeb702URJgAJJnm2vqfOGkrtoe9AEexyprghei1LbeL6LLR08qTpkxrShMpQXiU/9F0F7EfW1M26Z7Khy6IuJTfRGt1ECoPtNyuooVvLivwtbbPmt9NyVyz7OIZARmwFZA/hkfaO/IhINP3NdonjJ+64hdn/OjJTyON1ymxLHvctJUPqAmeAmAhvnztdHe3nlm3OjmGxxan95CPmu9NlEQ4BiAJCVCpwJC22tnhrruVMQgpKWUMyvoWgJa9JEENmsMeBhQfY6euKF+z7JJRIvY8AN/EkReNEoH8tL7Rd+massnTxxeueC6S8/gQWBaAtwRf6Q0SYKAfAy4HsPzzba//4bJjg6HgVNH6QoSngzr1tkAXNGyr/5+J1upg282jZ/y1z+0F8JPmfxERkTx1NOpYK9tuQ4mGCUASUkgloJe21U5U2QNwdEWtbHts/PRn2l3SlaJv/LSn3wHwLVXIuvsn3XXUgYHACQL8Y+39k1+0Q/LzM697Zq2Tc4ye9tz2dfdPfkIVU766XUSL1bL+vn7wm99U1WmhYHCyRFCxT4EtAv312G1n/C1aXfyxpHB2DxEYJgBJiAlAElJBpbN5uY677zqddUsvOk0hZ7fcrjCHDQijxBCel7/ypjVlk7dIuFDPkQsxKc4zRs9bd//ktQD+1OD1PTrxh08ctYtaIUsAnXLoVjln3aA3tkEj+rYPAP8W4Ndjt53+aPjBn7QdcY7uISrsAUhGTACSkDdkV4aMo4nFQwuswqxyqyziEcWpTj1mBg5fW/ntcVOffgWFcQmJHBpfuOIP6+6fXKmKv6ONV2HhcrgYlxEILFlbNvlNUXnFNvou1FQZsQ8aNY0BIEvsUG+BHgdgtwItixA5fvgrsAWq88ZtP+N/ww/+FZH/ByaI3Jtv7gI0OJrNYIdsJgBJiAlAEnoro98Hef7qgwC6ttHUEwykD0e4oAg1e/XBS7shFLqq5XYBFkej+hu5b+zUFeVrHrhwFGzfPQL9voNdPADGqOiYcO+ZDVUgBDs8EtpIB9d80DdUPfPGFT79ZHNPRUcOlhh8DcPhbKD4gU0L7vvQ7XAo+jgLIBlZlq2O5/iGzmi7Tedi7ODVOKT+OwDgABrtv8QjHmqf8dc+t3d84TNXq60XweV1L46QGygEL4roBeMKV54xftrTT6RUAmkwxmHLjXBUKpASDROAJGXCFVPbpCrj3I4l2Ygt17XcpioPubkCHLln/HUr/+FTc5qK3oJW5rxHQ4t3RXsB3K1qThs3dcX5Y6eufN6Nc8absWWsk3bhQcmUjPgKIFkp1kMwva1mAji6iDuL9tb9p8TWXDnvzlcfvHSpCdkzBDoVwAlRPYnIRgV+2+Q9+OjEH65ujOqxE5CKOvzyYK93NxJyCxOAJGV77HXibF30E4f9rGjAljuX7HA7pmQQ87r/FFNn/fipAwDmq2LB+rLJEyD4ngIXADimo8cW6Lvjpq5wVEEv2Q0v+Wl/IHi8k7bGeB1NtaTEwwQgSW2cc997eSXFu3H4iOXD+NJkDIBOX9r2zWUXDgyw7n+nEH4Xv2IVEC4lvG7pxUPV2GdCZSgEOQgXgMoAkCZASIHdAlSr4AOFbhE1AwH97VeP+fn6AJ2hToRHguOdvNVXYE/lnN9XuR8RuYEJQPJSFbwuikltNoSMBROA5rr/eljdfx/r/qe8sdc9sxXAVqftV1kTvBmDutyIQytFfr4+gBXl8BKQjj18denDiWAtOAAwaXEQYBITG4663prnQndqrPtPkWjP+gCpRNTZAEBRWed2LOQeJgBJTMVZAiDQ0ydYVqfu7WHdf4qUD4FlAA5JDr+yPkDKmmBZXgUKnLS1jbN7ECUmJgBJLDPNvIHweuJtyaoN7M53O54Ex7r/FJHR057bLoInWm4X0eJ4xBMrzfcKJ6sqhpr89W+4HQ+5hwlAEltvLdwPxdtO2qqNc92OJ1GtW3rRaWDdf2qH8PoALck5a5ZNGhH7aGLDVj3PUUPB5nfv+MMBl8MhFzEBSHYOXwOo6Pluh5Ko1GNm4PARTeG6/0RHMW7qM6vRStVNkcOLSaUQZwmAgvP/kxwTgCSnoqsdNv36uBtuONJa6inr1Qcv7QYF6/5TuwnQWpGoq9f9/qKW5aST3vHWNRkAznLSVpunWFLyYgKQ7Hz2i3A2DSejrkug080GYN1/6qiGQNZDAFqWie5qZ4qTRYiSSnd/lzMBOPmioDa8TACSHBOAJLfRWrpLHC4MZJy+20shrPtPHTWxePlBAIcljKJSrIcvKZ3UjNPuf8HGzfPu3elyOOQyJgApQBUvOGzXqcYBrFs2eSJY95+iQbAIh/e0fW3dAxefE49w3KJweI9weM+hxMYEIAUI8KLDpgUjZk3v6WowCcSWVqf+se4/RWzc1BX/BvByy+0Cbe0zlpTyret7ABjlpK0NcXrPoQTGBCAF2IHMlwH4HTT1GI+Z4G40ieHNZRcOFNb9pyhSxWFTAj9fHyAe8USbHQieB8DjoKnfTrP/5XY85D4mAClg41131QHqbEqO4kKXw0kI4br/OKzuv5d1/6mdmrbXPQ6gZeGoz9cHSHqieoGjdsC6LdaSg27HQ+5jApAi1PlrgMthWSn9d2fdf3JDSq8PYFkGkEucNFUo3/+niJR+EHQmIo4TgP4jm6rHuBpMnLHuP7klVdcHyG/aPQ7QgU7aRnCvoQTHBCBF9PT1Wwdgr5O2Cv2Wy+HEG+v+kytSd30A22kCs7eHr9/rroZCMcMEIEWstqygQJ5x1FjkCpfDiRvW/Se3peT6AM7vCU+ttqygq7FQzDABSCWKx501w0kjfj4jeW9WR8G6/+S2VFsfYHjJ9FwFTnLSVlUc3WMoOTABSCGZjb7nANQ5aWuCmnK9AKz7T7GSSusDGDj+9l/vS/dzAGAKYQKQQtbefXcDIM85aixIuQSAdf8pVlJpfQBx3v3/bLlVVu9qMBRTTABSj9MuuvwRs6af6GokMca6/xQrqbI+QP6s646HIs9JWxFl93+KYQKQYmw7tAItpikdiYgnZWYDsO4/xVwqrA8g3m87bBmAL22Fq7FQzDEBSDGbFtxXA2C1k7Zi9HvuRhM7rPtPsZYK6wOo6A8cNRRZtcG6Z5/L4VCMMQFIQepwNgAUeakwG4B1/yleknl9gNzS6WMBnOawObv/UxATgBTkk8ATAGwnbSWkSTdoqSXW/XduzQMXn9Gen1Hrknl9AFFzjcOmIa/6eS2lICYAKah8Xtl2VX3JSVsBvjtlyhQnK4AlJNb9j4zYOqc9P6PWJev6AONuuCETwP9z1FjwfPm8su3uRkTxwAQgRRnBXx02Hbw1p1/SrhDIuv8RG9fOn9ERJOP6AA1ZTd8CkO2oseKP7kZD8cIEIEU1BBv/DsDRnF0VTfjuyqNg3X+Kq2RcH0BVfuiw6d7atLqnXA2G4oYJQIp6944/HBAVh+/t5OKRt8wY5G5E0ce6/5ET4LX2/IyOLpnWB8i9ZeYxACY4aqzyyEfWnxpdDYjihglAClPBnx029YY8eo2bsbiBdf/bQVDarp/RUSXT+gDisX8EwNG4H1tDf3I3GoonJgAprDKtz/MAPnLSVgSFyTQYkHX/22fs1BXl7fkZtS0Z1geYYFleFfzYSVsBNm5acB8/EymMCUAqsywb0D84bD3k3ZP7J+ygpZZY958STTKsD1Djr/6WAMc5aiwc/JfqmACkOC+CD8BpaWC1f+pyOFHDuv+UaJJkfQCn17hfbON0JhElKSYAKa58Xtl2BVY6ay1fzy0pHuVuRB3Huv+UsBJ4fYCRpTNGAxjvrLU8UzF/YbWrAVHcMQHoBAzguCSuCK53M5ZoYN1/SlSJvD5ASPUGp22NkfvcjIUSAxOATmDDvMXPQw8fodwqxXdyb5txgsshtduR6v63VpOdKB6OsD7A5W8uu3BgPOIBgBGzpp8ogLOV/xRbKuYsfNHlkCgBMAHoNNRpL4AXNm52NZQOCIr3CrSo+w9gWxp2HFaIhSgemj+L21ps9jV/duPCGHMLAK+Ttiq4B4e/xqAUxASgk/CmBx9WYI+TtgL9cVIVBlK5n3X/KVGMnlYegMr98Y7jc8N+VjQAgLNlf4G9vrTAI27GQ4mDCUAnUW6V1Ys4viml21690dWA2sk2wf8F8PFXNn1sAr6F8YqHqDXNn8lDPqfNn92Y8/rkZgAZTtqKYGm5VeaohDglPyYAnUhIPfcAaHDYvLi5ZGhCGX/tc3vVBEdBUQRFkZrgqDEzHnfUs0EUK2NmPL6n5ed0/LXP7Y11HAUlhQMBTHfYvDHgVybTnYijd0KUGjbPu3dnXknxHwA4WaQkA16d7bBtTDXfSDlKmRJaInxOg/D+AkCWw+b3b7lzyQ4346HEwh6ATiYkejsAv5O2Ap06/LaZJ7kcEhG5IDybR37ksHnACH7rakCUcJgAdDKb5y75FIDTQT4+jx2yXAyHiNxi6xwAaQ5b/7Vi7uKP225GqYQJQCfksXUuHJYHBuSq3NnFY1wNiIiiKrd0+lgBvuOweVCNvcDVgCghMQHohN5asKQKcLzQhxgji2FZ/KwQJQPLMqLmXhy+VPaRPLhxzn3vuhkSJSbe1DspE5RfweGMAFUtyPXv+p7LIRFRFOQ17f4BgDMcNm/UoJnjZjyUuJgAdFIVdyzaBnU+Qlkg88dYMxNmXXMiOtwYa2Z3COY6bS+qizbesfAzN2OixMUEoBPzpgfmA6h12HxQg1/nuxkPEXVMk99eAKjTNQf2NUL47r8TYwLQiZVbZbsh+LXT9gK9Lq+06Cw3YyKi9sktnT5WgWlO24vgV+/MX8wiWp0YE4BOzlsdWAjA6QAgA5UHjreucVRWlIhiI2fmzHRR8yCc39Pf8VQHHC8TTqmJCUAnV15WFhBFJHX/T+nuz7rNtYCIKGJdu9u/AHCa0/Zq6w3lZWVcQKuTYwJA2DB/8UoVrHTaXiCz+CqAKDHkzp75dVXc6nwPWbFxwZJ/uBcRJQsmAAQA8ABFAA46bq7yyIhZ03u6GRMRHV3BrYXZIvZDADwOd6m37dBP3IyJkgcTAAIAhMuAqhXBLscaMVw5jCiOAh7fEgDHO99Db9u04L4P3IqHkgsTAPpCZVq/uxVY63gHwVW5JcXXuhgSER1B/uyiqQJ8N4Jd3jh5a/XvXQuIkg4TAPqSZdmekJkOx+sEAAIsHFk6Y7SLURFRCyNLZ4xWkUge5gETMlOXL18eci0oSjpMAOgQFbcvrIQiktKgGbbqYyNnz+zrWlBE9IVh1g29bNVHATifjqv4dcXtCyvdi4qSERMAOszJVbvmAng1gl2ODSH0yATL8roVExEBEyzL6/X7HwVwQgS7vXpy1S5W8aTDMAGgwyxfvjwUEv0ugBqn+4jI+TWBXUtdDIuo09vr330vgPMi2KVW7ND32fVPrWECQK3aPHfJpyI6M6KdVH6cV1ocSVEhInIod/aMmwVaFMk+AinasGDpRy6FREmOCQAd0Ya5S/4qwAMR7aS4M3/2jMtdComoU8qfPeNyEb09kn0EeGDDvEWPuBUTJT8mAHRUBw+YGQDeiGAXo6KPjJw9/Ry3YiLqTPJLi8ar6F8Qyf1atCKzIY0Ff+iomADQUVUtXNgUEr0SQHUEu2XaYp4aMWt6gVtxEXUGI2+dmacqKwB0iWC3vSrmyrV3393gVlyUGpgAUJs2z13yqTHmuwAiGUjU3RjzbO5t009xKy6iVDZi9oxTbY/9PIAeEewWMsb898Y5iz50Ky5KHUwAyJGKOQtfUIlo1UAA6CtqVo+cPdPxKmVEBOTf9pOhRvQFAJHV1xC9vmLOwhfciYpSDRMAcmzj3MW/BxBZ/X/FAFvsl5gEEDmTN7v4ZLVDqwAMjmhHxe8r5y5Z5E5UlIqYAFBETt666wYBnopwt/622C/l/bx4mCtBEaWIvNnFJ0MQ8cNfoM/2TO97k0thUYpiAkARWb58eagh2PA9iFZEuGt/hPBi3qyZI10JjCjJ5ZYUj4LgFQCDItz1rYZg43+vtqygG3FR6mICQBF7944/HDC250IA70S4a38Y+5X8kuJvuBEXUbLKv23GBAFeAtA/sj11awjeSe/e8YcDrgRGKY0JALVLxfyF1d6Q90IAn0a4a1cFnsorLb7CjbiIkk1u6Ywr1dZ/AMiOZD8FPgkJzts8796dLoVGKY4JALVb+e33fmKrXIDIagQAQAYUy1k2mDq7/JLin0l4Zb/0iHZU7IKxL9g8d0mkCTjRFyTeAVDyG3Vb0ddCKi9BMSDinUUf9FYHp5eXlQVcCI1asbZssra2fVzhCt4PYmSCZXn3+nffG2lt/2bVtkfO2/SbRZuiHhh1KuwBoA57a86Sf9umXT0BgMqPg318zxVYhX2iHxlR4imwCvvU+Kv/2a6Hv2IXH/4ULUwAKCo2/WbRJlvlbEC2t2P3iUG/ryK3dPrYqAdGlEByS4pHBf2+1wFMjHhnxS7bK+fz4U/RwgSAombT/EXvGJXzAXzWjt2PETWr80tnFEY7LqJEkF86o1CANQBOaMfunxmYiXz4UzTxnR9F3cjS4iG24h8ATm3fEfQvjcHGIk5tcgfHAMTWKbf8qFuGN2MJIN9r5yHe8Ya8F5bffu8nUQ2MOj32AFDUVcxd/HEwLe1MBda27wjyvQxv5qb82TPOjG5kRLE1snTG6Axv5lsdePi/YdSczYc/uYEJALlii3X33lCaXiDQZ9t5iCEquiq3pHj2lClTPFENjshlU6ZM8eSWFM+2VdcAyGnfUWSF+jMnVsxfGPngWiIHmACQa7ZYSw4O3Vp9CYDb23kInwDz3hva7838kqL8aMZG5JaRs2ee9t7QfmsEmAfA187DlPVM63P5xrvuqotmbERfxXd+FBO5s4uni+D3ALztPEQTVK2e6f3uYs3zjuEYAHdMsCxvTdOumyFiIdLCPl8KQmRm5dxFS6MYGlGr2ANAMbFx/uL7BJikwJ52HiIdIvNrAtVvcrogJZrc0uljawLVb0JkPtr/8N9tjLmID3+KFWb8FFO5t8w8Rrz23wCM6cBhFIK/eH2BG8utst3Riq2zYA9A9ORb1/fQpsCvICgG0JGxKm+pkf/aOGfRh9GKjagtvOAp5nJmzkzv0tW+A4KfdPBQewHcUXfA3FO1cGFTNGLrDJgAdFxBYaEv1Dfth6r6a0S8gl8Lgoez6tOmrb377oboREfkDC94ipvckqKrBbIIQLeOHEeA9xUoqZy3eDmAVh9u9CUmAB0i+aUz/ktV56Hdo/u/sF9EizbMXfLXaARGFCle8BRX+bOuO16N5y8AojHn/w0xcsuGOYtWR+FYKYsJQPvklk4fK2ruBHBWFA73hsfW7761YElVFI5F1C684CnuCgoLfcG+ab+G6s/QsfeoAAAFnvQanf3WnCX/jkJ4KYcJQGRG3Vb0taAt8wW4LAqHC0HkTm+1/xdcAZPijRc8JYzmb1h/RLtLCB/ChmCl2pizcf7i9VE4XspgAuBMfklRvorcCMV30P7pq18Q4H1R+8cV8+97OQrhEXUYL3hKKMdb12Rk+7tYAG5GFHoDmr2mordvnLvkGXCMABOANuSVFp0FyK1QTEZ07pE2gAfUn3kjC/tQIuEFTwlp5OzicSpYqkBuFA/7FkTuOPm9nX9bvnx5KIrHTSpMAA43ZcoUz3sn9/8vwL4VKiOjdmBBpdqYxl4oSkSd9oKnxDfBsrx7m3ZfL/L/27v/2KruMo7jn+ece1sotAKh0AWH0C2bs9CydLrIEoMTlmyLRqflPzUjoVmo9deGC5LpNaYy3ebMsEhYwhKN/rFppk63BMjU7FdmRkZLUVhiQRiRX4HSVqC995zHP8DQLSBS7rmnvff9+vP+8X2eNPne8+k95zxfz0maVqx1TfqHmzZlsvmfV+IcAQLARa259tmFfPZLcnVIaizi0sMyfXdmtv4pJldioqq4DY/Jp/Xhr80vhIUfS/p8kZcekftv3ezp3h90v6wKuT1AAJA1f7vjTnNfLbPPavyT+y7FTfpNwfybfV2bDhVxXaDoKmXDowy0rO/8mHn8q+bW+gAABu5JREFUmEufSGD5dyX9MhNlNpX70auVGgCa1q5pyGTtyyatdumGBEq86R6s7d2w8ZUE1gaKrqw3PMpTy7o1912YuX5TAsvnTXpJ5s9WZ8MX3sxtHEygRqoqKQDcnuusG8lHn5bbSpfu1vhP5/tf9sm0rqer+/kE1gYSU3YbHpVhWS6XGcifWOXy78nVkFCZEZm2u/tz2ajwu50/3HI6oTolVe4BoDXXXpPPZz5lsja57lMRnx95nxOSHi9U1T+5J5cbTagGkJiy2PCoXDd/a1XtlEzNWsm/IWl6gqVGZNpusX4dVuf/OJkfHizHANCaa58djWTv9UBfkGuFintf//2GJXvyXOHMY/t+tHUowTpAoibthgfGuj3XWXd21O836WHJr0u4XGxmb7v7jiAIdgyd1iuT6TCicggAbW1t4d4bZi8JgmC5uy83s2UqwrCeKzhhsu5z7hv3buge77HWwIQxaTY88P9ozbXXFPKZVXJ7UNKCEpUdlunPctsWu7bv3vDTvSWqOy6TNQAsXveVDwemFTK/S65lSvYXn7EOyPyJTLawdWduy5kS1QQSN6E3PDBuuVzQnD92r9y+Y9JtJa4+6O5/DSx4LbZ4p0f+6u5Hf3aqxD1c1mQIAM0PPTTNqs/c6h60mvwOScsk1Ze0CdduN398VtWcX/EuP8rRhNnwQEJsybqOu930VUkrJAUp9BDJ1Cf3N9yDtwKPe+NCzd/SGgs70QLA+Yv9SJN73GzyVpMtdalJxRsFfTViSdvN9dSuDd0vqUJmQ6AyEQBQMc4fPZxZJfkqSfNSbic2ab9LvZL1mWl3YHHf4OmwP+nnCdIKADd2dlbXfSBqjD1Y5K7Fki8yqdmlhUonmI11WLKtFhe27np084GUewFKggCAitPW1hbuu6n+HnNbLekepfOf5uXEkg5fCAf9kvdLwX6zuD/OhwfPnNXxaw0ISQWAGzs7q2umqj7IRvPdg0a5N8q00KTGCxf5eUr/Qj9WJOlFN3/65neOv1jJ50OgMhEAUNFa1j8wT3F4v0xfVDKDhZJwyqUjkh0z+b9MflQKjsfmQxbbkCseCsNwIHYNhhYN5Qs+UhVEZ0fj8JwkbWk8ePJSi7b3z58lSVVBNGU0DqdmM1YdeVgbmOqiKJphCmo98NrArVaK610212XXST7HpAZJM0v4N7gW78j1CwXRMz1dmw+n3QyQFgIAcEHLIx1NFllbLF9p0i1p95OUzQsOXPLzBw4sKGkfJbZfrhcU+HM9XZteTbsZYCIgAACX8N8w4PI2SR9Ju59iqqAA0C/XH7joA5dGAACuoOWRjiaP9Blz3SXTUklVafd0Lco4AIzK9bqbtlmo3/d8v3tP2g0BExkBALgKrbn2mrhQvTSO4+VmttzdW9Pu6WqVWQDol7TDzHaEhdFt5XJeA1AKBADgGty6vuND0fnZ8580aalKN31w3CZ5ADjg0uuS/hSatr/d1f3PtBsCJisCAFBETWvXNIRV+mjgQWvs8R1mtlRSTdp9jfXE/EOaFrz3jbd/x6EePHh9Sh1dVt7Mej3219x8Z2j2Fy74QPEQAIAEtba3Z+P6qpZYus3cm12+SLLFkmak1dPKWSd1Z93gez57ebBOz56clVJHkqQByXdL2iMLegLpreD4aM/OLVvyaTYFlDMCAJCCRevXXG8eLApdi93ixWbBLe7eqBK8S58x1+dmntLHpw9Lkt4Ynq7nT81UwUvydXDKzPrd479L1hfLet3ivr6uTYdKURzARQQAYAJZkvv6jHg03yizhYF7o8sbJVso1wdlmitpdto9XsEJuY7K9K6df0Bvf2zWL/f9QVW2f1fuJwNpNwjgPAIAMIm0trdnC/XBnDiyhjBQg3s4R4rnymyGSXUur5U0XbJaM5vhHtdJFko2VfIpY5aq08URyJGksfcEzko6J6lgZkPuPiD5kKRhkw25NCj3ASk4ahYdi2IdCUI/kjkeH+MnewAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACAJOk/2T8MIVuBW1sAAAAASUVORK5CYII=" alt="LiaVia Logo – Kintsugi-Schale" style="max-width:70%;height:auto;">
  </div>
  <div class="about-text">
    <p class="eyebrow">Über mich</p>
    <h2>Hinter LiaVia</h2>
    <p>Seit über 20 Jahren begleite ich Menschen auf dem Weg zu mehr Beweglichkeit, Körperbewusstsein und innerer Ruhe. 2014 habe ich meine Yogalehrer-Ausbildung in Indien abgeschlossen – seitdem verbinde ich klassische Yoga-Praxis mit Atemarbeit, Bewegung zu Musik und Methoden, die nach Libra und Precht inspiriert sind.</p>
    <p>Mein Schwerpunkt liegt auf Menschen, die spürbar etwas für ihren Rücken, ihre Hüfte und ihre allgemeine Beweglichkeit tun möchten – ohne Leistungsdruck, in ihrem eigenen Tempo.</p>
    <a class="book-pill" href="https://amzn.eu/d/4ZCwSxf" target="_blank" rel="noopener">Mein Buch „Kintsugi Kriegerin” auf Amazon →</a>
    <p style="font-size:0.9rem;color:#7A938E;margin-top:0.6rem;">Ein persönlicher Erfahrungsbericht – auch zum Thema Fibromyalgie.</p>
  </div>
</section>

<!-- CTA -->
<section id="buchen" class="cta">
  <p class="eyebrow">Jetzt loslegen</p>
  <h2>Bereit für die erste Einheit?</h2>
  <p class="lead">Wähle deinen Termin – outdoor im Park, indoor im Raum oder online. Ich freue mich auf dich.</p>
  <div class="cta-buttons">
    <a href="https://calendly.com/liavia-yoga2go" target="_blank" rel="noopener" class="btn btn-primary">Termin buchen (Calendly)</a>
    <a href="https://wa.me/4915207064907" target="_blank" rel="noopener" class="btn btn-outline">WhatsApp schreiben</a>
    <a href="mailto:liavia.yoga2go@gmail.com" class="btn btn-outline">E-Mail schreiben</a>
    <a href="https://www.instagram.com/liavia_kintsugi" target="_blank" rel="noopener" class="btn btn-outline">Instagram</a>
  </div>
  <p class="price-note">Gruppe: Online 12,50&nbsp;€ · Outdoor 15&nbsp;€ · Indoor 18&nbsp;€ &nbsp;|&nbsp; Personal: Online 25&nbsp;€ · Indoor 35&nbsp;€ · Outdoor/bei dir 55&nbsp;€ — Preise gelten für Köln und Umgebung.</p>
</section>

<footer>
  <div class="logo">LIA <span>VIA</span> · Balance Life2Go</div>
  <div class="footer-links">
    <a href="#angebote">Angebote</a>
    <a href="#fuer-wen">Für wen</a>
    <a href="#ueber-mich">Über mich</a>
    <a href="https://amzn.eu/d/4ZCwSxf" target="_blank" rel="noopener">Buch</a>
    <a href="mailto:liavia.yoga2go@gmail.com">liavia.yoga2go@gmail.com</a>
    <a href="https://wa.me/4915207064907" target="_blank" rel="noopener">WhatsApp</a>
    <a href="https://www.instagram.com/liavia_kintsugi" target="_blank" rel="noopener">Instagram</a>
  </div>
</footer>

</body>
</html>
