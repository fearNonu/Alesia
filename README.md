<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For Alesia <3</title>
  <style>
    * { box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
    body {
      margin: 0; min-height: 100vh;
      background: linear-gradient(135deg, #ffb6c1, #ffd1dc);
      display: flex; justify-content: center; align-items: center;
      overflow: hidden; color: #333;
    }

    /* Floating hearts */
    .heart-float {
      position: absolute; bottom: -40px; font-size: 22px;
      color: rgba(255, 105, 180, 0.7);
      animation: floatUp linear infinite; pointer-events: none;
    }
    @keyframes floatUp {
      from { transform: translateY(0) scale(1); opacity: 1; }
      to { transform: translateY(-110vh) scale(1.6); opacity: 0; }
    }

    .card {
      background: #fff0f6; width: 90%; max-width: 520px;
      border-radius: 25px; padding: 30px; text-align: center;
      box-shadow: 0 25px 50px rgba(255,105,180,0.35);
      animation: fadeIn 1s ease; position: relative; z-index: 2;
    }
    h1 { color: #ff4d88; margin-bottom: 10px; }
    p { line-height: 1.6; margin-bottom: 18px; font-size: 16px; }
    .buttons { display: flex; justify-content: center; gap: 18px; margin-top: 20px; }
    button {
      border: none; border-radius: 30px; padding: 14px 26px;
      font-size: 17px; cursor: pointer; transition: transform 0.25s ease;
    }
    .yes { background: #ff69b4; color: #fff; }
    .no { background: #ffe4ec; color: #ff4d88; }
    .hidden { display: none; }
    .heart { font-size: 42px; animation: pulse 1.3s infinite; }
    .kitty { width: 90px; margin: 10px; }
    .kitty-row { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; }

    @keyframes pulse { 0%{transform:scale(1);} 50%{transform:scale(1.25);} 100%{transform:scale(1);} }
    @keyframes fadeIn { from{opacity:0;transform:translateY(25px);} to{opacity:1;transform:translateY(0);} }

    /* Kiss & Hug animation */
    .hug {
      font-size: 60px; animation: hug 2s ease infinite;
    }
    @keyframes hug {
      0% { transform: scale(1); }
      50% { transform: scale(1.3); }
      100% { transform: scale(1); }
    }
  </style>
</head>
<body>

  <!-- PAGE 1 -->
  <div class="card" id="valentine-card">
    <div class="kitty-row">
      <img class="kitty" src="https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif" />
      <img class="kitty" src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif" />
    </div>
    <h1>Alesia </h1>
    <p>I made this little pink world just for you.<br>Will you be my Valentine?</p>
    <div class="buttons">
      <button class="yes" id="yesBtn" onclick="goToSorry()">Yes I want <33333</button>
      <button class="no">No ?:(</button>
    </div>
  </div>

  <!-- PAGE 2: SORRY + KISS/HUG -->
  <div class="card hidden" id="sorry-card">
    <div class="kitty-row">
      <img class="kitty" src="https://media.giphy.com/media/ASd0Ukj0y3qMM/giphy.gif" />
      <img class="kitty" src="https://media.giphy.com/media/26ufdipQqU2lhNA4g/giphy.gif" />
    </div>
    <div class="hug"><3333</div>
    <h1>I'm really sorry, Alesia</h1>
    <p>I know I hurt you and it breaks my heart. You never deserved that.</p>
    <p>Please believe my apology comes from the deepest place in my heart.</p>
    <button class="yes" onclick="goToPromise()">Continue ??</button>
  </div>

  <!-- PAGE 3: PROMISE -->
  <div class="card hidden" id="promise-card">
    <div class="heart"></div>
    <h1>My Promise to You</h1>
    <p>Alesia, I promise to listen more, care deeper, and never take you for granted.</p>
    <p>I promise to show you love through actions, respect, patience, and honesty.</p>
    <p>No matter what, I choose you. Every day.</p>
    <p><strong>I love you endlessly <3 </strong></p>
  </div>

  <script>
    /* Yes button grows more every hover */
    let scale = 1;
    const yesBtn = document.getElementById('yesBtn');
    yesBtn.addEventListener('mouseenter', () => {
      scale += 0.15;
      yesBtn.style.transform = `scale(${scale})`;
    });

    function goToSorry() {
      document.getElementById('valentine-card').classList.add('hidden');
      document.getElementById('sorry-card').classList.remove('hidden');
    }

    function goToPromise() {
      document.getElementById('sorry-card').classList.add('hidden');
      document.getElementById('promise-card').classList.remove('hidden');
    }

    /* Floating hearts */
    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart-float';
      heart.innerText = 'Te iubesccccc<33333';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = 4 + Math.random() * 4 + 's';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 8000);
    }
    setInterval(createHeart, 400);
  </script>
</body>
</html>
