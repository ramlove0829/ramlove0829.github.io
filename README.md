<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>For My Love ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      color: #ffffff;
      background: radial-gradient(circle at top, #ff9a9e 0%, #ff6a88 30%, #1a1b2f 80%);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 40px 16px;
    }

    .card {
      background: rgba(10, 10, 25, 0.9);
      border-radius: 24px;
      padding: 32px 24px;
      max-width: 640px;
      width: 100%;
      box-shadow: 0 24px 60px rgba(0, 0, 0, 0.6);
      border: 1px solid rgba(255, 255, 255, 0.08);
      position: relative;
      overflow: hidden;
    }

    .card::before,
    .card::after {
      content: "";
      position: absolute;
      width: 220px;
      height: 220px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(255, 105, 180, 0.5), transparent 60%);
      opacity: 0.35;
      z-index: -1;
    }

    .card::before {
      top: -60px;
      left: -60px;
    }

    .card::after {
      bottom: -80px;
      right: -40px;
    }

    .tag {
      display: inline-block;
      padding: 6px 14px;
      font-size: 12px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.06);
      border: 1px solid rgba(255, 255, 255, 0.12);
      margin-bottom: 18px;
    }

    h1 {
      font-size: 32px;
      line-height: 1.2;
      margin-bottom: 10px;
    }

    h1 span.name {
      color: #ffb6c1;
    }

    .sub {
      font-size: 14px;
      color: rgba(255, 255, 255, 0.7);
      margin-bottom: 24px;
    }

    .heart {
      font-size: 40px;
      margin: 8px 0 20px;
      animation: pulse 1.6s infinite;
      color: #ff4b81;
      text-shadow: 0 0 18px rgba(255, 77, 122, 0.8);
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      35% { transform: scale(1.18); }
      60% { transform: scale(0.98); }
      100% { transform: scale(1); }
    }

    .quote {
      font-size: 15px;
      line-height: 1.7;
      color: rgba(255, 255, 255, 0.86);
      margin-bottom: 20px;
    }

    .quote span.highlight {
      color: #ff9a9e;
      font-weight: 600;
    }

    .author {
      font-size: 12px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: rgba(255, 255, 255, 0.5);
      margin-bottom: 26px;
    }

    .message {
      background: rgba(255, 255, 255, 0.03);
      border-radius: 18px;
      padding: 16px 18px;
      border: 1px solid rgba(255, 255, 255, 0.06);
      text-align: left;
      font-size: 14px;
      line-height: 1.7;
      color: rgba(255, 255, 255, 0.9);
      margin-bottom: 22px;
    }

    .message p + p {
      margin-top: 8px;
    }

    .label {
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: rgba(255, 255, 255, 0.6);
      margin-bottom: 6px;
    }

    .timeline {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 22px;
      justify-content: center;
    }

    .pill {
      padding: 8px 14px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      font-size: 12px;
      background: rgba(255, 255, 255, 0.02);
      color: rgba(255, 255, 255, 0.9);
    }

    .pill span {
      color: #ff9a9e;
      font-weight: 600;
    }

    .button-row {
      display: flex;
      gap: 10px;
      justify-content: center;
      margin-top: 8px;
      flex-wrap: wrap;
    }

    button {
      border: none;
      cursor: pointer;
      border-radius: 999px;
      font-size: 13px;
      padding: 10px 18px;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: transform 0.15s ease, box-shadow 0.15s ease, background 0.2s ease;
    }

    button.primary {
      background: linear-gradient(135deg, #ff6a88, #ff99ac);
      color: #1a1025;
      font-weight: 600;
      box-shadow: 0 10px 25px rgba(255, 99, 132, 0.6);
    }

    button.secondary {
      background: rgba(255, 255, 255, 0.03);
      color: rgba(255, 255, 255, 0.9);
      border: 1px solid rgba(255, 255, 255, 0.16);
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 14px 30px rgba(0, 0, 0, 0.4);
    }

    footer {
      margin-top: 14px;
      font-size: 11px;
      color: rgba(255, 255, 255, 0.6);
    }

    footer span {
      color: #ff9a9e;
    }

    .floating-heart {
      position: fixed;
      font-size: 20px;
      pointer-events: none;
      animation: floatUp 2s ease-out forwards;
      color: #ff6a88;
      text-shadow: 0 0 12px rgba(255, 105, 135, 0.9);
    }

    @keyframes floatUp {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-80px); opacity: 0; }
    }

    @media (min-width: 640px) {
      h1 { font-size: 36px; }
      .card { padding: 36px 32px; }
      .message { font-size: 15px; }
    }
  </style>
</head>
<body>

  <div class="card">
    <div class="tag">A little website for you</div>

    <!-- Names updated -->
    <h1>Dear <span class="name">Saumya</span>, I love you</h1>

    <p class="sub">
      This page is my small way of saying how much you mean to me, today and every day.
    </p>

    <div class="heart" id="mainHeart">❤</div>

    <p class="quote">
      “Being deeply loved by someone gives you strength, while loving someone deeply gives you courage.”
      <span class="highlight">You are my strength and my courage.</span>
    </p>
    <p class="author">– For you, from Ram</p>

    <div class="label">From my heart</div>
    <div class="message">
      <p>
        I just want you to know that you are the best part of my every single day.
        Your smile makes everything lighter, your voice calms every storm, and your presence turns
        normal moments into my favourite memories.
      </p>
      <p>
        No matter how busy life gets, there will always be a corner of my world reserved just for you –
        where you are safe, loved, and endlessly appreciated.
      </p>
      <p>
        This website will stay online as a quiet reminder that somewhere, someone is always
        cheering for you, thinking of you, and completely, genuinely in love with you.
      </p>
    </div>

    <div class="label">Little things I adore</div>
    <div class="timeline">
      <div class="pill">Your <span>laugh</span> when you forget why you started laughing</div>
      <div class="pill">The way you say my <span>name</span></div>
      <div class="pill">Your cute <span>anger</span> that never lasts long</div>
      <div class="pill">How you always <span>care</span> about everyone</div>
      <div class="pill">The way you make everything feel <span>better</span></div>
    </div>

    <div class="button-row">
      <button class="primary" id="moreLoveBtn">
        Tap for more love 💕
      </button>
      <button class="secondary" onclick="alert('Reminder: You are loved more than you think, Saumya. Always. ❤')">
        Read this when you feel low
      </button>
    </div>

    <footer>
      Made with <span>infinite love</span> by <span>Ram</span>.
    </footer>
  </div>

  <script>
    const heart = document.getElementById("mainHeart");
    const moreLoveBtn = document.getElementById("moreLoveBtn");

    function createFloatingHeart(x, y) {
      const h = document.createElement("div");
      h.className = "floating-heart";
      h.textContent = "❤";
      h.style.left = x + "px";
      h.style.top = y + "px";
      document.body.appendChild(h);
      setTimeout(() => h.remove(), 1900);
    }

    heart.addEventListener("click", (e) => {
      for (let i = 0; i < 5; i++) {
        const offsetX = (Math.random() - 0.5) * 80;
        const offsetY = (Math.random() - 0.5) * 10;
        createFloatingHeart(e.clientX + offsetX, e.clientY + offsetY);
      }
    });

    moreLoveBtn.addEventListener("click", (e) => {
      for (let i = 0; i < 12; i++) {
        const angle = (Math.PI * 2 * i) / 12;
        const radius = 40 + Math.random() * 20;
        const x = e.clientX + Math.cos(angle) * radius;
        const y = e.clientY + Math.sin(angle) * radius;
        createFloatingHeart(x, y);
      }
    });
  </script>
</body>
</html>
