<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For Alesia 💖</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      min-height: 100vh;
      background: linear-gradient(135deg, #ffb6c1, #ff69b4);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      text-align: center;
      padding: 20px;
      overflow: hidden;
    }

    .card {
      background: rgba(255, 255, 255, 0.28);
      backdrop-filter: blur(14px);
      border-radius: 30px;
      padding: 44px 34px;
      max-width: 480px;
      width: 100%;
      box-shadow: 0 28px 55px rgba(0, 0, 0, 0.25);
      animation: fadeIn 1.2s ease;
      position: relative;
    }

    h1 {
      font-size: 2.4rem;
      margin-bottom: 12px;
    }

    h2 {
      font-size: 1.4rem;
      margin-bottom: 18px;
      font-weight: 500;
    }

    p {
      font-size: 1.15rem;
      line-height: 1.65;
      margin-bottom: 26px;
    }

    .kitty {
      width: 120px;
      margin: 0 auto 14px;
      border-radius: 18px;
    }

    .heart {
      font-size: 3.2rem;
      margin: 14px 0 22px;
      animation: pulse 1.5s infinite;
    }

    .buttons {
      display: flex;
      gap: 14px;
      justify-content: center;
      flex-wrap: wrap;
    }

    button {
      background: #fff;
      color: #ff4d88;
      border: none;
      border-radius: 999px;
      padding: 14px 26px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25);
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 14px 26px rgba(0, 0, 0, 0.3);
    }

    .hidden {
      display: none;
      margin-top: 24px;
      font-size: 1.2rem;
      animation: fadeIn 0.8s ease;
    }

    .floating-hearts span {
      position: absolute;
      bottom: -40px;
      font-size: 1.5rem;
      animation: floatUp 6s infinite;
      opacity: 0.8;
    }

    .floating-hearts span:nth-child(1) { left: 10%; animation-delay: 0s; }
    .floating-hearts span:nth-child(2) { left: 30%; animation-delay: 1.5s; }
    .floating-hearts span:nth-child(3) { left: 50%; animation-delay: 3s; }
    .floating-hearts span:nth-child(4) { left: 70%; animation-delay: 2s; }
    .floating-hearts span:nth-child(5) { left: 90%; animation-delay: 4s; }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.15); }
      100% { transform: scale(1); }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(12px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes floatUp {
      from { transform: translateY(0); opacity: 0; }
      20% { opacity: 0.9; }
      to { transform: translateY(-110vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="floating-hearts">
    <span>💗</span>
    <span>💖</span>
    <span>💕</span>
    <span>💞</span>
    <span>💓</span>
  </div>

  <div class="card">
    <img class="kitty" src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" alt="Hello Kitty" />
    <h1>Dear Alesia 💕</h1>
    <h2>This is for you</h2>
    <div class="heart">💖</div>
    <p>
      I know you’re upset, and I’m truly sorry if I hurt you.
      You mean the world to me, and I never want to lose you.
    </p>

    <p><strong>Will you forgive me?</strong></p>

    <div class="buttons">
      <button onclick="yesForgive()">Yes 💕</button>
      <button onclick="yesForgive()">Yes 💖</button>
    </div>

    <div id="finalMessage" class="hidden">
      <img class="kitty" src="https://media.giphy.com/media/l4FGGafcOHmrlQxG0/giphy.gif" alt="Hello Kitty Love" />
      <p>
        Thank you, my love 🤍<br />
        Alesia, will you be my Valentine?
      </p>
      <p><strong>Happy Valentine’s Day 💐</strong></p>
    </div>
  </div>

  <script>
    function yesForgive() {
      document.querySelector('.buttons').style.display = 'none';
      document.getElementById('finalMessage').style.display = 'block';
    }
  </script>
</body>
</html>
