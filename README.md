<!DOCTYPE html><html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Selamat Ulang Tahun Anisa</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background-color: #000;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      color: #ff69b4;
      font-family: 'Poppins', sans-serif;
      overflow: hidden;
      position: relative;
    }h1 {
  font-size: 3.5em;
  text-transform: uppercase;
  letter-spacing: 4px;
  color: #ff69b4;
  text-shadow: 0 0 10px #ff69b4, 0 0 20px #ff69b4, 0 0 40px #ff1493;
  animation: glow 2s ease-in-out infinite alternate;
  z-index: 2;
}

@keyframes glow {
  from { text-shadow: 0 0 10px #ff69b4, 0 0 20px #ff69b4; }
  to { text-shadow: 0 0 20px #ff1493, 0 0 40px #ff69b4; }
}

p {
  font-size: 1.2em;
  color: #fff;
  margin-top: 10px;
  text-align: center;
  max-width: 600px;
  line-height: 1.6;
  animation: fadeIn 3s ease;
  z-index: 2;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.heart {
  color: #ff69b4;
  font-size: 2em;
  animation: pulse 1.2s infinite;
  z-index: 2;
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.2); }
  100% { transform: scale(1); }
}

.balloon {
  position: absolute;
  bottom: -150px;
  width: 60px;
  height: 80px;
  background: radial-gradient(circle at 30% 30%, #ffb6c1, #ff1493);
  border-radius: 50% 50% 45% 45%;
  animation: float 10s linear infinite;
}

.string {
  position: absolute;
  top: 80px;
  left: 29px;
  width: 2px;
  height: 100px;
  background: #fff;
}

@keyframes float {
  0% { transform: translateY(0) rotate(0deg); opacity: 1; }
  50% { transform: translateY(-500px) rotate(5deg); opacity: 0.9; }
  100% { transform: translateY(-1000px) rotate(-5deg); opacity: 0; }
}

  </style>
</head>
<body>
  <h1>Selamat Ulang Tahun Anisa</h1>
  <p>Semoga hari ini penuh kebahagiaan dan tawa. Kamu pantas mendapatkan yang terbaik di setiap langkahmu.</p>
  <div class="heart">❤</div>  <script>
    function createBalloon() {
      const balloon = document.createElement('div');
      const string = document.createElement('div');
      balloon.classList.add('balloon');
      string.classList.add('string');
      balloon.appendChild(string);
      document.body.appendChild(balloon);

      const left = Math.random() * window.innerWidth;
      balloon.style.left = `${left}px`;
      balloon.style.animationDuration = `${8 + Math.random() * 4}s`;

      setTimeout(() => {
        balloon.remove();
      }, 12000);
    }

    setInterval(createBalloon, 800);
  </script></body>
</html>
