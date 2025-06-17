<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Phase Client</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <div class="background-overlay">
    <canvas id="rain-canvas"></canvas>

    <header>
      <img src="logo-transparent.png" alt="icon" class="logo">
      <h1 class="title">Phase</h1>
      <p class="subtitle">Links</p>
      <nav class="buttons">
        <a href="https://www.youtube.com/@FaunaClient-f1z" class="btn secondary">Youtube</a>
        <a href="https://discord.gg/2Nb6sygmSm" class="btn secondary">Discord</a>
        <a href="#" class="btn secondary">Github</a>
      </nav>

      <!-- Optional: UI Menu Image -->
      <img src="29253dcd-d7e9-4a10-91ac-86b7588d48a0.png" alt="UI Preview" class="floating-ui">
    </header>

    <section class="features">
      <h2 class="section-title">Why choose Phase?</h2>
      <p class="section-subtitle">With our abundant set of features, you'll never want to go back to another client.</p>
      <div class="feature-grid">
        <div class="feature-card">
          <h3>Feature-abundant</h3>
          <p>Loads of modules and options for full control.</p>
        </div>
        <div class="feature-card">
          <h3>User-friendly</h3>
          <p>Just install and you’re good to go.</p>
        </div>
        <div class="feature-card">
          <h3>Consistent updates</h3>
          <p>We deliver frequent improvements and features.</p>
        </div>
        <div class="feature-card">
          <h3>Universal compatibility</h3>
          <p>Runs on Windows, macOS, and Linux.</p>
        </div>
        <div class="feature-card">
          <h3>Trusted by thousands</h3>
          <p>Built by experienced developers.</p>
        </div>
        <div class="feature-card">
          <h3>Premium quality</h3>
          <p>High standards and polish guaranteed.</p>
        </div>
      </div>
    </section>
  </div>

  <script>
    const canvas = document.getElementById('rain-canvas');
    const ctx = canvas.getContext('2d');

    let width, height;
    let drops = [];

    function resizeCanvas() {
      width = canvas.width = window.innerWidth;
      height = canvas.height = window.innerHeight;
    }

    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    const numDrops = 600;
    for (let i = 0; i < numDrops; i++) {
      drops.push({
        x: Math.random() * width,
        y: Math.random() * height,
        length: Math.random() * 20 + 10,
        velocity: Math.random() * 4 + 4,
        opacity: Math.random() * 0.5 + 0.2
      });
    }

    function drawRain() {
      ctx.clearRect(0, 0, width, height);
      ctx.strokeStyle = 'rgba(255, 255, 255, 0.1)';
      ctx.lineWidth = 1.2;

      for (let i = 0; i < drops.length; i++) {
        const drop = drops[i];
        ctx.beginPath();
        ctx.moveTo(drop.x, drop.y);
        ctx.lineTo(drop.x, drop.y + drop.length);
        ctx.stroke();

        drop.y += drop.velocity;
        if (drop.y > height) {
          drop.y = -drop.length;
          drop.x = Math.random() * width;
        }
      }

      requestAnimationFrame(drawRain);
    }

    drawRain();
  </script>
</body>
</html>
