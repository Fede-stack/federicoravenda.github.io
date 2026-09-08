---
permalink: /
title: "👋 About Me"
excerpt: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a PhD candidate in Computer Science at Università della Svizzera italiana (USI) in Lugano, Switzerland, specializing in Natural Language Processing for Digital Health. I hold a Master's degree in Statistics from Università Milano-Bicocca, with expertise in probabilistic modeling and machine learning.


My research explores advanced NLP methods, with applications spanning mental health, Conversational AI, and Information Retrieval. Beyond NLP, I apply probabilistic deep learning techniques to time series analysis and engage in general machine learning research.

## 🧑‍💻 Research Interests

<style>
.ri{
  --ri-ink:#1c2b33;
  --ri-accent:#0e7c7b;
  --ri-line:rgba(28,43,51,.14);
  margin:0 0 1.8rem;
  display:grid;
  grid-template-columns:minmax(190px,240px) 1fr;
  gap:0;
  border:1px solid var(--ri-line);
  border-radius:10px;
  overflow:hidden;
  background:#fff;
}
.ri *{box-sizing:border-box;}
.ri-rail{
  display:flex;
  flex-direction:column;
  background:#f4f7f7;
  border-right:1px solid var(--ri-line);
}
.ri-tab{
  appearance:none;
  border:0;
  border-bottom:1px solid var(--ri-line);
  background:transparent;
  color:#41535d;
  text-align:left;
  font-size:.9rem;
  line-height:1.35;
  font-weight:600;
  padding:.85rem 1rem .85rem .9rem;
  cursor:pointer;
  border-left:3px solid transparent;
  transition:background .15s ease,color .15s ease,border-color .15s ease;
}
.ri-tab:last-child{border-bottom:0;}
.ri-tab:hover{background:#eaf0f0;color:var(--ri-ink);}
.ri-tab[aria-selected="true"]{
  background:#fff;
  color:var(--ri-ink);
  border-left-color:var(--ri-accent);
}
.ri-tab:focus-visible{outline:2px solid var(--ri-accent);outline-offset:-3px;}
.ri-panels{padding:1.3rem 1.4rem;}
.ri-panel[hidden]{display:none;}
.ri-panel h3{
  margin:0 0 .6rem;
  font-size:1.12rem;
  line-height:1.3;
  color:var(--ri-ink);
}
.ri-panel p{
  margin:0 0 1rem;
  font-size:.95rem;
  line-height:1.65;
  color:#3d4c56;
  max-width:66ch;
}
.ri-keys{
  list-style:none;
  display:flex;
  flex-wrap:wrap;
  gap:.4rem;
  margin:0;
  padding:0;
}
.ri-keys li{
  font-size:.78rem;
  color:#2f5d5c;
  background:rgba(14,124,123,.09);
  border-radius:999px;
  padding:.25rem .7rem;
}
@media (max-width:620px){
  .ri{grid-template-columns:1fr;}
  .ri-rail{flex-direction:row;flex-wrap:wrap;border-right:0;border-bottom:1px solid var(--ri-line);}
  .ri-tab{flex:1 1 45%;border-bottom:0;border-left:0;border-top:3px solid transparent;padding:.7rem .8rem;font-size:.82rem;}
  .ri-tab[aria-selected="true"]{border-left-color:transparent;border-top-color:var(--ri-accent);}
  .ri-panels{padding:1.1rem 1rem;}
}
@media (prefers-reduced-motion:reduce){.ri *{transition:none !important;}}
</style>

<div class="ri">
  <div class="ri-rail" role="tablist" aria-label="Research interests">
    <button class="ri-tab" id="ri-t1" role="tab" aria-controls="ri-p1" aria-selected="true">Understanding minds through language</button>
    <button class="ri-tab" id="ri-t2" role="tab" aria-controls="ri-p2" aria-selected="false" tabindex="-1">Trust, but verify</button>
    <button class="ri-tab" id="ri-t3" role="tab" aria-controls="ri-p3" aria-selected="false" tabindex="-1">Finding the needle in the haystack</button>
    <button class="ri-tab" id="ri-t4" role="tab" aria-controls="ri-p4" aria-selected="false" tabindex="-1">Good things come in small packages</button>
  </div>

  <div class="ri-panels">
    <div class="ri-panel" id="ri-p1" role="tabpanel" aria-labelledby="ri-t1">
      <h3>Understanding minds through language</h3>
      <p>Tailoring AI systems for automated screening and assessment of mental health conditions using digital data sources, including social media text and conversational interactions. My work applies psychological frameworks to design clinically relevant NLP systems that can identify behavioral patterns indicative of mental health disorders.</p>
      <ul class="ri-keys">
        <li>mental health screening</li>
        <li>social media text</li>
        <li>conversational data</li>
        <li>psychological frameworks</li>
      </ul>
    </div>

    <div class="ri-panel" id="ri-p2" role="tabpanel" aria-labelledby="ri-t2" hidden>
      <h3>Trust, but verify</h3>
      <p>Recently exploring interpretability methods and uncertainty quantification techniques to enhance the reliability and trustworthiness of large language models, with applications to clinical NLP.</p>
      <ul class="ri-keys">
        <li>interpretability</li>
        <li>uncertainty quantification</li>
        <li>clinical NLP</li>
      </ul>
    </div>

    <div class="ri-panel" id="ri-p3" role="tabpanel" aria-labelledby="ri-t3" hidden>
      <h3>Finding the needle in the haystack</h3>
      <p>Researching retrieval methods and ranking algorithms to improve access to relevant information in specialized domains. The aim is to develop effective search systems and explore retrieval-augmented generation techniques for knowledge-intensive applications.</p>
      <ul class="ri-keys">
        <li>information retrieval</li>
        <li>ranking</li>
        <li>retrieval-augmented generation</li>
      </ul>
    </div>

    <div class="ri-panel" id="ri-p4" role="tabpanel" aria-labelledby="ri-t4" hidden>
      <h3>Good things come in small packages</h3>
      <p>Investigating methods to improve the performance of small language models on clinically relevant diagnostic and assessment tasks. My research focuses on adapting and optimizing compact models through knowledge distillation, supervised fine-tuning, and reinforcement learning, with the goal of developing efficient models that can approach the diagnostic capabilities of larger systems while requiring substantially fewer computational resources.</p>
      <ul class="ri-keys">
        <li>small language models</li>
        <li>knowledge distillation</li>
        <li>supervised fine-tuning</li>
        <li>reinforcement learning</li>
      </ul>
    </div>
  </div>
</div>

<script>
(function(){
  var rail = document.querySelector('.ri-rail');
  if(!rail) return;
  var tabs = Array.prototype.slice.call(rail.querySelectorAll('.ri-tab'));

  function select(tab){
    tabs.forEach(function(t){
      var on = (t === tab);
      t.setAttribute('aria-selected', on ? 'true' : 'false');
      t.tabIndex = on ? 0 : -1;
      document.getElementById(t.getAttribute('aria-controls')).hidden = !on;
    });
  }

  tabs.forEach(function(tab, i){
    tab.addEventListener('click', function(){ select(tab); });
    tab.addEventListener('keydown', function(e){
      var dir = (e.key === 'ArrowDown' || e.key === 'ArrowRight') ? 1
              : (e.key === 'ArrowUp' || e.key === 'ArrowLeft') ? -1 : 0;
      if(!dir) return;
      e.preventDefault();
      var next = tabs[(i + dir + tabs.length) % tabs.length];
      select(next);
      next.focus();
    });
  });
})();
</script>

I've created a repository that I regularly update with available datasets from the literature for NLP research in Mental Health, intended for all practitioners. If you're interested, check out the following link: [[link]](https://github.com/Fede-stack/NLP-4-Mental-Health).

If you'd like to discuss any NLP-related topics, feel free to contact me at: 

*federico.ravenda [at] usi.ch* 

# Publications

* **The Changing Geometry of Grammar: Dimensionality and Neighborhood Reorganization across Transformer Layers**\
Samuele Vallisa*, Federico Ravenda*, Claudio Palominos, Rui He, Andrea Raballo, Antonietta Mira, Philipp Homan, Wolfram Hinzen \
[[paper]](https://arxiv.org/pdf/2608.25166)
*Submitted to *August 2026 ARR* *

* **TONY: an open-source TOolkit for Nlp in psYchology**\
Ravenda Federico, Ravenda Sofia Irene, Karpenko V., Montagnani, D., Mira, A., Raballo, A.  \
[[paper]](https://aclanthology.org/2026.acl-demo.65.pdf)
[Big News! 🤩] *Accepted as Main Paper at **Demo ACL 2026***

* **PersonalityDBench: A Dataset for Personality Disorders - from Modeling to Controlled Generation**\
Ravenda Federico, Bahrainian, S. A., Montagnani, D., Mira, A., Raballo, A.  \
[[paper]](https://aclanthology.org/2026.acl-long.1395.pdf)
[Big News! 🤩] *Accepted as Main Conference Paper at **ACL 2026***

* **A general framework for adaptive nonparametric dimensionality reduction**\
Di Noia, Antonio*, Federico Ravenda*, and Antonietta Mira. \
[[paper]](https://arxiv.org/pdf/2511.09486)
Accepted at Nature Scientific Reports\
*Nature Scientific Reports (2026).*

*  **Rethinking psychometrics through LLMs: how item semantics shape measurement and prediction in psychological questionnaires.**\
Ravenda, F., Preti, A., Poletti, M., Mira, A., & Raballo, A.\
[[paper]](https://www.nature.com/articles/s41598-025-21289-8)
*Nature Scientific Reports, 15(1), 37313, (2025).*

* **Navigating through the hidden embedding space: steering LLMs to improve mental health assessment**\
Ravenda, F., Bahrainian, S. A., Raballo, A., & Mira, A.\
[[paper]](https://arxiv.org/pdf/2510.16373)
*Accepted at SAC'2026*

* **Are llms effective psychological assessors? leveraging adaptive rag for interpretable mental health screening through psychometric practice**\
Ravenda, F., Bahrainian, S.A., Raballo, A., Mira, A., & Kando, N.  \
[[paper]](https://aclanthology.org/2025.acl-long.440/)
[Big News! 🤩] *Accepted as Main Conference Paper at **ACL 2025***

* **Diagnosing schizophrenia spectrum disorders: Large language models (LLMs) vs. leading international psychiatrists (LIPs)**\
Raballo, A., Ravenda, F., & Mira, A.\
[[paper]](https://pmc.ncbi.nlm.nih.gov/articles/PMC12405820/)
*Psychiatry and Clinical Neurosciences, 79(9), 599.*

* **From Evidence Mining to Meta-Prediction: a Gradient of Methodologies for Task-Specific Challenges in Psychological Assessment**\
Ravenda, F., Kara-Isitt, F. Z., Swift, S., Mira, A., & Raballo, A. \
[[paper]](https://aclanthology.org/2025.clpsych-1.3.pdf)
*Computational Linguistics and Clinical Psychology (**CLPsych 2025**)*

* **The emotional spectrum of llms: Leveraging empathy and emotion-based markers for mental health support**\
De Grandi, A.*, Ravenda, F.*, Raballo, A., & Crestani, F.  \
[[paper]](https://aclanthology.org/2025.clpsych-1.20.pdf)
*Computational Linguistics and Clinical Psychology (**CLPsych 2025**)*

* **Tailoring adaptive-zero-shot retrieval and probabilistic modelling for psychometric data**\ 
Ravenda, F., Bahrainian, S.A., Kando, N., Mira, A., Raballo, A., & Crestani, F.\
[[paper]](https://dl.acm.org/doi/10.1145/3672608.3707922)
*The 40th ACM/SIGAPP Symposium on Applied Computing (SAC '25)*, 2025

* **Transforming social media text into predictive tools for depression through AI: A test-case study on the Beck Depression Inventory-II.**\
Ravenda, F., Preti, A., Poletti, M., Mira, A., Crestani, F., & Raballo, A.\
[[paper]](https://journals.plos.org/digitalhealth/article?id=10.1371/journal.pdig.0000848)
*PLOS Digital Health, 4(6), e0000848.*

* **Zero-shot and efficient clarification need prediction**\
Lu, L., Meng, C., Ravenda, F., Aliannejadi, M., & Crestani, F.\
[[paper]](https://link.springer.com/chapter/10.1007/978-3-031-88708-6_25)
*European Conference of Information Retrieval, ECIR 2025*, 2025

* **A self-supervised seed-driven approach to topic modelling and clustering**\
Ravenda, F., Bahrainian, S.A., Raballo, A., Mira, A., & Crestani, F.\
[[paper]](https://link.springer.com/content/pdf/10.1007/s10844-024-00891-8.pdf)
*Journal of Intelligent Information Systems*, pages 1-21, 2024

* **A probabilistic spatio-temporal neural network to forecast covid-19 counts**\
Ravenda, F., Cesarini, M., Peluso, S., & Mira, A.\
[[paper]](https://link.springer.com/content/pdf/10.1007/s41060-024-00525-w.pdf)
*International Journal of Data Science and Analytics*, pages 1-8, 2024

* **Opinionated texts in social media: A proposal for evaluative judgement methodology**\   
Bączkowska, A., Negrea-Busuioc, E., Guzek, D., Liebeskind, C., Hess, A., Crestani, F., Ravenda, F., et al.\
[[paper]](https://repositorio.iscte-iul.pt/bitstream/10071/33093/1/article_108344)
*Beyond Philology An International Journal of Linguistics, Literary Studies and English Language Teaching*, pages 203-280, 2024

* **Spatio-temporal distribution, prediction and relationship of three major acute cardiovascular events: Out-of-hospital cardiac arrest, st-elevation myocardial infarction and stroke**\
Auricchio, A., Scquizzato, T., Ravenda, F., Cresta, R., Peluso, S., Caputo, M.L., Tonazzi, S., Benvenuti, C., & Mira, A.\
[[paper]](https://www.sciencedirect.com/science/article/pii/S2666520424002613)
*Resuscitation Plus*, volume 20, page 100810, 2024




