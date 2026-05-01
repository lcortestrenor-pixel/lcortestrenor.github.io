<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>IMG × USTA × ESPN, The $2.04B Deal</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@300;400;500;600;700&family=DM+Serif+Display:ital@0;1&display=swap');

:root {
  --navy: #0a1628;
  --navy-mid: #152240;
  --blue: #1e3a6e;
  --blue-mid: #1a4fa0;
  --accent: #00c8ff;
  --accent2: #ffd166;
  --green: #00b894;
  --red: #e84b3a;
  --white: #ffffff;
  --off-white: #f0f4ff;
  --muted: #7a8ea8;
  --border: rgba(255,255,255,0.1);
  --card-bg: rgba(255,255,255,0.05);
  --card-border: rgba(0,200,255,0.2);
  --text: #e8f0ff;
  --text-dim: #a0b4cc;
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--navy);
  color: var(--text);
  line-height: 1.65;
  min-height: 100vh;
}

/* ===== HEADER ===== */
header {
  background: linear-gradient(135deg, var(--navy) 0%, var(--blue) 60%, #0d2a50 100%);
  padding: 60px 24px 40px;
  text-align: center;
  position: relative;
  overflow: hidden;
  border-bottom: 1px solid var(--card-border);
}
header::before {
  content: '';
  position: absolute;
  top: -80px; left: 50%;
  transform: translateX(-50%);
  width: 600px; height: 600px;
  background: radial-gradient(circle, rgba(0,200,255,0.08) 0%, transparent 70%);
  pointer-events: none;
}
.header-tag {
  display: inline-flex; align-items: center; gap: 8px;
  background: rgba(0,200,255,0.15);
  border: 1px solid rgba(0,200,255,0.3);
  color: var(--accent);
  font-size: 0.72em; letter-spacing: 3px; text-transform: uppercase;
  padding: 6px 20px; border-radius: 30px; margin-bottom: 20px;
  font-weight: 600;
}
.header-tag-dot { width:7px; height:7px; background:var(--accent); border-radius:50%; animation: pulse 2s infinite; }
@keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.3} }

header h1 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(2.5em, 6vw, 5em);
  letter-spacing: 4px;
  color: var(--white);
  line-height: 1;
  margin-bottom: 12px;
}
header h1 span { color: var(--accent); }
.header-sub {
  font-size: 0.92em;
  color: var(--text-dim);
  letter-spacing: 1px;
  margin-bottom: 28px;
}
.header-stats {
  display: flex;
  justify-content: center;
  gap: 32px;
  flex-wrap: wrap;
  margin-top: 24px;
}
.hstat {
  text-align: center;
  padding: 14px 24px;
  background: rgba(0,200,255,0.07);
  border: 1px solid rgba(0,200,255,0.2);
  border-radius: 12px;
  min-width: 130px;
}
.hstat-val {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2.2em;
  color: var(--accent);
  letter-spacing: 2px;
  display: block;
}
.hstat-lbl {
  font-size: 0.72em;
  color: var(--text-dim);
  letter-spacing: 1px;
  text-transform: uppercase;
}

/* ===== PROGRESS BAR ===== */
.progress-bar-wrap {
  background: var(--navy-mid);
  padding: 14px 24px;
  display: flex;
  align-items: center;
  gap: 20px;
  border-bottom: 1px solid var(--border);
}
.pb-label { font-size: 0.8em; color: var(--text-dim); white-space: nowrap; }
.pb-track {
  flex: 1;
  background: rgba(255,255,255,0.08);
  border-radius: 20px; height: 8px;
  overflow: hidden;
}
.pb-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  border-radius: 20px;
  width: 0%;
  transition: width 0.9s cubic-bezier(.4,0,.2,1);
}
.pb-pct { font-size: 0.82em; font-weight: 700; color: var(--accent); white-space: nowrap; }

/* ===== NAV ===== */
.nav-wrap {
  max-width: 1100px; margin: 0 auto;
  padding: 24px 24px 0;
}
.nav-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
}
.nav-btn {
  padding: 18px 14px;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: var(--card-bg);
  cursor: pointer;
  transition: all 0.3s;
  text-align: center;
  display: flex; flex-direction: column; align-items: center; gap: 6px;
  position: relative;
  overflow: hidden;
}
.nav-btn::before {
  content: '';
  position: absolute; bottom: 0; left: 0;
  width: 100%; height: 3px;
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.3s;
}
.nav-btn:hover { border-color: var(--accent); background: rgba(0,200,255,0.07); transform: translateY(-3px); }
.nav-btn:hover::before { transform: scaleX(1); }
.nav-btn.active { border-color: var(--accent); background: rgba(0,200,255,0.12); }
.nav-btn.active::before { transform: scaleX(1); }
.nav-icon { font-size: 1.6em; }
.nav-num { font-size: 0.7em; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); font-weight: 600; }
.nav-btn.active .nav-num { color: var(--accent); }
.nav-title { font-size: 0.86em; font-weight: 600; color: var(--text-dim); line-height: 1.3; }
.nav-btn.active .nav-title, .nav-btn:hover .nav-title { color: var(--text); }

/* ===== CONTAINER ===== */
.container { max-width: 1100px; margin: 0 auto; padding: 28px 24px 60px; }

/* ===== SECTIONS ===== */
.section { display: none; animation: fadeUp 0.45s ease; }
.section.active { display: block; }
@keyframes fadeUp { from{opacity:0;transform:translateY(16px)} to{opacity:1;transform:translateY(0)} }

/* ===== SECTION HEADER ===== */
.sec-header {
  display: flex; align-items: center; gap: 20px;
  background: rgba(255,255,255,0.04);
  border: 1px solid var(--card-border);
  border-radius: 16px;
  padding: 28px 32px;
  margin-bottom: 24px;
}
.sh-icon { font-size: 2.8em; flex-shrink: 0; }
.sh-text h2 {
  font-family: 'DM Serif Display', serif;
  font-size: 1.9em; font-weight: 400;
  color: var(--white);
  line-height: 1.2; margin-bottom: 4px;
}
.sh-text h2 em { font-style: italic; color: var(--accent); }
.sh-text p { color: var(--text-dim); font-size: 0.93em; }
.sh-badge {
  margin-left: auto; flex-shrink: 0;
  background: rgba(0,200,255,0.12);
  border: 1px solid rgba(0,200,255,0.3);
  color: var(--accent);
  padding: 8px 18px; border-radius: 30px;
  font-size: 0.8em; font-weight: 700;
  white-space: nowrap;
}

/* ===== GRIDS ===== */
.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin: 16px 0; }
.grid-3 { display: grid; grid-template-columns: repeat(3,1fr); gap: 16px; margin: 16px 0; }
.grid-auto { display: grid; grid-template-columns: repeat(auto-fit,minmax(220px,1fr)); gap: 16px; margin: 16px 0; }

/* ===== CARDS ===== */
.card {
  background: rgba(255,255,255,0.04);
  border: 1px solid var(--border);
  border-radius: 14px; padding: 22px;
  transition: all 0.3s;
  position: relative; overflow: hidden;
}
.card::after {
  content: '';
  position: absolute; bottom: 0; left: 0;
  width: 100%; height: 3px;
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.3s;
}
.card:hover { transform: translateY(-4px); border-color: var(--card-border); background: rgba(0,200,255,0.05); }
.card:hover::after { transform: scaleX(1); }
.card-icon { font-size: 2em; margin-bottom: 10px; }
.card h4 { font-size: 0.97em; font-weight: 700; color: var(--accent); margin-bottom: 8px; }
.card p { font-size: 0.9em; color: var(--text-dim); }
.card .card-stat { font-family: 'Bebas Neue', sans-serif; font-size: 2.2em; color: var(--accent2); letter-spacing: 2px; display: block; margin-bottom: 4px; }

/* ===== STAT HERO CARDS ===== */
.stat-hero {
  background: linear-gradient(135deg, rgba(0,200,255,0.1), rgba(0,200,255,0.04));
  border: 1px solid rgba(0,200,255,0.25);
  border-radius: 16px; padding: 28px;
  text-align: center;
}
.stat-hero .val {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 3.5em; color: var(--accent);
  letter-spacing: 3px; display: block; line-height: 1;
}
.stat-hero .val.gold { color: var(--accent2); }
.stat-hero .val.green { color: var(--green); }
.stat-hero .lbl { font-size: 0.82em; color: var(--text-dim); margin-top: 8px; letter-spacing: 1px; display: block; }

/* ===== ACCORDION / STEP CARDS ===== */
.steps-wrap { display: flex; flex-direction: column; gap: 12px; margin: 16px 0; }
.step-card {
  background: rgba(255,255,255,0.04);
  border: 1px solid var(--border);
  border-radius: 14px;
  display: flex; gap: 0;
  overflow: hidden; cursor: pointer;
  transition: all 0.25s;
}
.step-card:hover { border-color: var(--card-border); transform: translateX(4px); }
.step-num-col {
  min-width: 56px;
  background: rgba(0,200,255,0.15);
  color: var(--accent);
  display: flex; align-items: center; justify-content: center;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.6em; flex-shrink: 0;
  border-right: 1px solid var(--border);
}
.step-card.gold .step-num-col { background: rgba(255,209,102,0.15); color: var(--accent2); border-right-color: rgba(255,209,102,0.2); }
.step-card.green .step-num-col { background: rgba(0,184,148,0.15); color: var(--green); border-right-color: rgba(0,184,148,0.2); }
.step-card.red .step-num-col { background: rgba(232,75,58,0.15); color: var(--red); border-right-color: rgba(232,75,58,0.2); }
.step-content { padding: 18px 20px; flex: 1; }
.step-content h4 { font-size: 0.97em; font-weight: 700; color: var(--text); margin-bottom: 5px; }
.step-content p { font-size: 0.9em; color: var(--text-dim); }
.step-detail { max-height: 0; overflow: hidden; transition: max-height 0.45s ease; }
.step-card.open .step-detail { max-height: 600px; }
.step-detail-inner { padding-top: 12px; border-top: 1px solid var(--border); margin-top: 12px; }
.step-detail-inner ul { padding-left: 18px; }
.step-detail-inner li { font-size: 0.88em; color: var(--text-dim); margin-bottom: 6px; }
.step-expand {
  margin-left: auto; padding: 0 18px;
  color: var(--accent); font-size: 1.3em;
  transition: transform 0.3s; align-self: center; flex-shrink: 0;
}
.step-card.open .step-expand { transform: rotate(180deg); }

/* ===== QUOTE ===== */
.quote-block {
  background: rgba(0,200,255,0.06);
  border-left: 3px solid var(--accent);
  border-radius: 0 12px 12px 0;
  padding: 20px 24px;
  margin: 20px 0;
}
.quote-block blockquote {
  font-family: 'DM Serif Display', serif;
  font-size: 1.12em; font-style: italic;
  color: var(--text); line-height: 1.5;
  margin-bottom: 10px;
}
.quote-block cite { font-size: 0.82em; color: var(--accent); font-style: normal; font-weight: 600; }

/* ===== HIGHLIGHT BOXES ===== */
.hbox { border-radius: 12px; padding: 16px 20px; margin: 14px 0; font-size: 0.93em; }
.hbox-blue { background: rgba(0,200,255,0.07); border-left: 3px solid var(--accent); color: var(--text-dim); }
.hbox-gold { background: rgba(255,209,102,0.07); border-left: 3px solid var(--accent2); color: var(--text-dim); }
.hbox-green { background: rgba(0,184,148,0.07); border-left: 3px solid var(--green); color: var(--text-dim); }
.hbox-red { background: rgba(232,75,58,0.07); border-left: 3px solid var(--red); color: var(--text-dim); }
.hbox strong { display: block; margin-bottom: 5px; color: var(--text); }

/* ===== CHANNEL CARDS ===== */
.channel-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 14px; margin: 16px 0; }
.channel-card {
  background: rgba(255,255,255,0.04);
  border: 1px solid var(--border);
  border-radius: 14px; padding: 20px;
  text-align: center; transition: all 0.3s;
}
.channel-card:hover { border-color: var(--accent2); transform: translateY(-3px); background: rgba(255,209,102,0.05); }
.channel-card .ch-name { font-family: 'Bebas Neue', sans-serif; font-size: 1.4em; color: var(--accent2); letter-spacing: 2px; margin-bottom: 8px; }
.channel-card .ch-role { font-size: 0.83em; color: var(--text-dim); line-height: 1.4; }

/* ===== BAR CHART ===== */
.chart-wrap { background: rgba(255,255,255,0.03); border: 1px solid var(--border); border-radius: 14px; padding: 24px; margin: 16px 0; }
.chart-title { font-size: 0.85em; color: var(--text-dim); letter-spacing: 1px; text-transform: uppercase; margin-bottom: 20px; font-weight: 600; }
.chart-bars { display: flex; align-items: flex-end; gap: 18px; height: 140px; margin-bottom: 10px; }
.bar-col { flex: 1; display: flex; flex-direction: column; align-items: center; gap: 8px; height: 100%; justify-content: flex-end; }
.bar {
  width: 100%; border-radius: 6px 6px 0 0;
  transition: height 1.2s cubic-bezier(.4,0,.2,1);
  position: relative; cursor: pointer;
}
.bar:hover { filter: brightness(1.2); }
.bar-tooltip {
  position: absolute; bottom: 105%; left: 50%; transform: translateX(-50%);
  background: var(--navy-mid); border: 1px solid var(--card-border);
  color: var(--accent); font-size: 0.82em; font-weight: 700;
  padding: 4px 10px; border-radius: 8px; white-space: nowrap;
  pointer-events: none; opacity: 0; transition: opacity 0.2s;
}
.bar:hover .bar-tooltip { opacity: 1; }
.bar-lbl { font-size: 0.78em; color: var(--text-dim); font-weight: 600; }
.bar-val { font-size: 0.88em; color: var(--text); font-weight: 700; }
.chart-note { font-size: 0.78em; color: var(--muted); margin-top: 8px; font-style: italic; }

/* ===== MY TAKE ===== */
.my-take {
  background: linear-gradient(135deg, rgba(0,184,148,0.1), rgba(0,200,255,0.07));
  border: 1px solid rgba(0,184,148,0.25);
  border-radius: 16px; padding: 28px;
  margin: 20px 0;
  display: flex; gap: 20px; align-items: flex-start;
}
.mt-icon { font-size: 2.2em; flex-shrink: 0; }
.mt-text h4 { color: var(--green); font-size: 1.05em; font-weight: 700; margin-bottom: 10px; }
.mt-text p { font-size: 0.93em; color: var(--text-dim); line-height: 1.65; }

/* ===== QUIZ ===== */
.quiz-wrap { background: rgba(255,255,255,0.03); border: 1px solid var(--border); border-radius: 16px; padding: 32px; margin: 24px 0; }
.quiz-q { margin-bottom: 28px; }
.quiz-q:last-child { margin-bottom: 0; }
.quiz-q h4 { font-size: 1em; font-weight: 700; color: var(--text); margin-bottom: 16px; line-height: 1.4; }
.quiz-options { display: flex; flex-direction: column; gap: 10px; }
.quiz-opt {
  padding: 14px 18px;
  background: rgba(255,255,255,0.04);
  border: 1.5px solid transparent;
  border-color: rgba(255,255,255,0.08);
  border-radius: 10px; cursor: pointer;
  transition: all 0.2s;
  display: flex; align-items: center; gap: 14px;
  font-size: 0.93em; color: var(--text-dim);
}
.quiz-opt:hover { background: rgba(0,200,255,0.07); border-color: var(--accent); color: var(--text); }
.quiz-opt input { width: 16px; height: 16px; accent-color: var(--accent); cursor: pointer; flex-shrink: 0; }
.quiz-opt.correct { background: rgba(0,184,148,0.12); border-color: var(--green); color: var(--text); }
.quiz-opt.incorrect { background: rgba(232,75,58,0.1); border-color: var(--red); color: var(--text); }
.quiz-expl {
  display: none;
  background: rgba(255,255,255,0.04);
  border-radius: 10px; padding: 14px 18px;
  margin-top: 12px; font-size: 0.9em;
  animation: slideDown 0.3s;
}
.quiz-expl.show { display: block; }
@keyframes slideDown { from{opacity:0;transform:translateY(-6px)} to{opacity:1;transform:translateY(0)} }
.quiz-expl h5 { color: var(--green); margin-bottom: 6px; font-size: 0.88em; }
.quiz-expl p { color: var(--text-dim); line-height: 1.5; }
.quiz-divider {
  height: 1px; background: var(--border);
  margin: 24px 0;
}
.quiz-score-banner {
  background: linear-gradient(135deg, rgba(0,200,255,0.1), rgba(255,209,102,0.08));
  border: 1px solid rgba(0,200,255,0.2);
  border-radius: 12px; padding: 16px 22px;
  text-align: center; margin-top: 20px;
  display: none;
}
.quiz-score-banner.show { display: block; animation: fadeUp 0.4s; }
.quiz-score-banner .score-val { font-family: 'Bebas Neue', sans-serif; font-size: 2.5em; color: var(--accent2); letter-spacing: 2px; }
.quiz-score-banner p { font-size: 0.88em; color: var(--text-dim); margin-top: 4px; }
.quiz-btn {
  display: inline-flex; align-items: center; gap: 8px;
  margin-top: 20px; padding: 12px 28px;
  background: rgba(0,200,255,0.12);
  border: 1px solid rgba(0,200,255,0.3);
  border-radius: 30px; color: var(--accent);
  cursor: pointer; font-size: 0.92em; font-weight: 700;
  transition: all 0.3s; letter-spacing: 1px;
  font-family: 'DM Sans', sans-serif;
}
.quiz-btn:hover { background: rgba(0,200,255,0.2); transform: translateY(-2px); }

/* ===== TIMELINE ===== */
.timeline { display: flex; flex-direction: column; gap: 0; margin: 16px 0; position: relative; }
.timeline::before {
  content: '';
  position: absolute; left: 22px; top: 0; bottom: 0;
  width: 2px; background: linear-gradient(180deg, var(--accent), var(--accent2));
}
.tl-item { display: flex; gap: 24px; padding-bottom: 24px; position: relative; }
.tl-dot {
  width: 44px; height: 44px; border-radius: 50%;
  background: var(--navy-mid); border: 2px solid var(--accent);
  display: flex; align-items: center; justify-content: center;
  font-size: 1em; flex-shrink: 0; z-index: 1;
  transition: all 0.3s;
}
.tl-item:hover .tl-dot { background: rgba(0,200,255,0.15); transform: scale(1.1); }
.tl-item.gold .tl-dot { border-color: var(--accent2); }
.tl-item.green .tl-dot { border-color: var(--green); }
.tl-content { flex: 1; background: rgba(255,255,255,0.03); border: 1px solid var(--border); border-radius: 12px; padding: 16px 20px; margin-top: 4px; transition: all 0.3s; }
.tl-item:hover .tl-content { border-color: var(--card-border); }
.tl-year { font-family: 'Bebas Neue', sans-serif; font-size: 1.2em; color: var(--accent); letter-spacing: 2px; }
.tl-item.gold .tl-year { color: var(--accent2); }
.tl-item.green .tl-year { color: var(--green); }
.tl-content h4 { font-size: 0.95em; font-weight: 700; color: var(--text); margin: 4px 0; }
.tl-content p { font-size: 0.88em; color: var(--text-dim); }

/* ===== SOURCES ===== */
.sources-tag {
  font-size: 0.75em; color: var(--muted);
  margin-top: 16px; padding-top: 12px;
  border-top: 1px solid var(--border);
  line-height: 1.6;
}
.sources-tag strong { color: var(--text-dim); }

/* ===== IMPACT BOX ===== */
.impact-box {
  background: linear-gradient(135deg, rgba(0,200,255,0.08), rgba(255,209,102,0.05));
  border: 1px solid rgba(0,200,255,0.2);
  border-radius: 14px; padding: 22px 26px;
  margin: 16px 0;
}
.impact-box .impact-label {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 0.85em; letter-spacing: 3px;
  color: var(--accent); margin-bottom: 8px;
  display: flex; align-items: center; gap: 8px;
}
.impact-box .impact-label::after { content: ''; flex: 1; height: 1px; background: rgba(0,200,255,0.2); }
.impact-box p { font-size: 0.93em; color: var(--text-dim); line-height: 1.65; }

/* ===== RESPONSIVE ===== */
@media (max-width: 700px) {
  .grid-2, .grid-3 { grid-template-columns: 1fr; }
  .nav-grid { grid-template-columns: 1fr; }
  .sec-header { flex-direction: column; text-align: center; }
  .sh-badge { margin-left: 0; }
  header h1 { font-size: 2.2em; }
  .header-stats { gap: 12px; }
  .my-take { flex-direction: column; }
}

/* ===== FOOTER ===== */
footer {
  background: var(--navy-mid);
  border-top: 1px solid var(--border);
  padding: 28px 24px;
  text-align: center;
}
footer p { font-size: 0.82em; color: var(--muted); }
footer strong { color: var(--accent); }
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="header-tag">
    <span class="header-tag-dot"></span>
    IMG Graduate Scheme, Application Task
  </div>
  <h1>THE <span>US OPEN</span> DEAL</h1>
  <p class="header-sub">IMG × USTA × ESPN &nbsp;·&nbsp; A 12-Year US Open Media Rights Extension</p>
  <p style="font-size:0.82em;color:var(--muted)">Presented by Lupe Cortés</p>
  <div class="header-stats">
    <div class="hstat"><span class="hstat-val">$2.04B</span><span class="hstat-lbl">Total Deal Value</span></div>
    <div class="hstat"><span class="hstat-val">+127%</span><span class="hstat-lbl">Annual Value Growth</span></div>
    <div class="hstat"><span class="hstat-val">12</span><span class="hstat-lbl">Years (2026–2037)</span></div>
    <div class="hstat"><span class="hstat-val">260+</span><span class="hstat-lbl">Hours/Year Coverage</span></div>
  </div>
</header>

<!-- PROGRESS BAR -->
<div class="progress-bar-wrap">
  <span class="pb-label">Reading progress</span>
  <div class="pb-track"><div class="pb-fill" id="pb-fill"></div></div>
  <span class="pb-pct" id="pb-pct">0%</span>
</div>

<!-- NAV -->
<div class="nav-wrap">
  <div class="nav-grid">
    <div class="nav-btn active" id="btn-1" onclick="openSection(1)">
      <span class="nav-icon">🎾</span>
      <span class="nav-num">Section 01</span>
      <span class="nav-title">The Deal at a Glance</span>
    </div>
    <div class="nav-btn" id="btn-2" onclick="openSection(2)">
      <span class="nav-icon">📈</span>
      <span class="nav-num">Section 02</span>
      <span class="nav-title">Market Context</span>
    </div>
    <div class="nav-btn" id="btn-3" onclick="openSection(3)">
      <span class="nav-icon">🌍</span>
      <span class="nav-num">Section 03</span>
      <span class="nav-title">Bigger Than One Deal</span>
    </div>
  </div>
</div>

<!-- CONTAINER -->
<div class="container">

  <!-- ===== SECTION 1: THE DEAL ===== -->
  <div class="section active" id="section-1">
    <div class="sec-header">
      <span class="sh-icon">🎾</span>
      <div class="sh-text">
        <h2>The Deal at a <em>Glance</em></h2>
        <p>Starting 2026, ESPN's longest-ever tennis agreement, brokered by IMG</p>
      </div>
      <span class="sh-badge">🏆 Historic</span>
    </div>

    <!-- Stats grid -->
    <div class="grid-3">
      <div class="stat-hero">
        <span class="val">$2.04B</span>
        <span class="lbl">Total deal value over 12 years</span>
      </div>
      <div class="stat-hero">
        <span class="val gold">+127%</span>
        <span class="lbl">Annual value growth: $75M/yr → $170M/yr</span>
      </div>
      <div class="stat-hero">
        <span class="val green">260+</span>
        <span class="lbl">Hours of US coverage per year</span>
      </div>
    </div>

    <!-- Quote -->
    <div class="quote-block">
      <blockquote>"This deal is groundbreaking, not only for the USTA and US Open, but for tennis globally."</blockquote>
      <cite>Hillary Mandel, EVP & Head of Americas Media, IMG</cite>
    </div>

    <!-- What is the deal -->
    <div class="hbox hbox-blue">
      <strong>What is the deal?</strong>
      Starting in 2026, ESPN and the USTA announced a 12-year extension keeping the US Open on ESPN through 2037, the longest tennis deal in ESPN history. The USTA takes over as host broadcaster, gaining full control of production and storytelling, while ESPN focuses entirely on maximising distribution across broadcast, cable, and streaming. The deal was brokered by IMG, the USTA's exclusive media rights representative.
    </div>

    <!-- Why it stood out -->
    <div class="my-take">
      <span class="mt-icon">💡</span>
      <div class="mt-text">
        <h4>Why This Deal Stood Out To Me</h4>
        <p>I have been passionate about tennis for as long as I can remember and I try to follow the business of the sport as closely as the sport itself. This deal stood out because it goes beyond price: IMG extracted a <strong style="color:var(--accent)">127% uplift</strong> by rebuilding the architecture of the deal entirely. Giving the USTA creative control of its own event production is a shift no US Grand Slam had attempted before, and it changes what future deals could look like across the entire sport.</p>
      </div>
    </div>

    <!-- Key components accordion -->
    <h3 style="font-size:1em;font-weight:700;color:var(--text-dim);letter-spacing:2px;text-transform:uppercase;margin:28px 0 14px;">Key Components, Click to Expand</h3>
    <div class="steps-wrap">
      <div class="step-card" onclick="toggleStep(this)">
        <div class="step-num-col">01</div>
        <div class="step-content">
          <h4>12-Year Extension, 2026–2037</h4>
          <p>ESPN's longest-ever tennis deal, a record by both duration and value.</p>
          <div class="step-detail">
            <div class="step-detail-inner">
              <ul>
                <li>Announced as a joint ESPN/USTA press release in 2024</li>
                <li>Replaces the previous deal valued at ~$75M/year (signed 2013)</li>
                <li>New annual value: $170M/yr, a 127% increase over one decade</li>
                <li>Brokered exclusively by IMG on behalf of the USTA</li>
              </ul>
            </div>
          </div>
        </div>
        <span class="step-expand">▾</span>
      </div>

      <div class="step-card gold" onclick="toggleStep(this)">
        <div class="step-num-col">02</div>
        <div class="step-content">
          <h4>USTA Becomes Host Broadcaster</h4>
          <p>A structural first for a Grand Slam in the United States, creative control returns to the event owner.</p>
          <div class="step-detail">
            <div class="step-detail-inner">
              <ul>
                <li>USTA takes over production from 2026, replacing ESPN's production role</li>
                <li>Mirrors the IOC/OBS model (Olympics) and UEFA model (Champions League), now imported into American tennis for the first time</li>
                <li>USTA is already trialling HBS + Red Cinema cameras and AI player audio ISOs</li>
                <li>Enables the USTA to own and monetise its own story and archive</li>
              </ul>
            </div>
          </div>
        </div>
        <span class="step-expand">▾</span>
      </div>

      <div class="step-card green" onclick="toggleStep(this)">
        <div class="step-num-col">03</div>
        <div class="step-content">
          <h4>Omnichannel by Design</h4>
          <p>Four platforms, every audience, broadcast, cable, streaming, and Spanish-language all covered.</p>
          <div class="step-detail">
            <div class="step-detail-inner">
              <p style="font-size:0.9em;color:var(--text-dim);margin-bottom:10px;">Rather than concentrating coverage on one platform, IMG structured the deal to reach every possible audience simultaneously, maximising both viewership and ad revenue, and giving ESPN full justification for the $170M/year price tag.</p>
            </div>
          </div>
        </div>
        <span class="step-expand">▾</span>
      </div>
    </div>

    <div class="sources-tag">
      <strong>Sources:</strong> IMG Press Release · ESPN Press Room · Sportcal · The Athletic · USTA 2024
    </div>
  </div>

  <!-- ===== SECTION 2: MARKET CONTEXT ===== -->
  <div class="section" id="section-2">
    <div class="sec-header">
      <span class="sh-icon">📈</span>
      <div class="sh-text">
        <h2>Market Context <em>Around the Deal</em></h2>
        <p>How the $2.04B deal reflects where the sports media market is heading</p>
      </div>
      <span class="sh-badge">Market Analysis</span>
    </div>

    <!-- Rights value chart -->
    <div class="chart-wrap">
      <div class="chart-title">US Open Annual Rights Value, IMG-Brokered ($M / year)</div>
      <div class="chart-bars" id="chart-bars">
        <div class="bar-col">
          <div class="bar" style="background:rgba(0,200,255,0.35);height:0%" data-target="44%" data-val="$75M">
            <div class="bar-tooltip">$75M / yr</div>
          </div>
          <span class="bar-lbl">2013</span>
          <span class="bar-val">$75M</span>
        </div>
        <div class="bar-col">
          <div class="bar" style="background:linear-gradient(180deg,var(--accent2),var(--accent));height:0%" data-target="100%" data-val="$170M">
            <div class="bar-tooltip">$170M / yr</div>
          </div>
          <span class="bar-lbl">2026+</span>
          <span class="bar-val" style="color:var(--accent2)">$170M</span>
        </div>
      </div>
      <div class="chart-note">+127% total annual value increase over one decade. Source: Market Intelligence / IMG Press Release</div>
    </div>

    <!-- 3 market trends accordion -->
    <h3 style="font-size:1em;font-weight:700;color:var(--text-dim);letter-spacing:2px;text-transform:uppercase;margin:28px 0 14px;">Three Market Trends That Drove This Deal</h3>
    <div class="steps-wrap">
      <div class="step-card" onclick="toggleStep(this)">
        <div class="step-num-col">🌐</div>
        <div class="step-content">
          <h4>Global Sports Rights Market: $55.3B → $102.8B by 2033</h4>
          <p>CAGR of 7.1%, IMG timed the USTA renewal at peak market momentum.</p>
          <div class="step-detail">
            <div class="step-detail-inner">
              <p style="font-size:0.9em;color:var(--text-dim);margin-bottom:10px;">As rights values double industry-wide, IMG strategically closed a 12-year deal before further inflation could make the numbers even more eye-watering for ESPN. Locking in $170M/year now reflects savvy timing, and deep market knowledge that IMG is uniquely positioned to have.</p>
              <div class="hbox hbox-blue" style="margin:0">
                <strong>IMG's Role</strong>
                Closing a long-term deal when the market is hot means maximum leverage. A shorter-term deal at this moment would have invited competitive bidding from tech giants at the next renegotiation.
              </div>
            </div>
          </div>
        </div>
        <span class="step-expand">▾</span>
      </div>

      <div class="step-card gold" onclick="toggleStep(this)">
        <div class="step-num-col">📱</div>
        <div class="step-content">
          <h4>Live Sports Streaming: $28.6B (2025) → $98.4B by 2034</h4>
          <p>CAGR of 14.7%, the fastest-growing segment in sports media.</p>
          <div class="step-detail">
            <div class="step-detail-inner">
              <p style="font-size:0.9em;color:var(--text-dim);margin-bottom:10px;">IMG expanded ESPN+ rights into this deal deliberately, streaming is where the growth is. The all-courts coverage on ESPN+ is a direct play on this trend, providing fans deeper access than ever before and making the package more valuable for both sides of the table.</p>
              <div class="hbox hbox-gold" style="margin:0">
                <strong>Key Insight</strong>
                The ESPN+ inclusion isn't just about more coverage, it's a hedge against cord-cutting. Digital streaming rights are where future value will concentrate.
              </div>
            </div>
          </div>
        </div>
        <span class="step-expand">▾</span>
      </div>

      <div class="step-card red" onclick="toggleStep(this)">
        <div class="step-num-col">🏈</div>
        <div class="step-content">
          <h4>US Sports Rights: $29.25B in 2025, projected $37B+ by 2030</h4>
          <p>Tech giants bidding aggressively, creating competitive tension that IMG leveraged.</p>
          <div class="step-detail">
            <div class="step-detail-inner">
              <p style="font-size:0.9em;color:var(--text-dim);margin-bottom:10px;">Apple, Amazon, and Google are now active bidders for live sport, forcing traditional broadcasters like ESPN to compete hard for anchor content. The US Open is exactly that kind of property. IMG understood this and drove ESPN to $170M/year by exploiting competitive pressure from the tech giants.</p>
            </div>
          </div>
        </div>
        <span class="step-expand">▾</span>
      </div>
    </div>

    <!-- Stats row -->
    <div class="grid-3" style="margin-top:24px">
      <div class="card">
        <div class="card-icon">🌍</div>
        <h4>Global Rights Market</h4>
        <span class="card-stat">7.1%</span>
        <p>CAGR through 2033. From $55.3B to $102.8B, a near doubling of the market.</p>
      </div>
      <div class="card">
        <div class="card-icon">📺</div>
        <h4>Live Streaming Growth</h4>
        <span class="card-stat" style="color:var(--accent2)">14.7%</span>
        <p>CAGR through 2034. Fastest-growing segment, from $28.6B to $98.4B.</p>
      </div>
      <div class="card">
        <div class="card-icon">🇺🇸</div>
        <h4>US Sports Rights</h4>
        <span class="card-stat" style="color:var(--green)">$37B+</span>
        <p>Projected by 2030, up from $29.25B in 2025. Tech competition driving inflation.</p>
      </div>
    </div>

    <div class="sources-tag">
      <strong>Sources:</strong> Market Intelo · S&P Global · SportBusiness · Front Office Sports · ESPN Press Room · Sportcal · Variety
    </div>
  </div>

  <!-- ===== SECTION 3: BIGGER THAN ONE DEAL ===== -->
  <div class="section" id="section-3">
    <div class="sec-header">
      <span class="sh-icon">🌍</span>
      <div class="sh-text">
        <h2>Bigger Than <em>One Deal</em></h2>
        <p>Industry impact, global precedent & personal perspective</p>
      </div>
      <span class="sh-badge">Industry Impact</span>
    </div>

    <!-- 3 pillars accordion -->
    <h3 style="font-size:1em;font-weight:700;color:var(--text-dim);letter-spacing:2px;text-transform:uppercase;margin:0 0 14px;">Three Structural Innovations</h3>

    <style>
    .innovation-card {
      position: relative; overflow: hidden;
      border-radius: 18px; margin-bottom: 16px;
      cursor: pointer; transition: all 0.35s cubic-bezier(.4,0,.2,1);
    }
    .innovation-card:hover { transform: translateY(-4px); }
    .innovation-card .inno-bg {
      position: absolute; inset: 0;
      opacity: 0.06; pointer-events: none;
      font-family: 'Bebas Neue', sans-serif;
      font-size: 9em; font-weight: 900;
      display: flex; align-items: center; justify-content: flex-end;
      padding-right: 20px; letter-spacing: -4px; line-height: 1;
      overflow: hidden; user-select: none;
    }
    .innovation-card .inno-inner {
      position: relative;
      padding: 26px 28px;
      border: 1px solid var(--border);
      border-radius: 18px;
      transition: border-color 0.3s;
    }
    .innovation-card:hover .inno-inner { border-color: var(--card-border); }
    .inno-num {
      font-family: 'DM Sans', sans-serif;
      font-size: 0.72em; letter-spacing: 4px; font-weight: 700; text-transform: uppercase;
      margin-bottom: 10px; display: flex; align-items: center; gap: 10px;
    }
    .inno-num::after { content: ''; flex: 1; height: 1px; background: currentColor; opacity: 0.2; }
    .inno-title {
      font-family: 'DM Sans', sans-serif;
      font-size: 1.1em; line-height: 1.3; font-weight: 700;
      color: var(--white); margin-bottom: 10px;
    }
    .inno-subtitle { font-size: 0.88em; color: var(--text-dim); margin-bottom: 16px; }
    .inno-detail { max-height: 0; overflow: hidden; transition: max-height 0.45s ease; }
    .innovation-card.open .inno-detail { max-height: 800px; }
    .inno-detail-inner { padding-top: 16px; border-top: 1px solid var(--border); margin-top: 4px; }
    .inno-detail-inner ul { padding-left: 18px; }
    .inno-detail-inner li { font-size: 0.88em; color: var(--text-dim); margin-bottom: 7px; line-height: 1.5; }
    .inno-expand { font-size: 0.8em; color: var(--accent); letter-spacing: 1px; font-weight: 600; display: flex; align-items: center; gap: 6px; }
    .inno-expand-icon { transition: transform 0.3s; display: inline-block; }
    .innovation-card.open .inno-expand-icon { transform: rotate(180deg); }
    /* card colours */
    .inno-1 .inno-inner { background: linear-gradient(135deg, rgba(0,200,255,0.07) 0%, rgba(10,22,40,0.6) 100%); }
    .inno-1 .inno-num { color: var(--accent); }
    .inno-1 .inno-bg { color: var(--accent); }
    .inno-2 .inno-inner { background: linear-gradient(135deg, rgba(255,209,102,0.07) 0%, rgba(10,22,40,0.6) 100%); }
    .inno-2 .inno-num { color: var(--accent2); }
    .inno-2 .inno-bg { color: var(--accent2); }
    .inno-3 .inno-inner { background: linear-gradient(135deg, rgba(0,184,148,0.07) 0%, rgba(10,22,40,0.6) 100%); }
    .inno-3 .inno-num { color: var(--green); }
    .inno-3 .inno-bg { color: var(--green); }
    </style>

    <div class="innovation-card inno-1" onclick="this.classList.toggle('open')">
      <div class="inno-bg">01</div>
      <div class="inno-inner">
        <div class="inno-num">Innovation 01</div>
        <div class="inno-title">Rights + Production Control, A Structural First</div>
        <div class="inno-subtitle">For the first time in US tennis, the event owner controls its own story.</div>
        <div class="inno-detail">
          <div class="inno-detail-inner">
            <p style="font-size:0.9em;color:var(--text-dim);margin-bottom:12px;">IMG imported the IOC/OBS and UEFA model into American tennis, separating rights ownership from production for the first time in the US. It gives the USTA the power to tell its own story, build its own archive, and monetise its IP independently.</p>
            <ul>
              <li><strong>Previously:</strong> ESPN controlled production and narrative</li>
              <li><strong>From 2026:</strong> USTA runs its own production (HBS, Red Cinema cameras, AI player audio ISOs)</li>
              <li><strong>ESPN role</strong> shifts to pure distribution maximisation</li>
              <li><strong>The model has proven transformative</strong> in European football and the Olympics</li>
            </ul>
          </div>
        </div>
        <div class="inno-expand">Expand <span class="inno-expand-icon">▾</span></div>
      </div>
    </div>

    <div class="innovation-card inno-2" onclick="this.classList.toggle('open')">
      <div class="inno-bg">02</div>
      <div class="inno-inner">
        <div class="inno-num">Innovation 02</div>
        <div class="inno-title">Omnichannel by Design, Maximum Reach Architecture</div>
        <div class="inno-subtitle">Four platforms working in concert: ABC, ESPN+, ESPN2, and Deportes.</div>
        <div class="inno-detail">
          <div class="inno-detail-inner">
            <p style="font-size:0.9em;color:var(--text-dim);margin-bottom:12px;">Rather than concentrating coverage on one platform, IMG structured the deal to reach every possible audience simultaneously. This maximises both viewership and ad revenue, and gives ESPN full justification for the $170M/year price tag.</p>
            <div class="channel-grid" style="margin-top:12px">
              <div class="channel-card"><div class="ch-name">ABC</div><div class="ch-role">Finals & Middle Sunday · Mass reach</div></div>
              <div class="channel-card"><div class="ch-name">ESPN+</div><div class="ch-role">All courts · Streaming anchor</div></div>
              <div class="channel-card"><div class="ch-name">ESPN2</div><div class="ch-role">Fan Week · Pre-tournament</div></div>
              <div class="channel-card"><div class="ch-name">Deportes</div><div class="ch-role">Spanish-language US exclusive</div></div>
            </div>
          </div>
        </div>
        <div class="inno-expand">Expand <span class="inno-expand-icon">▾</span></div>
      </div>
    </div>

    <div class="innovation-card inno-3" onclick="this.classList.toggle('open')">
      <div class="inno-bg">03</div>
      <div class="inno-inner">
        <div class="inno-num">Innovation 03</div>
        <div class="inno-title">Gender Equality as a Commercial Asset</div>
        <div class="inno-subtitle">WTA reached 1.1B+ viewers globally (+10% YoY), women's sport is now a valuation driver.</div>
        <div class="inno-detail">
          <div class="inno-detail-inner">
            <p style="font-size:0.9em;color:var(--text-dim);margin-bottom:12px;">Tennis rights can now command NFL-tier deal architecture. The US Open's legacy of equal prize money to men and women since 1973 has become a genuine commercial asset.</p>
            <div class="hbox hbox-green" style="margin:8px 0">
              <strong>ESPN Chairman's Framing</strong>
              Jimmy Pitaro publicly cited the US Open's gender equality legacy in justifying the $2.04B deal, framing it as proof of Disney's commitment to women's sports. That's not just PR, it's a signal that gender equity in sport is now a valuation driver.
            </div>
            <ul>
              <li>WTA: 1.1B+ global viewers, +10% year-over-year</li>
              <li>Equal prize money since 1973, a commercial differentiator in 2024</li>
              <li>Women's sport is now a financial argument, not a charity consideration</li>
            </ul>
          </div>
        </div>
        <div class="inno-expand">Expand <span class="inno-expand-icon">▾</span></div>
      </div>
    </div>

    <!-- Timeline: What happens next -->
    <h3 style="font-size:1em;font-weight:700;color:var(--text-dim);letter-spacing:2px;text-transform:uppercase;margin:32px 0 14px;">What Comes Next, The Ripple Effect</h3>
    <div class="timeline">
      <div class="tl-item">
        <div class="tl-dot">🎾</div>
        <div class="tl-content">
          <span class="tl-year">2026</span>
          <h4>US Open New Era Begins</h4>
          <p>USTA takes over as host broadcaster. New production model launches with HBS cameras and AI audio ISOs. ESPN distributes across all four platforms.</p>
        </div>
      </div>
      <div class="tl-item gold">
        <div class="tl-dot">⚖️</div>
        <div class="tl-content">
          <span class="tl-year">2027</span>
          <h4>Wimbledon: BBC Deal Renegotiation</h4>
          <p>Wimbledon's deal with BBC comes up for renegotiation. Every Grand Slam without a renegotiated deal now faces the question: who controls production? The USTA model changes the entire negotiating table.</p>
        </div>
      </div>
      <div class="tl-item green">
        <div class="tl-dot">🇫🇷</div>
        <div class="tl-content">
          <span class="tl-year">Now</span>
          <h4>Roland Garros: Deal with Warner Bros. Discovery</h4>
          <p>Roland Garros has just entered into a deal with Warner Bros. Discovery. These deals are alive right now, and the structural questions IMG raised at the US Open are now front and centre at Roland Garros too.</p>
        </div>
      </div>
    </div>

    <!-- My personal take -->
    <div class="my-take">
      <span class="mt-icon">🎾</span>
      <div class="mt-text">
        <h4>My Take, Why This Changes Everything</h4>
        <p>IMG didn't negotiate a better deal, it negotiated a <strong style="color:var(--accent)">structurally different one</strong>. By separating host broadcasting from distribution for the first time in US tennis, IMG ensured that the USTA owns its story and ESPN maximises its reach. The question for every future Grand Slam deal is no longer "who pays more?", it's "who controls what?" Wimbledon renegotiates with the BBC in 2027. Roland Garros has just entered into a live deal with Warner Bros. Discovery. Both now face that question directly. As for the fans, it means the US Open can finally tell its own story, on its own terms.</p>
      </div>
    </div>

    <div class="sources-tag">
      <strong>Sources:</strong> ESPN Press Room · IMG.com · Sports Video Group · SportBusiness · Perfect Tennis · CBS News · Market Intelo · Variety · USTA 2024
    </div>
  </div>

</div>

<!-- FOOTER -->
<footer>
  <p>Lupe Cortés · IMG Graduate Scheme Application Task · <strong>IMG × USTA × ESPN, The $2.04B Deal</strong></p>
  <p style="margin-top:6px;font-size:0.75em">Sources: IMG Press Release · ESPN Press Room · Sportcal · The Athletic · Market Intelo · S&P Global · SportBusiness · Front Office Sports · Variety · USTA 2024</p>
</footer>

<script>
// ===== SECTION NAV =====
function openSection(n) {
  for (let i = 1; i <= 3; i++) {
    document.getElementById('section-' + i).classList.toggle('active', i === n);
    document.getElementById('btn-' + i).classList.toggle('active', i === n);
  }
  updateProgress(n);
}

// ===== PROGRESS BAR =====
function updateProgress(n) {
  const pct = Math.round((n / 3) * 100);
  document.getElementById('pb-fill').style.width = pct + '%';
  document.getElementById('pb-pct').textContent = pct + '%';
}
updateProgress(1);

// ===== STEP ACCORDION =====
function toggleStep(el) {
  el.classList.toggle('open');
}

// ===== QUIZ =====
let answers = {};
function checkQ(qid, correct, explanation) {
  const opts = document.querySelectorAll('#' + qid + ' .quiz-opt');
  const radios = document.querySelectorAll('input[name="' + qid + '"]');
  let chosen = '';
  radios.forEach(r => { if (r.checked) chosen = r.value; });

  opts.forEach(opt => {
    const inp = opt.querySelector('input');
    if (inp.value === correct) opt.classList.add('correct');
    else if (inp.checked) opt.classList.add('incorrect');
    inp.disabled = true;
  });

  const expl = document.getElementById('expl-' + qid);
  const isCorrect = chosen === correct;
  expl.innerHTML = '<h5>' + (isCorrect ? '✅ Correct!' : '❌ Not quite') + '</h5><p>' + explanation + '</p>';
  expl.style.borderLeft = '3px solid ' + (isCorrect ? 'var(--green)' : 'var(--red)');
  expl.style.background = isCorrect ? 'rgba(0,184,148,0.08)' : 'rgba(232,75,58,0.08)';
  expl.classList.add('show');

  answers[qid] = isCorrect;
  updateScore();
}

function updateScore() {
  const total = Object.keys(answers).length;
  const correct = Object.values(answers).filter(Boolean).length;
  const banner = document.getElementById('quiz-score');
  document.getElementById('score-val').textContent = correct + '/' + total;
  const msgs = ['Keep going, more questions above!', 'Getting there! Review the sections above.', 'Solid, nearly there!', 'Almost perfect!', '🏆 Perfect score! You clearly follow the business of tennis.'];
  document.getElementById('score-msg').textContent = total < 4 ? 'Answer all 4 questions to complete.' : msgs[correct];
  if (total === 4) banner.classList.add('show');
}

// ===== CHART ANIMATION =====
function animateChart() {
  const bars = document.querySelectorAll('.bar');
  bars.forEach((bar, i) => {
    setTimeout(() => {
      bar.style.height = bar.getAttribute('data-target');
    }, i * 180);
  });
}

const obs = new IntersectionObserver((entries) => {
  entries.forEach(e => { if (e.isIntersecting) { animateChart(); obs.disconnect(); } });
}, { threshold: 0.3 });
const chartEl = document.getElementById('chart-bars');
if (chartEl) obs.observe(chartEl);
</script>
</body>
</html>
