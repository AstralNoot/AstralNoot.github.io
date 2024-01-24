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
      align-items: flex-start;
      justify-content: flex-end;
      height: 100vh;
      margin: 0;
    }

    .glow-text {
      font-size: 3em;
      color: #fff;
      font-family: 'Arial', sans-serif;
      text-align: right;
      margin: 10px;
      animation: glow 1s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from {
        text-shadow: 0 0 25px #fff, 0 0 50px #fff, 0 0 75px #fff;
      }
      to {
        text-shadow: 0 0 50px #fff, 0 0 75px #fff, 0 0 100px #fff;
      }
    }
  </style>
</head>
<body>
  <div class="glow-text">Hello</div>
</body>
</html>
