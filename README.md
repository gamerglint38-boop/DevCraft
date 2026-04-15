<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Devcraft</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }body {
  background: linear-gradient(to bottom, #87CEEB, #e0f7ff);
  color: #fff;
  overflow-x: hidden;
}

header {
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  padding: 20px;
  text-align: center;
  background: rgba(0,0,0,0.2);
  backdrop-filter: blur(10px);
  z-index: 1000;
}

header h1 {
  font-size: 28px;
  letter-spacing: 2px;
  animation: slideDown 1.5s ease;
}

@keyframes slideDown {
  from {
    transform: translateY(-50px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

.hero {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.hero h2 {
  font-size: 40px;
  margin-bottom: 20px;
  animation: fadeIn 2s ease;
}

.hero p {
  font-size: 18px;
  margin-bottom: 30px;
  animation: fadeIn 3s ease;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.yt-button {
  padding: 15px 30px;
  background: red;
  color: white;
  border: none;
  border-radius: 50px;
  font-size: 18px;
  cursor: pointer;
  transition: 0.3s;
  animation: pulse 2s infinite;
}

.yt-button:hover {
  transform: scale(1.1);
  box-shadow: 0 0 20px rgba(255,0,0,0.7);
}

@keyframes pulse {
  0% { box-shadow: 0 0 0 0 rgba(255,0,0,0.7); }
  70% { box-shadow: 0 0 0 20px rgba(255,0,0,0); }
  100% { box-shadow: 0 0 0 0 rgba(255,0,0,0); }
}

section {
  padding: 80px 20px;
  text-align: center;
  color: #000;
}

.card {
  background: white;
  padding: 20px;
  border-radius: 20px;
  margin: 20px auto;
  width: 80%;
  box-shadow: 0 10px 20px rgba(0,0,0,0.2);
  transform: translateY(50px);
  opacity: 0;
  transition: all 0.6s ease;
}

.card.show {
  transform: translateY(0);
  opacity: 1;
}

  </style>
</head>
<body>  <header>
    <h1>DevCraft</h1>
  </header>  <div class="hero">
    <h2>Welcome to DevCraft</h2>
    <p>Best Minecraft Plugins & Mods for MCPE 0.15.10</p>
    <button class="yt-button" onclick="openYT()">Subscribe on YouTube</button>
  </div>  <section>
    <div class="card">Amazing Plugins Available</div>
    <div class="card">Custom Gems & Crystals</div>
    <div class="card">Unique SMP Features</div>
  </section>  <script>
    function openYT() {
      window.open("https://www.youtube.com/@GlintGamer1", "_blank");
    }

    // Scroll Animation
    const cards = document.querySelectorAll('.card');

    window.addEventListener('scroll', () => {
      cards.forEach(card => {
        const cardTop = card.getBoundingClientRect().top;
        const windowHeight = window.innerHeight;

        if(cardTop < windowHeight - 100) {
          card.classList.add('show');
        }
      });
    });
  </script></body>
</html>
