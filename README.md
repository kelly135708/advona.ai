<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>ADVONA.AI | Performance Marketing for Global Growth</title>

<style>
:root {
  --bg:#05060a;
  --primary:#7aa2ff;
  --secondary:#9cf0ff;
  --text:#e6e8f0;
  --muted:#9aa0c3;
  --border:#1d2145;
}

*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Inter,Roboto,sans-serif;
  background:radial-gradient(1000px 500px at 20% -10%,#11144a,transparent),var(--bg);
  color:var(--text);
  overflow-x:hidden;
}
/* ===== EMERGENCY VISIBILITY FIX ===== */
body * {
  opacity: 1 !important;
  transform: none !important;
}

header, section, footer {
  position: relative !important;
  z-index: 10 !important;
}

.logo,
.hero h1,
.hero p,
nav a {
  color: #ffffff !important;
  -webkit-text-fill-color: initial !important;
  background: none !important;
}

/* ===== Header ===== */
header{
  position:fixed;
  top:0;left:0;right:0;
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:20px 32px;
  background:rgba(5,6,10,.6);
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--border);
  z-index:10;
}

.logo{
  font-size:26px;
  font-weight:900;
  letter-spacing:.32em;
  text-transform:uppercase;
  background:linear-gradient(90deg,var(--primary),var(--secondary),var(--primary));
  background-size:200% 200%;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:logoFlow 6s linear infinite;
}

@keyframes logoFlow{
  0%{background-position:0% 50%}
  100%{background-position:200% 50%}
}

nav a{
  margin-left:24px;
  font-size:14px;
  color:var(--muted);
}
nav a:hover{color:var(--text)}

/* ===== Sections ===== */
section{
  max-width:1200px;
  margin:auto;
  padding:140px 24px 100px;
}

.hero h1{
  font-size:56px;
  line-height:1.1;
  background:linear-gradient(90deg,var(--primary),var(--secondary));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

.hero p{
  max-width:640px;
  margin-top:16px;
  color:var(--muted);
  font-size:18px;
}

.btn{
  display:inline-block;
  margin-top:36px;
  margin-right:16px;
  padding:14px 32px;
  border-radius:999px;
  font-weight:600;
  font-size:14px;
  background:linear-gradient(90deg,var(--primary),var(--secondary));
  color:#000;
  transition:transform .3s ease;
}
.btn:hover{transform:translateY(-3px)}

.btn.secondary{
  background:transparent;
  color:var(--text);
  border:1px solid var(--border);
}

/* ===== Cards ===== */
.grid{
  display:grid;
  gap:24px;
}
.grid-3{
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
}

.card{
  background:linear-gradient(180deg,rgba(255,255,255,.06),transparent);
  border:1px solid var(--border);
  border-radius:20px;
  padding:28px;
  opacity:0;
  transform:translateY(40px);
  transition:all .8s ease;
}
.card.show{
  opacity:1;
  transform:none;
}

footer{
  border-top:1px solid var(--border);
  padding:48px 24px;
  text-align:center;
  color:var(--muted);
}

/* ===== Particle Background ===== */
canvas{
  position:fixed;
  inset:0;
  z-index:-1;
}

/* Mobile */
@media(max-width:900px){
  .hero h1{font-size:40px}
  .logo{font-size:22px;letter-spacing:.24em}
}
</style>
</head>

<body>

canvas {
  position: fixed;
  inset: 0;
  z-index: 0;
  pointer-events: none;
}


<header>
  <div class="logo">ADVONA.AI</div>
  <nav>
    <a href="#services">Services</a>
    <a href="#careers">Careers</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero">
  <h1>Data-Driven Growth<br>for Global Brands</h1>
  <p>
    ADVONA.AI 专注效果投放与出海增长，  
    用系统、数据与实验，把增长变成可复制的能力。
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
  <p>© 2026 ADVONA.AI · Performance Marketing for Global Growth</p>
</footer>

<script>
// ===== Scroll Reveal =====
const cards=document.querySelectorAll('.card');
const io=new IntersectionObserver(entries=>{
  entries.forEach(e=>{
    if(e.isIntersecting)e.target.classList.add('show');
  });
},{threshold:.2});
cards.forEach(c=>io.observe(c));

// ===== Particle Background =====
const canvas=document.getElementById('bg');
const ctx=canvas.getContext('2d');
let w,h,particles=[];
function resize(){
  w=canvas.width=window.innerWidth;
  h=canvas.height=window.innerHeight;
}
window.addEventListener('resize',resize);
resize();

for(let i=0;i<60;i++){
  particles.push({
    x:Math.random()*w,
    y:Math.random()*h,
    r:Math.random()*1.5+0.5,
    vx:(Math.random()-.5)*0.3,
    vy:(Math.random()-.5)*0.3
  });
}

function draw(){
  ctx.clearRect(0,0,w,h);
  ctx.fillStyle='rgba(122,162,255,.4)';
  particles.forEach(p=>{
    p.x+=p.vx; p.y+=p.vy;
    if(p.x<0||p.x>w)p.vx*=-1;
    if(p.y<0||p.y>h)p.vy*=-1;
    ctx.beginPath();
    ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
    ctx.fill();
  });
  requestAnimationFrame(draw);
}
draw();
</script>

</body>
</html>
