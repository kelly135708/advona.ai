<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>ADVONA.AI | Performance Marketing for Global Growth</title>

<style>
:root{
  --bg:#0b0c10;
  --primary:#7aa2ff;
  --secondary:#9cf0ff;
  --text:#ffffff;
  --muted:#c5c7d6;
  --border:#22254d;
}

*{box-sizing:border-box;margin:0;padding:0}

body{
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Inter,Roboto,sans-serif;
  background:var(--bg);
  color:var(--text);
  line-height:1.6;
}

/* ===== Header ===== */
header{
  position:fixed;
  top:0;left:0;right:0;
  padding:22px 40px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  background:rgba(11,12,16,.8);
  backdrop-filter:blur(10px);
  border-bottom:1px solid var(--border);
  z-index:10;
}

/* ===== LOGO（渐变但不透明） ===== */
.logo{
  font-size:26px;
  font-weight:900;
  letter-spacing:.3em;
  text-transform:uppercase;
  background:linear-gradient(
    90deg,
    var(--primary),
    var(--secondary),
    var(--primary)
  );
  background-size:200% 100%;
  color:#ffffff; /* 兜底 */
  -webkit-background-clip:text;
  background-clip:text;
  animation:logoMove 6s linear infinite;
}

@keyframes logoMove{
  0%{background-position:0%}
  100%{background-position:200%}
}

nav a{
  margin-left:24px;
  font-size:14px;
  color:var(--muted);
}
nav a:hover{color:#fff}

/* ===== Sections ===== */
section{
  max-width:1100px;
  margin:auto;
  padding:140px 40px 100px;
}

/* ===== Hero（不依赖 observer） ===== */
.hero h1{
  font-size:54px;
  line-height:1.1;
  margin-bottom:20px;
  opacity:0;
  transform:translateY(30px);
  animation:heroIn 1s ease forwards;
}

.hero p{
  max-width:640px;
  font-size:18px;
  color:var(--muted);
  opacity:0;
  transform:translateY(20px);
  animation:heroIn 1s ease forwards;
  animation-delay:.3s;
}

.hero .btn{
  opacity:0;
  transform:translateY(20px);
  animation:heroIn 1s ease forwards;
  animation-delay:.6s;
}

@keyframes heroIn{
  to{
    opacity:1;
    transform:none;
  }
}

/* ===== Buttons ===== */
.btn{
  display:inline-block;
  margin-top:36px;
  margin-right:16px;
  padding:14px 32px;
  border-radius:999px;
  font-size:14px;
  font-weight:600;
  background:linear-gradient(90deg,var(--primary),var(--secondary));
  color:#000;
}
.btn.secondary{
  background:transparent;
  color:#fff;
  border:1px solid var(--border);
}

/* ===== Cards + 滚动动画（window.scroll） ===== */
.grid{
  display:grid;
  gap:24px;
}
.grid-3{
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
}

.card{
  border:1px solid var(--border);
  border-radius:20px;
  padding:28px;
  background:linear-gradient(180deg,rgba(255,255,255,.05),transparent);
  opacity:0;
  transform:translateY(40px);
  transition:all .8s ease;
}

.card.visible{
  opacity:1;
  transform:none;
}

/* ===== Footer ===== */
footer{
  border-top:1px solid var(--border);
  padding:48px 24px;
  text-align:center;
  color:var(--muted);
}

/* ===== Mobile ===== */
@media(max-width:900px){
  .hero h1{font-size:40px}
  .logo{font-size:22px;letter-spacing:.24em}
}
</style>
</head>

<body>

<header>
  <div class="logo">ADVONA.AI</div>
  <nav>
    <a href="#services">Services</a>
    <a href="#careers">Careers</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero">
  <h1>Performance Marketing<br>for Global Growth</h1>
  <p>
    ADVONA.AI 专注效果投放与出海增长，  
    用数据、实验和系统化方法，持续放大 ROI。
  </p>
  <p>We are hiring performance-driven builders.</p>

  <a class="btn" href="#contact">Start Growth</a>
  <a class="btn secondary" href="#careers">Join ADVONA</a>
</section>

<section id="services">
  <div class="grid grid-3">
    <div class="card"><h3>Markets</h3><p>NA · EU · SEA</p></div>
    <div class="card"><h3>Channels</h3><p>Meta · Google · TikTok</p></div>
    <div class="card"><h3>Metrics</h3><p>ROAS · CAC · LTV</p></div>
  </div>
</section>

<section id="careers">
  <div class="card">
    <h3>We Are Hiring</h3>
    <p>Core Paid Media Lead · Ownership · Global Scale</p>
  </div>
</section>

<section id="contact">
  <div class="card">
    <h3>Join ADVONA.AI</h3>
    <p><strong>talent@advona.ai</strong></p>
  </div>
</section>

<footer>
  © 2026 ADVONA.AI · Performance Marketing for Global Growth
</footer>

<script>
/* ===== 滚动动画（最稳方案） ===== */
const cards = document.querySelectorAll('.card');

function reveal(){
  const trigger = window.innerHeight * 0.85;
  cards.forEach(card=>{
    const top = card.getBoundingClientRect().top;
    if(top < trigger){
      card.classList.add('visible');
    }
  });
}

window.addEventListener('scroll', reveal);
window.addEventListener('load', reveal);
</script>

</body>
</html>
