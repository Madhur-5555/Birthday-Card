<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday!</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #ffecd2, #fcb69f);
      text-align: center;
      padding: 50px;
    }
    .cake {
      position: relative;
      width: 200px;
      height: 200px;
      margin: 0 auto;
      background: #fddde6;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }
    .candle {
      position: absolute;
      top: -40px;
      left: 50%;
      transform: translateX(-50%);
      width: 10px;
      height: 40px;
      background: #ff6f61;
      border-radius: 2px;
      animation: flicker 1s infinite;
    }
    .flame {
      position: absolute;
      top: -10px;
      left: 50%;
      transform: translateX(-50%);
      width: 10px;
      height: 10px;
      background: radial-gradient(circle, #fff700 0%, #ff6f00 100%);
      border-radius: 50%;
      animation: flicker 1s infinite;
    }
    @keyframes flicker {
      0% { opacity: 1; }
      50% { opacity: 0.5; }
      100% { opacity: 1; }
    }
    #message {
      margin-top: 30px;
      font-size: 1.5em;
      color: #333;
      display: none;
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 1em;
      background-color: #ff6f61;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #ff3b2e;
    }
  </style>
</head>
<body>

  <h1>🎉 Happy Birthday! 🎉</h1>
  <div class="cake">
    <div class="candle">
      <div class="flame"></div>
    </div>
  </div>

  <button onclick="blowCandle()">Blow Candle</button>

  <div id="message">🎁 Surprise! Wishing you a fantastic year ahead! 🎁</div>

  <script>
    function blowCandle() {
      const flame = document.querySelector('.flame');
      flame.style.display = 'none';
      document.getElementById('message').style.display = 'block';
    }
  </script>

</body>
</html>
