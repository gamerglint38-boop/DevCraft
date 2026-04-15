<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DevCraft</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
  <style>
    * {margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}body {
  background: radial-gradient(circle at top, #0a1f3c, #020817);
  color:#fff;
  overflow-x:hidden;
}

header {
  position:fixed;
  width:100%;
  top:0;
  padding:15px;
  text-align:center;
  background:rgba(0,0,0,0.4);
  backdrop-filter:blur(10px);
  z-index:1000;
}

header h1 {
  color:#00cfff;
  letter-spacing:2px;
  animation:slideDown 1.5s ease;
}

@keyframes slideDown {
  from {transform:translateY(-40px);opacity:0;}
  to {transform:translateY(0);opacity:1;}
}

.hero {
  height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
}

.hero h2 {
  font-size:50px;
  background:linear-gradient(to right,#00cfff,#00ffcc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  margin-bottom:10px;
}

.hero h3 {
  opacity:0.7;
  margin-bottom:30px;
}

.buttons {
  display:flex;
  flex-wrap:wrap;
  gap:15px;
  justify-content:center;
}

.btn {
  padding:12px 25px;
  border-radius:30px;
  border:none;
  cursor:pointer;
  font-size:16px;
  color:#fff;
  transition:0.3s;
}

.btn:hover {
  transform:scale(1.1);
  box-shadow:0 0 15px rgba(0,255,255,0.6);
}

.yt {background:red;}
.dc {background:#5865F2;}
.wa {background:#25D366;}
.ig {background:#E1306C;}
.dl {background:#00cfff;}
.git {background:#333;}

section {
  padding:80px 20px;
  text-align:center;
}

.card {
  background:#0f172a;
  border:1px solid rgba(0,255,255,0.2);
  padding:20px;
  border-radius:20px;
  margin:20px auto;
  width:80%;
  box-shadow:0 10px 30px rgba(0,0,0,0.5);
  transform:translateY(50px);
  opacity:0;
  transition:0.6s;
}

.card.show {
  transform:translateY(0);
  opacity:1;
}

  </style>
</head>
<body><header>
  <h1>DevCraft</h1>
</header><div class="hero">
  <h2>DevCraft</h2>
  <h3>MCPE Plugin Developer & Content Creator</h3>  <div class="buttons">
    <button class="btn yt" onclick="openLink('https://youtube.com/@GlintGamer1')">YouTube</button>
    <button class="btn dc" onclick="openLink('#')">Discord</button>
    <button class="btn wa" onclick="openLink('#')">WhatsApp</button>
    <button class="btn ig" onclick="openLink('#')">Instagram</button>
    <button class="btn dl" onclick="openLink('#')">Downloads</button>
    <button class="btn git" onclick="openLink('#')">GitHub</button>
  </div>
</div><section>
  <h2>Downloads & Resources</h2>  <div class="card">MCPE Plugins</div>
  <div class="card">JavaScript Mods</div>
  <div class="card">Custom Gems & Crystals</div>
  <div class="card">Servers & Hosting</div>
</section><script>
function openLink(link){window.open(link,'_blank');}

const cards=document.querySelectorAll('.card');
window.addEventListener('scroll',()=>{
  cards.forEach(card=>{
    const top=card.getBoundingClientRect().top;
    if(top<window.innerHeight-100){card.classList.add('show');}
  });
});
</script></body>
</html>
