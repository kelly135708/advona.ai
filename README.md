<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>ADVONA.AI</title>

<style>
:root{
  --bg:#0b0c10;
  --primary:#7aa2ff;
  --secondary:#9cf0ff;
  --text:#ffffff;
  --muted:#c5c7d6;
  --border:#22254d;
}

*{margin:0;padding:0;box-sizing:border-box}

body{
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Inter,Roboto,sans-serif;
  background:var(--bg);
  color:var(--text);
}

/* Header */
header{
  position:fixed;
  top:0;left:0;right:0;
  padding:22px 40px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  background:rgba(11,12,16,.9);
  border-bottom:1px solid var(--border);
  z-index:10;
}

.logo{
  font-size:26px;
  font-weight:900;
  letter-spacing:.32em;
  text-transform:uppercase;
  background:linear-gradient(
    90deg,
    var(--primary),
    var(--secondary),
    var(--primary)
  );
  background-size:200% 100%;
  color:#fff;
  -webkit-background-clip:text;
  background-clip:text;
  animation:logoMove 6s linear infinite;
}

@keyframes logoMove{
  to{background-position:200%}
}

nav a{
  margin-left:28px;
  font-size:14px;
  color:var(--muted);
  text-decoration:none;
}
nav a:hover{color:#fff}

/* Hero */
.hero{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  padding:140px 32px 80px;
}

.hero h1{
  font-size:56px;
  margin-bottom:20px;
  opacity:0;
  transform:translateY(30px);
  animation:fadeUp 1s ease forwards;
}

.hero p{
  font-size:18px;
  color:var(--muted);
  margin-bottom:36px;
  opacity:0;
  transform:translateY(20px);
  animation:fadeUp 1s ease forwards;
  animation-delay:.3s;
}

.hero a{
  display:inline-block;
  padding:14px 40px;
  border-radius:999px;
  font-weight:600;
  font-size:14px;
  background:linear-gradient(90deg,var(--primary),var(--secondary));
  color:#000;
  text-decoration:none;
  animation:fadeUp 1s ease forwards;
  animation-delay:.6s;
}

@keyframes fadeUp{
  to{opacity:1;transform:none}
}

footer{
  border-top:1px solid var(--border);
  padding:40px;
  text-align:center;
  color:var(--muted);
}
</style>
</head>

<body>

<header>
  <div class="logo">ADVONA.AI</div>
  <nav>
    <a href="careers.html">Careers</a>
  </nav>
</header>

<section class="hero">
  <div>
    <h1>Performance Marketing for Global Growth</h1>
    <p>
      We build ROI-driven paid media systems for brands scaling globally.
    </p>
    <a href="careers.html">Join ADVONA</a>
  </div>
</section>

<footer>
  © 2026 ADVONA.AI · All rights reserved
</footer>

</body>
</html>

