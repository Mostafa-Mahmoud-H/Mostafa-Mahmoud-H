
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: var(--font-mono); }
  .readme { max-width: 780px; margin: 0 auto; padding: 1rem 0.5rem; background: #0d1117; color: #c9d1d9; border-radius: var(--border-radius-lg); }
  .hero { background: linear-gradient(135deg, #000, #0a0f1c); padding: 2rem 1.5rem 1.5rem; border-radius: 12px 12px 0 0; text-align: center; border-bottom: 1px solid #00f2fe22; }
  .hero-name { font-size: 26px; font-weight: 700; color: #00f2fe; letter-spacing: 1px; }
  .hero-sub { font-size: 12px; color: #7ee8fa; margin-top: 4px; opacity: 0.8; }
  .typing { font-size: 12px; color: #00f2fe; margin-top: 10px; border: 1px solid #00f2fe33; padding: 4px 14px; border-radius: 20px; display: inline-block; }
  .section { padding: 1rem 1.25rem; border-bottom: 1px solid #161b22; }
  .section-title { font-size: 13px; font-weight: 700; color: #00f2fe; text-transform: uppercase; letter-spacing: 2px; margin-bottom: 14px; display: flex; align-items: center; gap: 8px; }
  .section-title::after { content: ''; flex: 1; height: 1px; background: linear-gradient(to right, #00f2fe33, transparent); }

  /* About */
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
  .about-item { background: #161b22; border: 1px solid #00f2fe22; border-radius: 8px; padding: 8px 12px; font-size: 11px; color: #8b949e; }
  .about-item span { color: #00f2fe; }

  /* Stats */
  .stats-row { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; }
  .stat-card { background: #161b22; border: 1px solid #21262d; border-radius: 8px; padding: 10px; text-align: center; }
  .stat-num { font-size: 20px; font-weight: 700; color: #00f2fe; }
  .stat-label { font-size: 10px; color: #6e7681; margin-top: 2px; }

  /* Trophy */
  .trophy-row { display: flex; flex-wrap: wrap; gap: 8px; }
  .trophy { background: #161b22; border: 1px solid #f0c040aa; border-radius: 8px; padding: 6px 12px; font-size: 11px; color: #f0c040; display: flex; align-items: center; gap: 6px; }
  .trophy i { font-size: 14px; }

  /* Skills */
  .skill-group { margin-bottom: 12px; }
  .skill-label { font-size: 11px; color: #8b949e; margin-bottom: 5px; display: flex; justify-content: space-between; }
  .skill-bar { height: 5px; background: #21262d; border-radius: 4px; overflow: hidden; }
  .skill-fill { height: 100%; border-radius: 4px; background: linear-gradient(to right, #00f2fe, #4facfe); }
  .tech-chips { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 10px; }
  .chip { background: #161b22; border: 1px solid #00f2fe33; border-radius: 6px; padding: 4px 10px; font-size: 10px; color: #00f2fe; }

  /* Projects */
  .project-card { background: #161b22; border: 1px solid #21262d; border-radius: 10px; padding: 14px; margin-bottom: 10px; position: relative; transition: border-color 0.2s; cursor: pointer; }
  .project-card:hover { border-color: #00f2fe55; }
  .project-card.featured { border-color: #00f2fe44; }
  .project-card.featured::before { content: 'FEATURED'; position: absolute; top: -1px; right: 14px; background: #00f2fe; color: #000; font-size: 9px; font-weight: 700; padding: 2px 8px; border-radius: 0 0 6px 6px; letter-spacing: 1px; }
  .proj-title { font-size: 14px; font-weight: 700; color: #58a6ff; margin-bottom: 4px; }
  .proj-desc { font-size: 11px; color: #8b949e; margin-bottom: 10px; line-height: 1.6; }
  .proj-tags { display: flex; gap: 6px; flex-wrap: wrap; margin-bottom: 8px; }
  .proj-tag { background: #0d1117; border: 1px solid #30363d; border-radius: 20px; padding: 2px 9px; font-size: 10px; color: #7ee8fa; }
  .proj-footer { display: flex; justify-content: space-between; align-items: center; }
  .proj-lang { font-size: 10px; color: #6e7681; display: flex; align-items: center; gap: 5px; }
  .lang-dot { width: 8px; height: 8px; border-radius: 50%; background: #3572A5; display: inline-block; }
  .proj-stats { display: flex; gap: 12px; font-size: 10px; color: #6e7681; }

  /* Contribution */
  .contrib-note { background: #161b22; border-radius: 8px; padding: 12px; font-size: 11px; color: #8b949e; text-align: center; border: 1px dashed #00f2fe22; }
  .contrib-preview { display: flex; gap: 3px; justify-content: center; margin-top: 10px; flex-wrap: wrap; }
  .contrib-cell { width: 12px; height: 12px; border-radius: 2px; }

  /* Contact */
  .contact-row { display: flex; gap: 8px; flex-wrap: wrap; }
  .contact-btn { background: #161b22; border: 1px solid #00f2fe44; border-radius: 8px; padding: 8px 14px; font-size: 11px; color: #00f2fe; display: flex; align-items: center; gap: 6px; text-decoration: none; cursor: pointer; }
  .contact-btn:hover { background: #00f2fe11; }
  .contact-btn i { font-size: 15px; }

  /* New additions */
  .quote-box { background: #0a0f1c; border-left: 3px solid #00f2fe; padding: 12px 16px; border-radius: 0 8px 8px 0; font-size: 12px; color: #8b949e; font-style: italic; }
  .quote-box strong { color: #00f2fe; font-style: normal; }
  .badge-new { background: #00f2fe22; border: 1px solid #00f2fe44; border-radius: 4px; padding: 1px 6px; font-size: 9px; color: #00f2fe; margin-left: 6px; }
  .streak-display { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; }
  .streak-item { background: #161b22; border: 1px solid #21262d; border-radius: 8px; padding: 10px; text-align: center; }
  .streak-val { font-size: 18px; font-weight: 700; color: #00f2fe; }
  .streak-lbl { font-size: 10px; color: #6e7681; margin-top: 2px; }

  .footer-area { padding: 1.5rem; text-align: center; }
  .final-line { font-size: 13px; color: #00f2fe; font-style: italic; letter-spacing: 0.5px; }
  .visitor-badge { display: inline-flex; align-items: center; gap: 6px; background: #161b22; border: 1px solid #21262d; border-radius: 20px; padding: 4px 12px; font-size: 10px; color: #6e7681; margin-top: 10px; }
</style>

<div class="readme">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-name">⬡ MOSTAFA MAHMOUD</div>
    <div class="hero-sub">AI Engineer • ML System Builder • Data Scientist</div>
    <div class="typing">&gt; Building Intelligent AI Systems_</div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-title">About</div>
    <div class="about-grid">
      <div class="about-item"><span>🎓</span> Alexandria National University — Data Science</div>
      <div class="about-item"><span>🔭</span> Building production-ready ML systems</div>
      <div class="about-item"><span>🧠</span> ML · NLP · Computer Vision · RecSys</div>
      <div class="about-item"><span>🏆</span> Competitive Programming background</div>
      <div class="about-item"><span>🚀</span> Streamlit · FastAPI · ML Pipelines</div>
      <div class="about-item"><span>📍</span> Alexandria, Egypt — Open to remote</div>
    </div>
    <div style="margin-top: 12px;">
      <div class="quote-box"><strong>"</strong> Engineering intelligence from dark data into real-world systems. <strong>"</strong></div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="section">
    <div class="section-title">GitHub Stats</div>
    <div class="stats-row">
      <div class="stat-card"><div class="stat-num">12+</div><div class="stat-label">Repositories</div></div>
      <div class="stat-card"><div class="stat-num">3</div><div class="stat-label">Stars Earned</div></div>
      <div class="stat-card"><div class="stat-num">150+</div><div class="stat-label">Contributions</div></div>
      <div class="stat-card"><div class="stat-num">2</div><div class="stat-label">Forks</div></div>
    </div>
    <div style="margin-top: 10px;">
      <div class="streak-display">
        <div class="streak-item"><div class="streak-val">🔥 14</div><div class="streak-lbl">Current streak (days)</div></div>
        <div class="streak-item"><div class="streak-val">📅 30</div><div class="streak-lbl">Longest streak</div></div>
        <div class="streak-item"><div class="streak-val">⭐ Top 10%</div><div class="streak-lbl">This month</div></div>
      </div>
    </div>
  </div>

  <!-- TROPHIES — NEW -->
  <div class="section">
    <div class="section-title">Achievements <span class="badge-new">NEW</span></div>
    <div class="trophy-row">
      <div class="trophy"><i class="ti ti-trophy" aria-hidden="true"></i> MultiLanguage</div>
      <div class="trophy"><i class="ti ti-trophy" aria-hidden="true"></i> Commits × 100</div>
      <div class="trophy"><i class="ti ti-trophy" aria-hidden="true"></i> PullRequest</div>
      <div class="trophy"><i class="ti ti-trophy" aria-hidden="true"></i> Repositories × 10</div>
      <div class="trophy"><i class="ti ti-trophy" aria-hidden="true"></i> Follower</div>
      <div class="trophy"><i class="ti ti-trophy" aria-hidden="true"></i> Experience</div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section">
    <div class="section-title">Tech Stack & Skills</div>
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px 24px;">
      <div class="skill-group">
        <div class="skill-label"><span>Python</span><span>95%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 95%"></div></div>
      </div>
      <div class="skill-group">
        <div class="skill-label"><span>Machine Learning</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 90%"></div></div>
      </div>
      <div class="skill-group">
        <div class="skill-label"><span>NLP</span><span>82%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 82%"></div></div>
      </div>
      <div class="skill-group">
        <div class="skill-label"><span>Computer Vision</span><span>78%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 78%"></div></div>
      </div>
      <div class="skill-group">
        <div class="skill-label"><span>SQL / Data Engineering</span><span>75%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 75%"></div></div>
      </div>
      <div class="skill-group">
        <div class="skill-label"><span>C++</span><span>70%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 70%"></div></div>
      </div>
    </div>
    <div class="tech-chips">
      <div class="chip">TensorFlow</div><div class="chip">PyTorch</div><div class="chip">Scikit-learn</div>
      <div class="chip">OpenCV</div><div class="chip">Pandas</div><div class="chip">NumPy</div>
      <div class="chip">Streamlit</div><div class="chip">FastAPI</div><div class="chip">Git</div>
      <div class="chip">Linux</div><div class="chip">Jupyter</div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-title">Featured Projects</div>

    <div class="project-card featured">
      <div class="proj-title">⚡ DiaPipeline — Production ML Framework</div>
      <div class="proj-desc">End-to-end ML pipeline covering preprocessing → feature engineering → training → evaluation → deployment. Built for real production use, not just Kaggle notebooks.</div>
      <div class="proj-tags">
        <span class="proj-tag">ML Pipelines</span>
        <span class="proj-tag">Python</span>
        <span class="proj-tag">Scikit-learn</span>
        <span class="proj-tag">Deployment</span>
      </div>
      <div class="proj-footer">
        <div class="proj-lang"><span class="lang-dot"></span> Python</div>
        <div class="proj-stats"><span>⭐ 0</span><span>🍴 0</span></div>
      </div>
    </div>

    <div class="project-card">
      <div class="proj-title">📰 Fake News Detector — Bilingual NLP</div>
      <div class="proj-desc">Arabic + English dual-language fake news detection using TF-IDF, classical ML models, and preprocessing pipelines for both RTL and LTR text.</div>
      <div class="proj-tags">
        <span class="proj-tag">NLP</span>
        <span class="proj-tag">Arabic</span>
        <span class="proj-tag">TF-IDF</span>
        <span class="proj-tag">Classification</span>
      </div>
      <div class="proj-footer">
        <div class="proj-lang"><span class="lang-dot"></span> Python</div>
        <div class="proj-stats"><span>⭐ 0</span><span>🍴 0</span></div>
      </div>
    </div>

    <div class="project-card">
      <div class="proj-title">❤️ Heart Disease Prediction System</div>
      <div class="proj-desc">Medical ML system with full EDA, feature selection, and multiple classification models. Focused on interpretability and clinical usability.</div>
      <div class="proj-tags">
        <span class="proj-tag">Healthcare ML</span>
        <span class="proj-tag">EDA</span>
        <span class="proj-tag">Classification</span>
        <span class="proj-tag">Streamlit</span>
      </div>
      <div class="proj-footer">
        <div class="proj-lang"><span class="lang-dot"></span> Python</div>
        <div class="proj-stats"><span>⭐ 0</span><span>🍴 0</span></div>
      </div>
    </div>
  </div>

  <!-- CONTRIBUTION SNAKE — NEW -->
  <div class="section">
    <div class="section-title">Contribution Activity</div>
    <div class="contrib-note">
      🐍 Snake animation + activity graph auto-generated via GitHub Actions
      <div class="contrib-preview" id="snake-preview"></div>
    </div>
  </div>

  <!-- CONTACT -->
  <div class="section">
    <div class="section-title">Contact</div>
    <div class="contact-row">
      <div class="contact-btn"><i class="ti ti-mail" aria-hidden="true"></i> Email</div>
      <div class="contact-btn"><i class="ti ti-brand-linkedin" aria-hidden="true"></i> LinkedIn</div>
      <div class="contact-btn"><i class="ti ti-brand-github" aria-hidden="true"></i> GitHub</div>
      <div class="contact-btn"><i class="ti ti-chart-bar" aria-hidden="true"></i> Kaggle</div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer-area">
    <div class="final-line">"Engineering intelligence from dark data into real-world systems."</div>
    <div class="visitor-badge"><i class="ti ti-eye" style="font-size:13px" aria-hidden="true"></i> Profile views tracked via shields.io</div>
  </div>

</div>

<script>
const preview = document.getElementById('snake-preview');
const colors = ['#0d1117','#0d1117','#0d1117','#003820','#006440','#00a060','#00f2fe'];
for(let i=0;i<63;i++){
  const cell = document.createElement('div');
  cell.className = 'contrib-cell';
  const w = Math.random();
  cell.style.background = w < 0.5 ? colors[0] : w < 0.65 ? colors[3] : w < 0.78 ? colors[4] : w < 0.9 ? colors[5] : colors[6];
  preview.appendChild(cell);
}
</script>
