<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your GitHub Website</title>
  <style>
    body {
      background-color: #1f1f1f;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    .glow-text {
      font-size: 3em;
      color: #00f;
      font-family: 'Arial', sans-serif;
      text-align: center;
      animation: glow 1s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from {
        text-shadow: 0 0 10px #00f, 0 0 20px #00f, 0 0 30px #00f;
      }
      to {
        text-shadow: 0 0 20px #00f, 0 0 30px #00f, 0 0 40px #00f;
      }
    }
  </style>
</head>
<body>
  <div class="glow-text">Hello</div>
</body>
</html>
