<!DOCTYPE html>
<html lang="fr" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Invitation de mariage &mdash; Walid &amp; Shaïma</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;500;600&family=Parisienne&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --green-deep:#fdf3ef;
    --green-mid:#f7e3dc;
    --green-soft:#f3d9d0;
    --gold:#b8886a;
    --gold-light:#a8635a;
    --rose-deep:#8a4a44;
    --rose-mid:#c98a7d;
    --blush:#f3d5cb;
    --cream:#4a2f2b;
    --cream-dim:#8a6a63;
    --card-bg:rgba(255,255,255,.55);
    --card-border:rgba(183,110,95,.28);
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html,body{
    background:var(--green-deep);
    color:var(--cream);
    font-family:'Jost',sans-serif;
    overflow-x:hidden;
    scroll-behavior:smooth;
  }
  .display{font-family:'Cormorant Garamond',serif;}
  .script{font-family:'Parisienne',cursive;}

  body::before{
    content:'';
    position:fixed;inset:0;
    background:
      radial-gradient(circle at 15% 10%, rgba(201,142,110,.16), transparent 40%),
      radial-gradient(circle at 85% 90%, rgba(183,110,95,.14), transparent 45%),
      linear-gradient(180deg, var(--green-deep), var(--green-mid) 60%, var(--green-deep));
    z-index:-2;
  }
  body::after{
    content:'';
    position:fixed;inset:0;
    background-image:radial-gradient(rgba(120,70,60,.05) 1px, transparent 1px);
    background-size:3px 3px;
    z-index:-1;
    opacity:.5;
  }

  /* ================= SEAL / ENVELOPE OVERLAY ================= */
  #envelope{
    position:fixed;inset:0;
    z-index:50;
    display:flex;align-items:center;justify-content:center;
    background:linear-gradient(180deg, var(--green-deep), var(--green-mid));
    transition:transform 1.1s cubic-bezier(.65,0,.35,1), opacity 1s ease .1s;
  }
  #envelope.opened{
    transform:translateY(-100%);
    opacity:0;
    pointer-events:none;
  }
  .env-card{
    position:relative;
    width:min(78vw,300px);
    aspect-ratio:3/4;
    display:flex;flex-direction:column;align-items:center;justify-content:center;
    text-align:center;
    border:1px solid var(--card-border);
    background:var(--card-bg);
    box-shadow:0 20px 50px rgba(150,90,80,.14);
    border-radius:4px;
    padding:28px 20px;
    cursor:pointer;
    -webkit-tap-highlight-color:transparent;
  }
  .env-card::before,.env-card::after{
    content:'';
    position:absolute; inset:8px;
    border:1px solid rgba(183,110,95,.22);
    pointer-events:none;
  }
  .env-note{
    font-size:16px;
    letter-spacing:.5px;
    color:var(--gold-light);
    opacity:.9;
    margin-top:22px;
    font-style:italic;
  }
  .env-hint{
    margin-top:auto;
    font-size:11px;
    color:var(--cream-dim);
    opacity:.55;
    letter-spacing:1.5px;
    padding-top:26px;
    text-transform:uppercase;
  }

  .seal{
    width:78px;height:78px;
    border-radius:50%;
    background:radial-gradient(circle at 35% 30%, var(--rose-mid), var(--rose-deep) 65%, #6b332e 100%);
    display:flex;align-items:center;justify-content:center;
    box-shadow:0 8px 22px rgba(0,0,0,.45), inset 0 2px 4px rgba(255,255,255,.15), inset 0 -6px 10px rgba(0,0,0,.35);
    transition:transform .5s cubic-bezier(.34,1.56,.64,1);
  }
  .seal svg{width:34px;height:34px;opacity:.9;}
  .env-card:active .seal{transform:scale(.9) rotate(-8deg);}
  .seal.crack{animation:crack .6s ease forwards;}
  @keyframes crack{
    0%{transform:scale(1) rotate(0);}
    40%{transform:scale(1.15) rotate(10deg);}
    100%{transform:scale(0) rotate(35deg);opacity:0;}
  }

  /* ================= MAIN PAGE ================= */
  main{
    position:relative;
    max-width:480px;
    margin:0 auto;
    min-height:100vh;
    padding:0 22px 60px;
  }

  .branch{
    position:absolute;
    width:150px;height:150px;
    opacity:.9;
    pointer-events:none;
  }
  .branch.tl{top:0;left:-6px;}
  .branch.br{bottom:0;right:-6px;transform:rotate(180deg);}

  section{position:relative;padding:64px 0 10px;}

  .eyebrow{
    display:flex;align-items:center;justify-content:center;gap:10px;
    font-size:12px;letter-spacing:3px;color:var(--gold-light);
    opacity:.85;margin-bottom:18px;
    text-transform:uppercase;
  }
  .eyebrow::before,.eyebrow::after{content:'';width:26px;height:1px;background:linear-gradient(90deg,transparent,var(--gold),transparent);}

  /* HERO */
  .hero{text-align:center;padding-top:86px;}
  .hero .names{
    font-family:'Parisienne',cursive;
    font-size:clamp(46px,14vw,62px);
    line-height:1.3;
    color:var(--gold-light);
    text-shadow:0 2px 18px rgba(201,162,95,.25);
  }
  .hero .amp{
    display:block;
    font-size:24px;
    color:var(--rose-mid);
    margin:2px 0;
    font-family:'Cormorant Garamond',serif;
    font-style:italic;
  }
  .hero .verse{
    margin-top:26px;
    font-size:15px;
    line-height:1.9;
    color:var(--cream-dim);
    font-weight:300;
    font-style:italic;
    max-width:300px;
    margin-inline:auto;
  }
  .hero .verse span{color:var(--gold-light);font-size:11.5px;display:block;margin-top:10px;letter-spacing:1px;font-style:normal;text-transform:uppercase;}

  .divider{
    width:1px;height:44px;
    background:linear-gradient(var(--gold),transparent);
    margin:34px auto 0;
  }

  /* COUNTDOWN */
  .countdown-wrap{text-align:center;}
  .countdown{
    display:flex;justify-content:center;gap:14px;margin-top:26px;
  }
  .cd-cell{
    width:64px;
    padding:14px 0 10px;
    background:var(--card-bg);
    border:1px solid var(--card-border);
    border-radius:8px;
    box-shadow:0 8px 24px rgba(150,90,80,.08);
  }
  .cd-num{font-family:'Cormorant Garamond',serif;font-weight:600;font-size:26px;color:var(--gold-light);}
  .cd-label{font-size:9.5px;letter-spacing:1px;color:var(--cream-dim);opacity:.7;margin-top:4px;text-transform:uppercase;}

  /* DETAILS */
  .details{display:flex;flex-direction:column;gap:14px;margin-top:26px;}
  .detail-card{
    display:flex;align-items:center;gap:16px;
    padding:18px 18px;
    background:var(--card-bg);
    border:1px solid var(--card-border);
    border-radius:10px;
    box-shadow:0 8px 24px rgba(150,90,80,.08);
  }
  .detail-icon{
    flex:none;width:42px;height:42px;border-radius:50%;
    background:rgba(183,110,95,.14);
    display:flex;align-items:center;justify-content:center;
  }
  .detail-icon svg{width:20px;height:20px;stroke:var(--gold-light);}
  .detail-text .t1{font-size:15.5px;color:var(--cream);font-weight:500;}
  .detail-text .t2{font-size:12.5px;color:var(--cream-dim);opacity:.7;margin-top:2px;}

  /* LOCATION */
  .map-box{
    margin-top:22px;
    border-radius:12px;
    overflow:hidden;
    border:1px solid var(--card-border);
    position:relative;
    aspect-ratio:16/10;
    background:
      linear-gradient(160deg, rgba(183,110,95,.14), rgba(183,110,95,.03)),
      repeating-linear-gradient(45deg, rgba(120,70,60,.035) 0 2px, transparent 2px 14px);
  }
  .map-pin{
    position:absolute;top:50%;left:50%;
    transform:translate(-50%,-100%);
    width:34px;height:34px;
  }
  .map-pin svg{width:100%;height:100%;filter:drop-shadow(0 6px 10px rgba(0,0,0,.4));}
  .map-btn{
    display:inline-flex;align-items:center;gap:8px;
    margin-top:16px;
    padding:12px 26px;
    border:1px solid var(--gold-light);
    border-radius:30px;
    color:var(--gold-light);
    font-size:13px;
    letter-spacing:.5px;
    text-decoration:none;
    background:rgba(183,110,95,.08);
  }

  /* RSVP */
  .rsvp{text-align:center;}
  .rsvp-btn{
    appearance:none;border:none;cursor:pointer;
    margin-top:22px;
    padding:16px 40px;
    font-family:'Jost',sans-serif;
    font-size:14px;letter-spacing:1px;font-weight:500;
    text-transform:uppercase;
    color:#fdf3ef;
    background:linear-gradient(135deg, var(--rose-mid), var(--gold-light));
    border-radius:30px;
    box-shadow:0 10px 26px rgba(183,110,95,.28);
    transition:transform .25s ease;
  }
  .rsvp-btn:active{transform:scale(.96);}
  .rsvp-btn.confirmed{
    background:linear-gradient(135deg,#8a4a44,#6b332e);
    color:#fdf3ef;
  }
  .rsvp-sub{margin-top:14px;font-size:12.5px;color:var(--cream-dim);opacity:.65;}

  .cal-link{
    display:block;margin-top:10px;
    font-size:12px;color:var(--gold-light);
    opacity:.8;text-decoration:underline;
  }

  footer{
    text-align:center;
    margin-top:70px;
    padding-top:26px;
    border-top:1px solid rgba(201,162,95,.2);
  }
  footer .fam{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:18px;color:var(--gold-light);line-height:1.6;}
  footer small{display:block;margin-top:10px;font-size:11px;color:var(--cream-dim);opacity:.5;letter-spacing:2px;}

  /* ---------- falling petals (ambient ) ---------- */
  #petals{position:fixed;inset:0;pointer-events:none;z-index:5;overflow:hidden;}
  .petal{
    position:absolute;top:-5%;
    width:9px;height:9px;
    background:var(--rose-mid);
    border-radius:0 60% 0 60%;
    opacity:.55;
    animation:fall linear infinite, sway ease-in-out infinite;
    filter:drop-shadow(0 0 2px rgba(0,0,0,.2));
  }
  @keyframes fall{
    to{transform:translateY(112vh) rotate(300deg);}
  }
  @keyframes sway{
    0%,100%{margin-left:0;}
    50%{margin-left:26px;}
  }

  /* ---------- gold burst on seal open ---------- */
  .burst{position:absolute;inset:0;pointer-events:none;}
  .spark{
    position:absolute;top:50%;left:50%;
    width:5px;height:5px;border-radius:50%;
    background:var(--gold-light);
    opacity:0;
  }
  .spark.go{animation:spark-fly .8s ease-out forwards;}
  @keyframes spark-fly{
    0%{opacity:1;transform:translate(-50%,-50%) scale(1);}
    100%{opacity:0;transform:translate(calc(-50% + var(--dx)), calc(-50% + var(--dy))) scale(.3);}
  }

  /* ---------- scroll reveal ---------- */
  .reveal{opacity:0;transform:translateY(26px);transition:opacity .9s cubic-bezier(.2,.7,.2,1), transform .9s cubic-bezier(.2,.7,.2,1);}
  .reveal.in{opacity:1;transform:translateY(0);}
  .details .detail-card{opacity:0;transform:translateY(16px);transition:opacity .7s ease, transform .7s ease;}
  .reveal.in .detail-card{opacity:1;transform:translateY(0);}
  .details .detail-card:nth-child(1){transition-delay:.05s;}
  .details .detail-card:nth-child(2){transition-delay:.18s;}
  .details .detail-card:nth-child(3){transition-delay:.31s;}
  .countdown .cd-cell{opacity:0;transform:translateY(14px) scale(.9);transition:opacity .6s ease, transform .6s ease;}
  .reveal.in .cd-cell{opacity:1;transform:translateY(0) scale(1);}
  .countdown .cd-cell:nth-child(1){transition-delay:.05s;}
  .countdown .cd-cell:nth-child(2){transition-delay:.15s;}
  .countdown .cd-cell:nth-child(3){transition-delay:.25s;}
  .countdown .cd-cell:nth-child(4){transition-delay:.35s;}

  /* ---------- hero letter-in ---------- */
  .hero .eyebrow, .hero .names, .hero .verse, .hero .divider{
    opacity:0;transform:translateY(18px);
    animation:hero-in .9s cubic-bezier(.2,.7,.2,1) forwards;
  }
  .hero .eyebrow{animation-delay:.15s;}
  .hero .names{animation-delay:.35s;}
  .hero .verse{animation-delay:.65s;}
  .hero .divider{animation-delay:.85s;}
  @keyframes hero-in{to{opacity:1;transform:translateY(0);}}

  /* ---------- countdown tick pulse ---------- */
  .cd-num.pulse{animation:pulse .4s ease;}
  @keyframes pulse{
    0%{transform:scale(1);}
    30%{transform:scale(1.28);color:var(--rose-mid);}
    100%{transform:scale(1);}
  }

  /* ---------- branch draw-in ---------- */
  .branch path{
    stroke-dasharray:260;
    stroke-dashoffset:260;
    animation:draw 1.8s ease forwards 1.1s;
  }
  .branch ellipse, .branch circle{
    opacity:0;
    animation:fadein .6s ease forwards;
  }
  .branch ellipse:nth-of-type(1){animation-delay:1.6s;}
  .branch ellipse:nth-of-type(2){animation-delay:1.8s;}
  .branch ellipse:nth-of-type(3){animation-delay:2s;}
  .branch circle:nth-of-type(1){animation-delay:2.1s;}
  .branch circle:nth-of-type(2){animation-delay:2.2s;}
  .branch circle:nth-of-type(3){animation-delay:2.3s;}
  @keyframes draw{to{stroke-dashoffset:0;}}
  @keyframes fadein{to{opacity:.55;}}

  /* ---------- map pin drop ---------- */
  .map-pin{opacity:0;transform:translate(-50%,-160%);}
  .map-box.in .map-pin{animation:drop .7s cubic-bezier(.34,1.56,.64,1) forwards;}
  @keyframes drop{
    0%{opacity:0;transform:translate(-50%,-220%);}
    60%{opacity:1;transform:translate(-50%,-90%);}
    100%{opacity:1;transform:translate(-50%,-100%);}
  }

  @media (prefers-reduced-motion: reduce){
    *{animation:none !important;transition:none !important;}
    .reveal{opacity:1;transform:none;}
    #petals{display:none;}
  }
</style>
</head>
<body>

<!-- ===== SEAL / ENVELOPE INTRO ===== -->
<div id="envelope">
  <div class="env-card" id="envCard">
    <div class="seal" id="seal">
      <svg viewBox="0 0 24 24" fill="none" stroke="var(--gold-light)" stroke-width="1.2">
        <path d="M12 21s-7-4.35-9.5-9C.5 7.5 3 3 7 3c2.2 0 3.7 1.3 5 3 1.3-1.7 2.8-3 5-3 4 0 6.5 4.5 4.5 9-2.5 4.65-9.5 9-9.5 9z"/>
      </svg>
    </div>
    <div class="env-note display">Cette invitation vous est réservée</div>
    <div class="env-hint">Touchez le sceau pour l'ouvrir</div>
    <div class="burst" id="burst"></div>
  </div>
</div>

<!-- ambient falling petals -->
<div id="petals"></div>

<!-- ===== MAIN INVITATION ===== -->
<main>

  <svg class="branch tl" viewBox="0 0 150 150" fill="none">
    <path d="M2 2C40 8 70 20 90 45c14 17 20 38 16 60" stroke="#b8886a" stroke-width="1.1" opacity=".6"/>
    <ellipse cx="32" cy="16" rx="10" ry="6" fill="#8a4a44" opacity=".55" transform="rotate(25 32 16)"/>
    <ellipse cx="55" cy="30" rx="8" ry="5" fill="#c98a7d" opacity=".5" transform="rotate(10 55 30)"/>
    <ellipse cx="80" cy="52" rx="7" ry="4.5" fill="#b8886a" opacity=".55" transform="rotate(-15 80 52)"/>
    <circle cx="20" cy="10" r="2" fill="#a8635a"/>
    <circle cx="45" cy="22" r="1.6" fill="#a8635a"/>
    <circle cx="90" cy="70" r="1.6" fill="#a8635a"/>
  </svg>
  <svg class="branch br" viewBox="0 0 150 150" fill="none">
    <path d="M2 2C40 8 70 20 90 45c14 17 20 38 16 60" stroke="#b8886a" stroke-width="1.1" opacity=".6"/>
    <ellipse cx="32" cy="16" rx="10" ry="6" fill="#8a4a44" opacity=".55" transform="rotate(25 32 16)"/>
    <ellipse cx="55" cy="30" rx="8" ry="5" fill="#c98a7d" opacity=".5" transform="rotate(10 55 30)"/>
    <ellipse cx="80" cy="52" rx="7" ry="4.5" fill="#b8886a" opacity=".55" transform="rotate(-15 80 52)"/>
    <circle cx="20" cy="10" r="2" fill="#a8635a"/>
    <circle cx="45" cy="22" r="1.6" fill="#a8635a"/>
    <circle cx="90" cy="70" r="1.6" fill="#a8635a"/>
  </svg>

  <!-- HERO -->
  <section class="hero">
    <div class="eyebrow">Nous nous marions</div>
    <div class="names script">Walid<span class="amp">&amp;</span>Shaïma</div>
    <p class="verse">
      « Aimer, ce n'est pas se regarder l'un l'autre, c'est regarder ensemble dans la même direction. »
      <span>Antoine de Saint-Exupéry</span>
    </p>
    <div class="divider"></div>
  </section>

  <!-- COUNTDOWN -->
  <section class="countdown-wrap reveal">
    <div class="eyebrow">Compte à rebours</div>
    <div class="countdown" id="countdown">
      <div class="cd-cell"><div class="cd-num" id="cd-days">00</div><div class="cd-label">Jours</div></div>
      <div class="cd-cell"><div class="cd-num" id="cd-hours">00</div><div class="cd-label">Heures</div></div>
      <div class="cd-cell"><div class="cd-num" id="cd-mins">00</div><div class="cd-label">Min</div></div>
      <div class="cd-cell"><div class="cd-num" id="cd-secs">00</div><div class="cd-label">Sec</div></div>
    </div>
  </section>

  <!-- DETAILS -->
  <section class="reveal">
    <div class="eyebrow">Détails du grand jour</div>
    <div class="details">
      <div class="detail-card">
        <div class="detail-icon"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="5" width="18" height="16" rx="2"/><path d="M8 3v4M16 3v4M3 10h18"/></svg></div>
        <div class="detail-text">
          <div class="t1">Vendredi 18 décembre 2026</div>
          <div class="t2">Merci de noter la date dans votre agenda</div>
        </div>
      </div>
      <div class="detail-card">
        <div class="detail-icon"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 3"/></svg></div>
        <div class="detail-text">
          <div class="t1">Réception à 20h00</div>
          <div class="t2">Merci d'arriver un quart d'heure avant</div>
        </div>
      </div>
      <div class="detail-card">
        <div class="detail-icon"><svg viewBox="0 0 24 24" fill="none" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M12 21s7-6.5 7-12a7 7 0 1 0-14 0c0 5.5 7 12 7 12z"/><circle cx="12" cy="9" r="2.5"/></svg></div>
        <div class="detail-text">
          <div class="t1">Domaine des Roses</div>
          <div class="t2">12 avenue des Lilas, Lyon</div>
        </div>
      </div>
    </div>
  </section>

  <!-- LOCATION -->
  <section style="text-align:center;" class="reveal">
    <div class="eyebrow">Le lieu</div>
    <div class="map-box" id="mapBox">
      <div class="map-pin">
        <svg viewBox="0 0 24 24" fill="#c98a7d" stroke="#fdf3ef" stroke-width="1"><path d="M12 2C7.6 2 4 5.6 4 10c0 6 8 12 8 12s8-6 8-12c0-4.4-3.6-8-8-8z"/><circle cx="12" cy="10" r="3" fill="#4a2f2b"/></svg>
      </div>
    </div>
    <a class="map-btn" href="https://maps.google.com/?q=Domaine+des+Roses+Lyon" target="_blank" rel="noopener">
      Ouvrir dans Google Maps
    </a>
  </section>

  <!-- RSVP -->
  <section class="rsvp reveal">
    <div class="eyebrow">Confirmez votre présence</div>
    <p style="font-size:13.5px;color:var(--cream-dim);opacity:.75;max-width:280px;margin-inline:auto;">
      Votre présence compte énormément pour nous. Merci de confirmer avant le 1er décembre.
    </p>
    <button class="rsvp-btn" id="rsvpBtn">Je confirme ma présence</button>
    <div class="rsvp-sub" id="rsvpSub">Appuyez pour confirmer</div>
    <a href="#" class="cal-link" id="calLink">+ Ajouter à mon calendrier</a>
  </section>

  <footer>
    <div class="fam display">Avec tout notre amour,<br>nous avons hâte de vous accueillir</div>
    <small>WALID &amp; SHAÏMA &nbsp;&middot;&nbsp; 18.12.2026</small>
  </footer>

</main>

<script>
  const envCard = document.getElementById('envCard');
  const envelope = document.getElementById('envelope');
  const seal = document.getElementById('seal');
  const burst = document.getElementById('burst');

  function fireBurst(){
    for(let i=0;i<18;i++){
      const s = document.createElement('div');
      s.className = 'spark';
      const angle = (Math.PI*2/18)*i + Math.random()*.3;
      const dist = 60 + Math.random()*50;
      s.style.setProperty('--dx', Math.cos(angle)*dist + 'px');
      s.style.setProperty('--dy', Math.sin(angle)*dist + 'px');
      s.style.animationDelay = (Math.random()*.08) + 's';
      burst.appendChild(s);
      requestAnimationFrame(()=> s.classList.add('go'));
      setTimeout(()=> s.remove(), 1000);
    }
  }

  envCard.addEventListener('click', () => {
    if (envelope.classList.contains('opened')) return;
    seal.classList.add('crack');
    fireBurst();
    setTimeout(() => envelope.classList.add('opened'), 380);
    document.body.style.overflow = 'auto';
  });

  // ---- ambient falling petals ----
  const petalLayer = document.getElementById('petals');
  const petalColors = ['#c98a7d','#b8886a','#e8b4a0'];
  for(let i=0;i<14;i++){
    const p = document.createElement('div');
    p.className = 'petal';
    p.style.left = Math.random()*100 + 'vw';
    p.style.background = petalColors[i % petalColors.length];
    p.style.width = p.style.height = (6 + Math.random()*6) + 'px';
    const dur = 9 + Math.random()*9;
    p.style.animationDuration = dur + 's, ' + (dur/2.2) + 's';
    p.style.animationDelay = (-Math.random()*dur) + 's, 0s';
    p.style.opacity = .3 + Math.random()*.35;
    petalLayer.appendChild(p);
  }

  // ---- scroll reveal ----
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(en=>{
      if(en.isIntersecting){
        en.target.classList.add('in');
        if(en.target.querySelector('#mapBox')) en.target.querySelector('#mapBox').classList.add('in');
        io.unobserve(en.target);
      }
    });
  }, {threshold:.25});
  revealEls.forEach(el=>io.observe(el));

  // ---- countdown ----
  const target = new Date('2026-09-04T13:00:00');
  let prev = {d:null,h:null,m:null,s:null};
  function pulseIfChanged(id, val, key){
    const el = document.getElementById(id);
    if(prev[key] !== val){
      el.textContent = val;
      el.classList.remove('pulse'); void el.offsetWidth; el.classList.add('pulse');
      prev[key] = val;
    }
  }
  function tick(){
    const now = new Date();
    let diff = Math.max(0, target - now);
    const d = Math.floor(diff / 86400000);
    const h = Math.floor((diff % 86400000) / 3600000);
    const m = Math.floor((diff % 3600000) / 60000);
    const s = Math.floor((diff % 60000) / 1000);
    const pad = n => String(n).padStart(2,'0');
    pulseIfChanged('cd-days', pad(d), 'd');
    pulseIfChanged('cd-hours', pad(h), 'h');
    pulseIfChanged('cd-mins', pad(m), 'm');
    pulseIfChanged('cd-secs', pad(s), 's');
  }
  tick();
  setInterval(tick, 1000);

  const rsvpBtn = document.getElementById('rsvpBtn');
  const rsvpSub = document.getElementById('rsvpSub');
  rsvpBtn.addEventListener('click', () => {
    rsvpBtn.classList.add('confirmed');
    rsvpBtn.textContent = 'Présence confirmée ✓';
    rsvpSub.textContent = 'Merci, nous avons hâte de vous voir !';
  });

  document.getElementById('calLink').addEventListener('click', (e) => {
    e.preventDefault();
    const ics = [
      'BEGIN:VCALENDAR','VERSION:2.0','BEGIN:VEVENT',
      'SUMMARY:Mariage de Walid et Shaïma',
      'DTSTART:20261218T180000Z',
      'DTEND:20261218T220000Z',
      'LOCATION:Domaine des Roses, 12 avenue des Lilas, Lyon',
      'DESCRIPTION:Nous serions heureux de vous compter parmi nous',
      'END:VEVENT','END:VCALENDAR'
    ].join('\n');
    const blob = new Blob([ics], {type:'text/calendar'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'invitation-mariage.ics';
    document.body.appendChild(a); a.click(); a.remove();
  });

  document.body.style.overflow = 'hidden';
</script>
</body>
</html>
