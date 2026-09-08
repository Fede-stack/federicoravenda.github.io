---
layout: single
title: "Beyond Research"
permalink: /hobbies/
author_profile: true
---

{% include base_path %}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">

<style>
.hb{
  --ink:#132029;
  --mist:#e7edee;
  --sea:#0e7c7b;
  --plum:#5a3e85;
  --neon:#d93b70;
  --line:rgba(19,32,41,.14);
  --accent:var(--sea);
  color:var(--ink);
  font-size:16px;
  line-height:1.6;
}
.hb *{box-sizing:border-box;}
.hb h2,.hb h3,.hb .hb-num,.hb .hb-tab{
  font-family:"Space Grotesk",system-ui,sans-serif;
  letter-spacing:-0.01em;
}

/* ---------- hero ---------- */
.hb-hero{
  border-top:3px solid var(--ink);
  padding-top:1.1rem;
  margin-bottom:1.6rem;
}
.hb-hero h2{
  font-size:2.1rem;
  line-height:1.1;
  margin:0 0 .5rem;
  font-weight:700;
}
.hb-hero p{
  margin:0;
  max-width:60ch;
  color:#3d4c56;
}
.hb-tabs{
  display:flex;
  flex-wrap:wrap;
  gap:.5rem;
  margin:1.4rem 0 0;
  padding:0;
}
.hb-tab{
  border:1px solid var(--line);
  background:#fff;
  color:var(--ink);
  border-radius:999px;
  padding:.5rem 1rem;
  font-size:.95rem;
  font-weight:500;
  cursor:pointer;
  transition:background .18s ease,color .18s ease,border-color .18s ease;
}
.hb-tab:hover{border-color:var(--ink);}
.hb-tab[aria-selected="true"]{
  background:var(--tab-color,var(--ink));
  border-color:var(--tab-color,var(--ink));
  color:#fff;
}
.hb-tab:focus-visible{outline:2px solid var(--ink);outline-offset:2px;}

/* ---------- panels ---------- */
.hb-panel[hidden]{display:none;}
.hb-panel{
  background:var(--mist);
  border-radius:14px;
  padding:1.4rem;
}
.hb-lead{
  font-size:1.05rem;
  margin:0 0 1.3rem;
  max-width:62ch;
}
.hb-lead b{font-weight:700;color:var(--accent);}

/* ---------- sport cards ---------- */
.hb-cards{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:1rem;
}
.hb-card{
  background:#fff;
  border-radius:10px;
  overflow:hidden;
  display:flex;
  flex-direction:column;
}
.hb-shot{
  position:relative;
  aspect-ratio:4/3;
  background:linear-gradient(160deg,#cfdcdd,#9fb6b8);
  overflow:hidden;
}
.hb-shot img{
  width:100%;height:100%;
  object-fit:cover;
  display:block;
  position:relative;z-index:2;
}
.hb-shot.is-empty img{display:none;}
.hb-shot svg{position:absolute;inset:0;width:100%;height:100%;z-index:1;}
.hb-card-body{padding:.9rem 1rem 1.1rem;}
.hb-card h3{
  margin:0 0 .35rem;
  font-size:1.1rem;
  font-weight:700;
}
.hb-card p{margin:0 0 .8rem;font-size:.92rem;color:#3d4c56;}
.hb-meter{margin-bottom:.45rem;font-size:.8rem;}
.hb-meter span{display:block;margin-bottom:.15rem;color:#5b6a73;}
.hb-bar{height:6px;border-radius:99px;background:rgba(19,32,41,.1);overflow:hidden;}
.hb-bar i{
  display:block;height:100%;width:0;
  background:var(--accent);
  transition:width .9s cubic-bezier(.2,.7,.3,1);
}

/* ---------- music ---------- */
.hb-music{display:grid;grid-template-columns:150px 1fr;gap:1.4rem;align-items:start;}
.hb-vinyl{
  width:150px;height:150px;border-radius:50%;
  border:0;padding:0;cursor:pointer;
  background:
    radial-gradient(circle at 50% 50%, #f3f0ea 0 12%, var(--plum) 12% 15%, #1a1420 15% 46%, #241b2c 46% 48%, #1a1420 48% 100%);
  box-shadow:0 6px 20px rgba(19,32,41,.25);
  position:relative;
}
.hb-vinyl::after{
  content:"";position:absolute;inset:0;border-radius:50%;
  background:repeating-radial-gradient(circle at 50% 50%,rgba(255,255,255,.05) 0 2px,transparent 2px 5px);
}
.hb-vinyl.is-spinning{animation:hb-spin 3.2s linear infinite;}
@keyframes hb-spin{to{transform:rotate(360deg);}}
.hb-vinyl-hint{display:block;font-size:.78rem;color:#5b6a73;text-align:center;margin-top:.5rem;}
.hb-steps{list-style:none;margin:0;padding:0;}
.hb-steps li{
  padding:0 0 1.1rem 2.4rem;
  position:relative;
  border-left:2px solid rgba(19,32,41,.15);
  margin-left:.6rem;
}
.hb-steps li:last-child{border-left-color:transparent;padding-bottom:0;}
.hb-num{
  position:absolute;left:-.85rem;top:0;
  width:1.7rem;height:1.7rem;border-radius:50%;
  background:var(--accent);color:#fff;
  font-size:.8rem;font-weight:700;
  display:flex;align-items:center;justify-content:center;
}
.hb-steps h3{margin:.15rem 0 .2rem;font-size:1rem;}
.hb-steps p{margin:0;font-size:.92rem;color:#3d4c56;}

/* ---------- tokyo ---------- */
.hb-skyline{
  display:block;width:100%;height:110px;
  margin-bottom:1.2rem;border-radius:10px;background:#101a2b;
}
.hb-polaroids{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
  gap:1rem;
  margin-bottom:1.2rem;
}
.hb-polaroid{background:#fff;padding:.6rem .6rem 0;border-radius:6px;}
.hb-polaroid .hb-shot{aspect-ratio:1/1;background:linear-gradient(160deg,#e3c6d3,#a3849b);}
.hb-polaroid figcaption{
  font-size:.8rem;color:#5b6a73;
  padding:.55rem .1rem .7rem;
}
.hb-chips{display:flex;flex-wrap:wrap;gap:.5rem;margin:0;padding:0;list-style:none;}
.hb-chips li{
  background:#fff;border-radius:999px;
  padding:.35rem .85rem;font-size:.85rem;
  border:1px solid var(--line);
}

.hb-polaroid .hb-shot{
  aspect-ratio:auto;
  background:none;
}
.hb-polaroid .hb-shot img{
  height:auto;
  object-fit:contain;
}
.hb-polaroid .hb-shot svg{position:static;height:150px;}
.hb-polaroids{align-items:start;}
  
@media (max-width:600px){
  .hb-hero h2{font-size:1.7rem;}
  .hb-music{grid-template-columns:1fr;justify-items:center;}
  .hb-steps{justify-self:stretch;}
}
@media (prefers-reduced-motion:reduce){
  .hb *{animation:none !important;transition:none !important;}
}
</style>

<div class="hb">

  <div class="hb-hero">
    <h2>Beyond Academia</h2>
    <p>Now that I am closer to 30 rather than 20, which, as far as I can tell, is the ideal age to start two new careers at once: in the water, and on a padel court.</p>
    <div class="hb-tabs" role="tablist" aria-label="Things I do outside research">
      <button class="hb-tab" id="hb-tab-sport" role="tab" aria-controls="hb-panel-sport" aria-selected="true" style="--tab-color:#0e7c7b">🏄 Board &amp; rackets</button>
      <button class="hb-tab" id="hb-tab-music" role="tab" aria-controls="hb-panel-music" aria-selected="false" tabindex="-1" style="--tab-color:#5a3e85">🎧 On repeat</button>
      <button class="hb-tab" id="hb-tab-tokyo" role="tab" aria-controls="hb-panel-tokyo" aria-selected="false" tabindex="-1" style="--tab-color:#d93b70">🗼 Tokyo, finally</button>
    </div>
  </div>

  <!-- ============ SPORT ============ -->
  <div class="hb-panel" id="hb-panel-sport" role="tabpanel" aria-labelledby="hb-tab-sport" style="--accent:var(--sea)">
    <p class="hb-lead">Now that I'm closer to 30 than to 20, I've reinvented myself as an <b>occasional, low-level surfer</b> and a padel player with a decent smash and a certain elegance at the net.</p>

    <div class="hb-cards">

      <div class="hb-card">
        <div class="hb-shot">
          <svg viewBox="0 0 200 150" aria-hidden="true" preserveAspectRatio="none">
            <rect width="200" height="150" fill="#bcd4d6"/>
            <path d="M0 95c30-22 55 8 85-8s55-26 115-6v69H0z" fill="#3d8a8c"/>
            <path d="M0 118c35-16 62 10 92-4s58-20 108-2v38H0z" fill="#1c6b6e"/>
            <circle cx="152" cy="34" r="16" fill="#f0e2c4"/>
          </svg>
          <img src="{{ base_path }}/images/hobbies/surf.jpg" alt="Surfing" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <div class="hb-card-body">
          <h3>Surfing</h3>
          <p>Occasional and unmistakably low-level. The ocean and I have a deal: it lets me try and have fun, I let it win.</p>
          <div class="hb-meter"><span>Time spent finding the right wave</span><div class="hb-bar"><i data-fill="92"></i></div></div>
          <div class="hb-meter"><span>Time spent standing up</span><div class="hb-bar"><i data-fill="24"></i></div></div>
        </div>
      </div>

      <div class="hb-card">
        <div class="hb-shot">
          <svg viewBox="0 0 200 150" aria-hidden="true" preserveAspectRatio="none">
            <rect width="200" height="150" fill="#2f6f8f"/>
            <rect x="18" y="20" width="164" height="110" fill="none" stroke="#dfe9ec" stroke-width="3"/>
            <line x1="18" y1="75" x2="182" y2="75" stroke="#dfe9ec" stroke-width="3"/>
            <circle cx="100" cy="48" r="9" fill="#e4ef50"/>
          </svg>
          <img src="{{ base_path }}/images/hobbies/padel.jpg" alt="Padel" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <div class="hb-card-body">
          <h3>Padel</h3>
          <p>A decent smash, and an elegant way of moving at the net that I stole from tennis. Still understanding how to use the walls. </p>
          <div class="hb-meter"><span>Smash</span><div class="hb-bar"><i data-fill="82"></i></div></div>
          <div class="hb-meter"><span>Elegance at the net</span><div class="hb-bar"><i data-fill="88"></i></div></div>
        </div>
      </div>

      <div class="hb-card">
        <div class="hb-shot">
          <svg viewBox="0 0 200 150" aria-hidden="true" preserveAspectRatio="none">
            <rect width="200" height="150" fill="#3f8a4d"/>
            <circle cx="100" cy="75" r="34" fill="none" stroke="#e8f2e6" stroke-width="3"/>
            <line x1="0" y1="75" x2="200" y2="75" stroke="#e8f2e6" stroke-width="3"/>
            <circle cx="100" cy="75" r="7" fill="#e8f2e6"/>
          </svg>
          <img src="{{ base_path }}/images/hobbies/football.jpg" alt="Football" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <div class="hb-card-body">
          <h3>Football, past tense</h3>
          <p>Former attacking midfielder. Without all those ankle and knee injuries I would have… still not made it.</p>
          <div class="hb-meter"><span>Vision on the pitch</span><div class="hb-bar"><i data-fill="74"></i></div></div>
          <div class="hb-meter"><span>Ankles and knees</span><div class="hb-bar"><i data-fill="18"></i></div></div>
        </div>
      </div>

    </div>
  </div>

  <!-- ============ MUSIC ============ -->
  <div class="hb-panel" id="hb-panel-music" role="tabpanel" aria-labelledby="hb-tab-music" style="--accent:var(--plum)" hidden>
    <p class="hb-lead">My taste has one clear origin story and one long detour: from rock heard through car speakers to <b>RnB and Hip Hop</b>.</p>
    <div class="hb-music">
      <div>
        <button class="hb-vinyl" type="button" aria-pressed="false" aria-label="Spin the record"></button>
        <span class="hb-vinyl-hint">Tap the record</span>
      </div>
      <ol class="hb-steps">
        <li>
          <span class="hb-num">1</span>
          <h3>Aerosmith and Red Hot Chili Peppers</h3>
          <p>Played on repeat with my dad in his old Toyota Avensis. Still the sound of every long drive.</p>
        </li>
        <li>
          <span class="hb-num">2</span>
          <h3>High school: the switch</h3>
          <p>Rock made room for RnB and Hip Hop, and it never really moved back.</p>
        </li>
        <li>
          <span class="hb-num">3</span>
          <h3>Favourite album: <em>Take Care</em>, Drake</h3>
          <p>Probably. Ask me again in a year and the answer will probably be the same.</p>
        </li>
      </ol>
    </div>
  </div>

  <!-- ============ TOKYO ============ -->
  <div class="hb-panel" id="hb-panel-tokyo" role="tabpanel" aria-labelledby="hb-tab-tokyo" style="--accent:var(--neon)" hidden>
    <svg class="hb-skyline" viewBox="0 0 600 110" preserveAspectRatio="none" aria-hidden="true">
      <rect width="600" height="110" fill="#101a2b"/>
      <circle cx="512" cy="30" r="14" fill="#d93b70" opacity=".85"/>
      <g fill="#1e2c44">
        <rect x="0" y="60" width="46" height="50"/><rect x="52" y="42" width="34" height="68"/>
        <rect x="92" y="70" width="58" height="40"/><rect x="156" y="30" width="28" height="80"/>
        <rect x="190" y="66" width="48" height="44"/><rect x="244" y="52" width="36" height="58"/>
        <rect x="330" y="58" width="52" height="52"/><rect x="388" y="38" width="30" height="72"/>
        <rect x="424" y="72" width="60" height="38"/><rect x="490" y="56" width="42" height="54"/>
        <rect x="538" y="46" width="62" height="64"/>
      </g>
      <path d="M300 18 L288 110 h24 z M282 60 h36 M276 86 h48" fill="#d93b70" stroke="#d93b70" stroke-width="3"/>
      <g fill="#f2c15b" opacity=".8">
        <rect x="60" y="52" width="4" height="5"/><rect x="70" y="64" width="4" height="5"/>
        <rect x="163" y="44" width="4" height="5"/><rect x="396" y="50" width="4" height="5"/>
        <rect x="546" y="58" width="4" height="5"/><rect x="560" y="76" width="4" height="5"/>
      </g>
    </svg>

    <p class="hb-lead">I spent high school reading Murakami and picturing Japan. In 2024 I got the opportunity to live in Tokyo for four months as a visiting researcher at NII, and <b>the city is better than the one I had imagined</b>.</p>

    <div class="hb-polaroids">
      <figure class="hb-polaroid">
        <div class="hb-shot">
          <svg viewBox="0 0 150 150" aria-hidden="true"><rect width="150" height="150" fill="#e8d3dc"/><circle cx="75" cy="70" r="30" fill="#d93b70" opacity=".55"/></svg>
          <img src="{{ base_path }}/images/hobbies/tokyo-1.jpeg" alt="Tokyo" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <figcaption>Me in Shibuya, the first day I arrived in Tokyo. </figcaption>
      </figure>
      <figure class="hb-polaroid">
        <div class="hb-shot">
          <svg viewBox="0 0 150 150" aria-hidden="true"><rect width="150" height="150" fill="#d6dde8"/><rect x="30" y="60" width="90" height="60" fill="#5a3e85" opacity=".45"/></svg>
          <img src="{{ base_path }}/images/hobbies/tokyo-2.jpeg" alt="Tokyo" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <figcaption>One of the many (!) dinner ramen</figcaption>
      </figure>
      <figure class="hb-polaroid">
        <div class="hb-shot">
          <svg viewBox="0 0 150 150" aria-hidden="true"><rect width="150" height="150" fill="#dfe8e0"/><path d="M0 110c40-30 70 10 150-20v60H0z" fill="#0e7c7b" opacity=".5"/></svg>
          <img src="{{ base_path }}/images/hobbies/tokyo-3.jpeg" alt="Tokyo" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <figcaption>Fushimi Inari-taisha</figcaption>
      </figure>
    </div>

    <ul class="hb-chips">
      <li>4 months in Tokyo</li>
      <li>2024</li>
      <li>Visiting research at NII</li>
      <li>Murakami, since high school</li>
    </ul>
  </div>

</div>



<script>
(function(){
  var root = document.querySelector('.hb');
  if(!root) return;

  var tabs = Array.prototype.slice.call(root.querySelectorAll('.hb-tab'));

  function fillMeters(panel){
    panel.querySelectorAll('.hb-bar i').forEach(function(bar){
      bar.style.width = '0';
      requestAnimationFrame(function(){
        requestAnimationFrame(function(){ bar.style.width = bar.dataset.fill + '%'; });
      });
    });
  }

  function select(tab){
    tabs.forEach(function(t){
      var panel = document.getElementById(t.getAttribute('aria-controls'));
      var on = (t === tab);
      t.setAttribute('aria-selected', on ? 'true' : 'false');
      t.tabIndex = on ? 0 : -1;
      panel.hidden = !on;
      if(on) fillMeters(panel);
    });
  }

  tabs.forEach(function(tab, i){
    tab.addEventListener('click', function(){ select(tab); });
    tab.addEventListener('keydown', function(e){
      var dir = e.key === 'ArrowRight' ? 1 : e.key === 'ArrowLeft' ? -1 : 0;
      if(!dir) return;
      e.preventDefault();
      var next = tabs[(i + dir + tabs.length) % tabs.length];
      select(next);
      next.focus();
    });
  });

  select(tabs[0]);

  var vinyl = root.querySelector('.hb-vinyl');
  var hint = root.querySelector('.hb-vinyl-hint');
  vinyl.addEventListener('click', function(){
    var spinning = vinyl.classList.toggle('is-spinning');
    vinyl.setAttribute('aria-pressed', spinning ? 'true' : 'false');
    hint.textContent = spinning ? 'Take Care, side A' : 'Tap the record';
  });
})();
</script>
