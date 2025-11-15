<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday to my fav Akka 🎉</title>
<style>
/* ==== GENERAL STYLE ==== */
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ffd6ff, #c8b6ff, #b8c0ff);
  font-family: "Poppins", sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  flex-direction: column;
}

/* ==== TITLE ==== */
h1 {
  font-size: 3em;
  color: #fff;
  text-shadow: 0 0 20px #ff85a2, 0 0 40px #ff85a2;
  animation: glow 2s infinite alternate;
  margin-bottom: 20px;
}

@keyframes glow {
  from { text-shadow: 0 0 10px #fff, 0 0 20px #ff9ecd; }
  to { text-shadow: 0 0 20px #ffb5d0, 0 0 50px #ff85a2; }
}

/* ==== MESSAGE BOX ==== */
.message-box {
  width: 80%;
  max-width: 500px;
  background: rgba(255,255,255,0.3);
  backdrop-filter: blur(10px);
  border-radius: 20px;
  padding: 20px;
  text-align: center;
  color: #fff;
  font-size: 1.2em;
  line-height: 1.5em;
  box-shadow: 0 0 20px rgba(255,255,255,0.2);
  border: 1px solid rgba(255,255,255,0.4);
  animation: fadeIn 3s ease;
}
@keyframes fadeIn {
  from {opacity: 0; transform: translateY(50px);}
  to {opacity: 1; transform: translateY(0);}
}

/* ==== BUTTON ==== */
button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 1em;
  background-color: #ff85a2;
  border: none;
  border-radius: 30px;
  color: white;
  cursor: pointer;
  transition: 0.3s;
  box-shadow: 0 4px 10px rgba(255, 133, 162, 0.4);
}
button:hover {
  transform: scale(1.1);
  background-color: #ff5f87;
}

/* ==== HEARTS ==== */
.heart {
  position: absolute;
  color: #ff85a2;
  font-size: 20px;
  animation: floatHearts 5s linear infinite;
  opacity: 0.8;
}
@keyframes floatHearts {
  0% { transform: translateY(0) scale(1); opacity: 1;}
  100% { transform: translateY(-800px) scale(1.5); opacity: 0;}
}

/* ==== CONFETTI ==== */
.confetti {
  position: absolute;
  width: 8px;
  height: 8px;
  background-color: #fff;
  opacity: 0.8;
  border-radius: 50%;
  animation: fall 4s linear infinite;
}
@keyframes fall {
  0% { transform: translateY(0) rotate(0deg);}
  100% { transform: translateY(800px) rotate(360deg);}
}

/* ==== MUSIC ==== */
audio {
  margin-top: 20px;
  outline: none;
}
</style>
</head>

<body>
<h1>🎂 Happy Birthday Megha Akka 🎂</h1>

<div class="message-box" id="message">
  <p>Dear Cutie Akka,<br>
  You’re not just my fav Akka, you’re my best friend, my secret keeper, and my forever favorite person. 💖<br>
  May your day sparkle with laughter, your dreams shine bright, and your heart be full of joy.<br>
  You deserve all the happiness in the world! 🎉</p>
</div>

<button id="surpriseBtn">Click for Surprise 💝</button>

<audio id="music" src="https://cdn.pixabay.com/download/audio/2023/03/14/audio_fa7b8b0d2c.mp3?filename=happy-birthday-to-you-14082.mp3"></audio>

<script>
// ====== HEART ANIMATION ======
function createHeart() {
  const heart = document.createElement('div');
  heart.classList.add('heart');
  heart.innerHTML = '💖';
  heart.style.left = Math.random() * 100 + 'vw';
  heart.style.animationDuration = 3 + Math.random() * 2 + 's';
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 5000);
}
setInterval(createHeart, 500);

// ====== CONFETTI ANIMATION ======
function createConfetti() {
  const confetti = document.createElement('div');
  confetti.classList.add('confetti');
  confetti.style.left = Math.random() * 100 + 'vw';
  confetti.style.backgroundColor = ['#ff85a2','#ffc0cb','#fff','#f4a261'][Math.floor(Math.random()*4)];
  confetti.style.animationDuration = 3 + Math.random() * 2 + 's';
  document.body.appendChild(confetti);
  setTimeout(() => confetti.remove(), 4000);
}
setInterval(createConfetti, 200);

// ====== SURPRISE BUTTON ======
const btn = document.getElementById("surpriseBtn");
const message = document.getElementById("message");
const music = document.getElementById("music");

btn.addEventListener("click", () => {
  message.innerHTML = `
    <p>🌸 Surprise Time 🌸<br><br>
    Hey Megha Akka, this little webpage is just for you!<br>
    May your journey ahead be filled with smiles, sparkles, and endless memories.<br>
    Happy Birthday my lovely sister! 💕🎂🎉<br>
Happy Birthday to the most beautiful soul in my life my sister, my best friend, and my everything!<br> You’re the one who knows me inside out and You’ve been my comfort on tough days and my partner in all the silly moments that turned into our sweetest memories. I don’t just love you — I adore you for the way you care, protect, and love me unconditionally. On your special day, I just want to remind you that you are my heart’s purest joy, my forever favorite person, and I’ll always be here for you — no matter what. 💖🎂✨
</p>`;
  btn.style.display = "none";
  music.play();
});
</script>
</body>
</html>
