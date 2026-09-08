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
.hb h2,.hb h3,.hb .hb-tab{
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
.hb-music{display:grid;grid-template-columns:230px 1fr;gap:1.8rem;align-items:start;}
.hb-player{position:relative;width:230px;}
.hb-turntable{
  position:relative;
  width:100%;
  aspect-ratio:1/1;
  background:0;
  border:0;
  padding:0;
  cursor:pointer;
  display:block;
}
.hb-turntable:focus-visible{outline:2px solid var(--plum);outline-offset:6px;border-radius:8px;}
.hb-disc{
  position:absolute;
  top:6%;
  left:0;
  width:88%;
  aspect-ratio:1/1;
  border-radius:50%;
  background:radial-gradient(circle at 50% 50%, #f3f0ea 0 11%, #5a3e85 11% 14%, #1a1420 14% 46%, #241b2c 46% 48%, #1a1420 48% 100%);
  box-shadow:0 6px 18px rgba(19,32,41,.3);
  transition:transform .55s cubic-bezier(.2,.75,.3,1);
  z-index:1;
}
.hb-disc::after{
  content:"";
  position:absolute;
  inset:0;
  border-radius:50%;
  background:repeating-radial-gradient(circle at 50% 50%,rgba(255,255,255,.05) 0 2px,transparent 2px 5px);
}
.hb-sleeve{
  position:relative;
  display:block;
  width:88%;
  aspect-ratio:1/1;
  background:#d9d4cc;
  border-radius:3px;
  overflow:hidden;
  box-shadow:0 4px 14px rgba(19,32,41,.28);
  z-index:2;
}
.hb-sleeve img{width:100%;height:100%;object-fit:cover;display:block;}
.hb-sleeve.is-empty img{display:none;}
.hb-sleeve.is-empty::after{
  content:"cover";
  position:absolute;
  inset:0;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:.8rem;
  color:#6d6459;
  letter-spacing:.08em;
}
.hb-player.is-playing .hb-disc{
  transform:translateX(38%);
  animation:hb-spin 3.2s linear infinite;
}
@keyframes hb-spin{to{transform:translateX(38%) rotate(360deg);}}
.hb-caption{
  display:block;
  margin-top:.7rem;
  font-size:.82rem;
  color:#5b6a73;
  line-height:1.4;
}
.hb-caption b{display:block;color:var(--ink);font-weight:700;font-size:.9rem;}
.hb-prose{margin:0;font-size:1.02rem;line-height:1.75;max-width:60ch;}
.hb-prose b{color:var(--accent);font-weight:700;}

/* ---------- tokyo ---------- */
.hb-skyline{
  display:block;width:100%;height:110px;
  margin-bottom:1.2rem;border-radius:10px;background:#101a2b;
}
.hb-polaroids{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
  gap:1rem;
  align-items:start;
  margin-bottom:.4rem;
}
.hb-polaroid{background:#fff;padding:.6rem .6rem 0;border-radius:6px;}
.hb-polaroid .hb-shot{aspect-ratio:auto;background:none;}
.hb-polaroid .hb-shot img{height:auto;object-fit:contain;}
.hb-polaroid .hb-shot svg{position:static;height:150px;}
.hb-polaroid figcaption{
  font-size:.8rem;color:#5b6a73;
  padding:.55rem .1rem .7rem;
}

@media (max-width:600px){
  .hb-hero h2{font-size:1.7rem;}
  .hb-music{grid-template-columns:1fr;justify-items:center;}
  .hb-player{width:200px;}
  .hb-prose{font-size:.98rem;}
}
@media (prefers-reduced-motion:reduce){
  .hb *{animation:none !important;transition:none !important;}
}
</style>

<div class="hb">

  <div class="hb-hero">
    <h2>Hobbies</h2>
    <p>I am now closer to 30 than to 20, which, as far as I can tell, is the ideal age to start two new sporting careers at once.</p>
    <div class="hb-tabs" role="tablist" aria-label="Things I do outside research">
      <button class="hb-tab" id="hb-tab-sport" role="tab" aria-controls="hb-panel-sport" aria-selected="true" style="--tab-color:#0e7c7b">🏄 Board &amp; rackets</button>
      <button class="hb-tab" id="hb-tab-music" role="tab" aria-controls="hb-panel-music" aria-selected="false" tabindex="-1" style="--tab-color:#5a3e85">🎧 On repeat</button>
      <button class="hb-tab" id="hb-tab-tokyo" role="tab" aria-controls="hb-panel-tokyo" aria-selected="false" tabindex="-1" style="--tab-color:#d93b70">🗼 Tokyo and Murakami</button>
    </div>
  </div>

  <!-- ============ SPORT ============ -->
  <div class="hb-panel" id="hb-panel-sport" role="tabpanel" aria-labelledby="hb-tab-sport" style="--accent:var(--sea)">
    <p class="hb-lead">I have reinvented myself as an <b>occasional, low-level surfer</b> and a padel player with a decent smash and a certain elegance at the net.</p>

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
          <p>A decent smash, and an elegant way of moving at the net that I stole from tennis. Still figuring out how to use the walls.</p>
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
    <div class="hb-music">
      <div class="hb-player" id="hb-player">
        <button class="hb-turntable" type="button" aria-pressed="false" aria-label="Play the record">
          <span class="hb-disc"></span>
          <span class="hb-sleeve">
            <img src="{{ base_path }}/images/hobbies/album.jpg" alt="Album cover" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
          </span>
        </button>
        <span class="hb-caption" id="hb-caption"><b>Take Care</b>Tap the cover</span>
      </div>
      <p class="hb-prose">I grew up on Aerosmith and the Red Hot Chili Peppers, played loud with my dad in his old Toyota Avensis. Somewhere around high school rock quietly gave way to <b>RnB and Hip Hop</b>, and it never really moved back. My favourite album is probably <em>Take Care</em> by Drake (honourable mentions to Nonostante Tutto by Gemitaiz - a skipless record and by far my favourite Italian album; Views by Drake - the soundtrack of my life across all seasons; Get Rich or Die Trying - the first album that comes to mind when I hear the word 'hip hop'; the 'College' trilogy by Kanye West - to boost my self-esteem; and Rated-R by Rihanna - one of the best pop albums of the 2000s).</p>
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

    <p class="hb-lead">I spent high school reading <b>Murakami</b> and picturing Japan. In 2024 I got the opportunity to live in Tokyo for four months as a visiting researcher at NII, and <b>the city is even better than the one I had imagined through Murakami's lens. </b></p>

    <div class="hb-polaroids">
      <figure class="hb-polaroid">
        <div class="hb-shot">
          <svg viewBox="0 0 150 150" aria-hidden="true"><rect width="150" height="150" fill="#e8d3dc"/><circle cx="75" cy="70" r="30" fill="#d93b70" opacity=".55"/></svg>
          <img src="{{ base_path }}/images/hobbies/tokyo-1.jpeg" alt="Shibuya crossing at night" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <figcaption>Me in Shibuya, the first day I arrived in Tokyo.</figcaption>
      </figure>
      <figure class="hb-polaroid">
        <div class="hb-shot">
          <svg viewBox="0 0 150 150" aria-hidden="true"><rect width="150" height="150" fill="#d6dde8"/><rect x="30" y="60" width="90" height="60" fill="#5a3e85" opacity=".45"/></svg>
          <img src="{{ base_path }}/images/hobbies/tokyo-2.jpeg" alt="A bowl of ramen" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <figcaption>One of the many (!) ramen dinners.</figcaption>
      </figure>
      <figure class="hb-polaroid">
        <div class="hb-shot">
          <svg viewBox="0 0 150 150" aria-hidden="true"><rect width="150" height="150" fill="#dfe8e0"/><path d="M0 110c40-30 70 10 150-20v60H0z" fill="#0e7c7b" opacity=".5"/></svg>
          <img src="{{ base_path }}/images/hobbies/tokyo-3.jpeg" alt="A temple" loading="lazy" onerror="this.parentNode.classList.add('is-empty')">
        </div>
        <figcaption>Fushimi Inari-taisha, Kyoto.</figcaption>
      </figure>
    </div>

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

  /* ---------- record player ---------- */
  var player = document.getElementById('hb-player');
  if(!player) return;
  var turntable = player.querySelector('.hb-turntable');
  var caption = document.getElementById('hb-caption');
  var audioCtx, crackleNode, gainNode;

  var track = new Audio('{{ base_path }}/files/audio/album.mp3');
  track.loop = true;
  track.preload = 'none';
  track.volume = 0.8;

  function startCrackle(){
    var Ctx = window.AudioContext || window.webkitAudioContext;
    if(!Ctx) return;
    if(!audioCtx) audioCtx = new Ctx();
    if(audioCtx.state === 'suspended') audioCtx.resume();

    var seconds = 2;
    var buffer = audioCtx.createBuffer(1, audioCtx.sampleRate * seconds, audioCtx.sampleRate);
    var data = buffer.getChannelData(0);
    for(var i = 0; i < data.length; i++){
      var hiss = (Math.random() * 2 - 1) * 0.035;
      var pop = Math.random() < 0.0004 ? (Math.random() * 2 - 1) * 0.7 : 0;
      data[i] = hiss + pop;
    }

    crackleNode = audioCtx.createBufferSource();
    crackleNode.buffer = buffer;
    crackleNode.loop = true;

    var filter = audioCtx.createBiquadFilter();
    filter.type = 'lowpass';
    filter.frequency.value = 3200;

    gainNode = audioCtx.createGain();
    gainNode.gain.setValueAtTime(0, audioCtx.currentTime);
    gainNode.gain.linearRampToValueAtTime(0.12, audioCtx.currentTime + 0.35);

    crackleNode.connect(filter).connect(gainNode).connect(audioCtx.destination);
    crackleNode.start();
  }

  function stopCrackle(){
    if(!crackleNode || !audioCtx) return;
    var node = crackleNode;
    gainNode.gain.linearRampToValueAtTime(0, audioCtx.currentTime + 0.25);
    setTimeout(function(){ try{ node.stop(); }catch(e){} }, 300);
    crackleNode = null;
  }

  turntable.addEventListener('click', function(){
    var playing = player.classList.toggle('is-playing');
    turntable.setAttribute('aria-pressed', playing ? 'true' : 'false');
    caption.innerHTML = playing
      ? '<b>Take Care</b>Side A, spinning'
      : '<b>Take Care</b>Tap the sleeve';
    if(playing){
      startCrackle();
      track.play().catch(function(){});
    } else {
      stopCrackle();
      track.pause();
      track.currentTime = 0;
    }
  });
})();
</script>
