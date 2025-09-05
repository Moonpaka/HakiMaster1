<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>HakiMaster ($HIM) - Ultimate Meme Coin</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&family=Dancing+Script:wght@700&family=Roboto+Mono&display=swap" rel="stylesheet">
  <style>
    html, body {
      height: 100%;
      margin: 0;
      padding: 0;
      overflow-x: hidden;
      background: #161616;
      position: relative;
    }
    body {
      font-family: 'Roboto Mono', monospace;
      color: #fff;
      min-height: 100vh;
      padding: 0 0 40px 0;
      position: relative;
      z-index: 1;
    }
    /* Particle background */
    .bg-particles {
      position: fixed;
      top:0; left:0; width:100vw; height:100vh;
      pointer-events:none;
      z-index: 0;
      overflow: hidden;
      filter: blur(0.8px);
      opacity: 0.15;
    }
    .container {
      position: relative;
      z-index: 2;
      max-width: 780px;
      margin: 42px auto;
      padding: 36px 24px 28px 24px;
      background: rgba(18,18,18,0.95);
      border-radius: 26px;
      box-shadow: 0 0 48px #ffe4401a, 0 8px 60px #111c;
      backdrop-filter: blur(2.5px);
      animation: slideDown 1.3s cubic-bezier(.37,1.41,.47,.99);
    }
    @keyframes slideDown {
      from { opacity:0; transform: translateY(-60px) scale(0.98);}
      to { opacity:1; transform: none;}
    }
    .logo3d {
      display: block;
      margin: 0 auto 18px auto;
      width: 260px; max-width: 95vw;
      filter: drop-shadow(0 2px 42px #ffe44088);
      transition: transform 0.9s cubic-bezier(.68,-0.55,.27,1.55);
      cursor:pointer;
      will-change: transform;
      perspective: 600px;
      backface-visibility: hidden;
      animation: logoFloat 3.7s infinite ease-in-out alternate;
    }
    .logo3d:hover {
      transform: rotateY(1turn) scale(1.07);
      filter: drop-shadow(0 4px 88px #ffe440ee);
    }
    @keyframes logoFloat {
      0% { transform: translateY(0) rotateX(0deg);}
      60% { transform: translateY(-9px) rotateX(10deg);}
      100% { transform: translateY(0) rotateX(0deg);}
    }
    .subtitle {
      font-size: 1.32em;
      color: #ffe440;
      margin-bottom: 16px;
      font-family: 'Dancing Script', cursive;
      letter-spacing: 1px;
      animation: fadeIn 1.8s 0.2s both;
    }
    @keyframes fadeIn {
      from { opacity:0; filter: blur(16px);}
      to { opacity:1; filter: none;}
    }
    h1 {
      font-family: 'Orbitron', sans-serif;
      font-size: 2.7em;
      color: #fff;
      text-shadow:
        0 0 28px #ffe440,
        0 0 2px #000,
        0 1px 0 #ffe44055;
      margin: 0 0 20px 0;
      letter-spacing: 2.5px;
      background: linear-gradient(92deg, #ffe440 30%, #fff 55%, #ffec80 80%);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      -webkit-text-fill-color: transparent;
      filter: drop-shadow(0 1px 8px #ffe44055);
      animation: shineText 4s infinite linear alternate;
    }
    @keyframes shineText {
      0% {filter: drop-shadow(0 1px 8px #ffe44055);}
      45% {filter: drop-shadow(0 1px 24px #ffe440cc);}
      100% {filter: drop-shadow(0 1px 8px #ffe44055);}
    }
    .desc {
      font-size: 1.15em;
      color: #eee;
      margin: 8px 0 24px;
      font-family:inherit;
      animation: fadeIn 1.3s 0.6s both;
    }
    .btn-row {
      margin: 0 0 18px 0;
      display: flex;
      gap: 18px;
      justify-content: center;
      flex-wrap: wrap;
    }
    .btn3d {
      font-family: 'Orbitron', sans-serif;
      font-weight: 600;
      letter-spacing: 1.5px;
      font-size: 1.1em;
      color: #222;
      background: linear-gradient(90deg,#ffe440,#fff59c 60%,#ffe440);
      box-shadow: 0 2px 16px #ffe44033,0 0px 0 #ffe440,0 2.5px 0 #fff inset;
      border-radius: 10px;
      border: none;
      padding: 15px 32px;
      margin: 7px 0;
      outline: none;
      cursor: pointer;
      transition: 
        box-shadow .19s, 
        transform .19s, 
        background .17s, 
        color .18s;
      text-shadow: 0 2px 14px #fff7,0 1px 0 #ffe440bb;
      position: relative;
      overflow: hidden;
      will-change: transform;
      filter: brightness(1.08);
    }
    .btn3d:hover, .btn3d:focus {
      background: linear-gradient(90deg,#fff59c,#ffe440 50%,#fffdd0 100%);
      color: #111;
      box-shadow: 0 6px 28px #ffe44099,0 0 0 #ffe440,0 2.5px 0 #fff inset;
      transform: translateY(-3px) scale(1.06);
      outline: none;
      filter: brightness(1.13);
    }
    .contract {
      font-size: 1.07em;
      background: #191919;
      border-radius: 13px;
      padding: 15px;
      margin: 28px auto 26px auto;
      max-width: 540px;
      word-break: break-all;
      color: #ffe440;
      box-shadow: 0 0 22px #ffe44011;
      border: 1.5px dashed #ffe440;
      animation: fadeIn 1.9s 1.9s both;
    }
    h2 {
      font-size: 1.63em;
      color: #fff;
      margin-top: 34px;
      margin-bottom: 7px;
      text-shadow: 0 0 14px #ffe44055;
      font-family: 'Orbitron', sans-serif;
      letter-spacing: 1.2px;
      background: linear-gradient(96deg,#ffe440 10%,#fff 50%,#ffe440 90%);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      -webkit-text-fill-color: transparent;
      animation: shineText 4.5s .6s infinite linear alternate;
    }
    ul.steps, ul.goals {
      list-style: none;
      padding: 0;
      font-size: 1.13em;
      margin: 18px auto 20px auto;
      text-align: left;
      max-width: 540px;
      animation: fadeIn 1.6s 1.4s both;
    }
    ul.steps li, ul.goals li {
      margin: 11px 0;
      padding: 12px 18px;
      background: #181818cc;
      border-radius: 11px;
      border-left: 4px solid #ffe440cc;
      color: #fff;
      box-shadow: 0 0 12px #ffe44010;
    }
    ul.goals li b { color: #ffe440; }
    .story-block {
      background: #181818;
      border-radius: 13px;
      padding: 16px 17px 13px 17px;
      margin: 26px auto;
      max-width: 600px;
      font-size: 1.09em;
      color: #ffe440;
      border: 1.5px dashed #ffe440;
      box-shadow: 0 0 16px #ffe44012;
      animation: fadeIn 2.1s 2.1s both;
    }
    .social-section {
      margin: 38px 0 22px 0;
    }
    .social-icons {
      display: flex;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
      margin: 13px 0 8px 0;
    }
    .icon-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 54px;
      height: 54px;
      background: #191919;
      border-radius: 50%;
      box-shadow: 0 2px 17px #ffe44022;
      transition: transform 0.19s, box-shadow 0.15s, background 0.15s;
      margin: 0;
      border: 1.5px solid #ffe440;
      outline: none;
      cursor: pointer;
      position: relative;
      overflow: hidden;
      will-change: transform;
    }
    .icon-btn:hover {
      transform: scale(1.19) rotateZ(-8deg);
      box-shadow: 0 4px 32px #ffe44077;
      background: #ffe440;
      border-color: #fff;
    }
    .icon-btn svg {
      width: 32px;
      height: 32px;
      display: block;
      transition: filter 0.27s, transform 0.27s;
      filter: drop-shadow(0 0 6px #ffe44077);
      fill: #ffe440;
    }
    .icon-btn:hover svg {
      filter: drop-shadow(0 0 35px #000a);
      fill: #191919;
      transform: scale(1.13) rotate(-6deg);
    }
    .community-list {
      margin: 0 auto;
      text-align: left;
      max-width: 420px;
      color: #ffe440;
      font-size: 1.07em;
    }
    .community-list li { margin: 8px 0 8px 0; }
    .community-list a {
      color: #fff;
      text-decoration: underline;
      transition: color 0.2s;
    }
    .community-list a:hover { color: #ffe440; }
    footer {
      font-size: 0.97em;
      color: #888;
      margin-top: 36px;
      opacity: 0.7;
      text-align: center;
    }
    @media (max-width: 700px) {
      h1 { font-size: 1.16em; }
      .logo3d { width: 140px;}
      .container { padding: 7px;}
      .icon-btn { width: 36px; height: 36px;}
      .icon-btn svg { width: 20px; height: 20px;}
      h2 { font-size: 1.08em;}
      ul.steps, ul.goals { font-size: 0.94em;}
      .story-block { font-size: 0.98em;}
    }
  </style>
</head>
<body>
  <!-- Particle/Light background -->
  <svg class="bg-particles"></svg>
  <div class="container">
    <!-- Animated 3D-effect Logo: "HakiMaster" SVG -->
    <svg class="logo3d" viewBox="0 0 520 110">
      <defs>
        <linearGradient id="gold3d" x1="0" y1="0" x2="1" y2="1">
          <stop stop-color="#ffe440"/>
          <stop offset="0.45" stop-color="#fff59c"/>
          <stop offset="0.7" stop-color="#ffe440"/>
          <stop offset="1" stop-color="#fff9c4"/>
        </linearGradient>
        <filter id="glow" x="-70%" y="-70%" width="250%" height="250%">
          <feGaussianBlur stdDeviation="6" result="coloredBlur"/>
          <feMerge>
            <feMergeNode in="coloredBlur"/>
            <feMergeNode in="SourceGraphic"/>
          </feMerge>
        </filter>
      </defs>
      <text x="50%" y="50%" text-anchor="middle" dy=".32em"
        font-family="'Orbitron', Arial Black, sans-serif"
        font-size="74"
        font-weight="bold"
        fill="url(#gold3d)"
        filter="url(#glow)"
        letter-spacing="3"
        style="paint-order:stroke; stroke:#fff8; stroke-width:2.5; text-shadow:0 0 60px #ffe44077;">
        HakiMaster
      </text>
    </svg>
    <div class="subtitle">Unleash Your Haki! The Ultimate Meme Coin.</div>
    <h1>HakiMaster ($HIM)</h1>
    <p class="desc">
      🔥 Join a movement with real power. HakiMaster is 100% community, 0% tax, only vibes.<br>
      Are you ready to master your Haki?
    </p>
    <div class="btn-row">
      <a class="btn3d" href="https://www.dextools.io/" target="_blank">Chart</a>
      <a class="btn3d" href="https://t.me/hakimastercoin" target="_blank">Telegram</a>
      <a class="btn3d" href="#" target="_blank">Buy $HIM</a>
    </div>
    <div class="contract">
      <b>Token Contract Address:<br></b>
      0x0000000000000000000000000000000000000000
    </div>
    <h2>How To Join?</h2>
    <ul class="steps">
      <li>1️⃣ Get $HIM on DEXTools or join our Telegram for help</li>
      <li>2️⃣ HOLD and become part of the HakiMaster Army</li>
      <li>3️⃣ Enjoy the ride — this is just the beginning!</li>
    </ul>
    <h2>Tokenomics</h2>
    <ul class="goals">
      <li><b>Total Supply:</b> 1,000,000,000 $HIM</li>
      <li><b>Community:</b> 100% fair launch. No presale. No taxes.</li>
      <li><b>Security:</b> Liquidity locked, contract renounced.</li>
      <li><b>Driven by:</b> Memes, energy, and real Haki!</li>
    </ul>
    <h2>Roadmap</h2>
    <ul class="goals">
      <li><b>Step 1:</b> Launch & Initial Hype</li>
      <li><b>Step 2:</b> Listings on CoinGecko & CoinMarketCap</li>
      <li><b>Step 3:</b> Viral Community Memes & Marketing</li>
      <li><b>Step 4:</b> Centralized Exchange Listings</li>
      <li><b>Step 5:</b> HakiMaster Merch Drop</li>
      <li><b>Step 6:</b> More to be revealed...</li>
    </ul>
    <h2>Our Story</h2>
    <div class="story-block">
      It all began with a dream of mastering Haki — power, will, and unity. HakiMaster ($HIM) is more than a token, it's a movement.<br><br>
      0% tax, 100% community. No presale, no nonsense. Just unleash your Haki, meme hard, and join the most legendary army in crypto!
    </div>
    <div class="social-section">
      <h2>Connect & Join Us</h2>
      <div class="social-icons">
        <!-- Twitter/X -->
        <a href="https://x.com/devniqq" class="icon-btn" target="_blank" title="Twitter/X">
          <svg viewBox="0 0 32 32" fill="none">
            <rect width="32" height="32" rx="16" />
            <path d="M23.643 9.75c-.835.37-1.732.62-2.675.733a4.684 4.684 0 002.05-2.579 9.281 9.281 0 01-2.97 1.135 4.662 4.662 0 00-7.95 4.252A13.228 13.228 0 018.1 8.845a4.662 4.662 0 001.44 6.216 4.635 4.635 0 01-2.112-.583v.059a4.666 4.666 0 003.74 4.574c-.446.121-.915.148-1.393.056a4.667 4.667 0 004.355 3.237A9.357 9.357 0 017 24.027a13.173 13.173 0 007.188 2.108c8.621 0 13.337-7.148 13.337-13.337 0-.203-.005-.407-.015-.609a9.57 9.57 0 002.346-2.439z"/>
          </svg>
        </a>
        <!-- X Community -->
        <a href="https://x.com/i/communities/1963034145736790347" class="icon-btn" target="_blank" title="X Community">
          <svg viewBox="0 0 32 32" fill="none">
            <rect width="32" height="32" rx="16" />
            <path d="M10 22L22 10M10 10l12 12" stroke="#ffe440" stroke-width="2" stroke-linecap="round"/>
          </svg>
        </a>
        <!-- Discord -->
        <a href="https://discord.com/invite/jSagY6e3" class="icon-btn" target="_blank" title="Discord">
          <svg viewBox="0 0 32 32" fill="none">
            <rect width="32" height="32" rx="16" />
            <path d="M24.5 21.5c0 .552-.448 1-1 1h-15c-.552 0-1-.448-1-1v-11c0-.552.448-1 1-1h15c.552 0 1 .448 1 1v11zm-6.5-5.5c.552 0 1-.448 1-1s-.448-1-1-1-1 .448-1 1 .448 1 1 1zm-5 0c.552 0 1-.448 1-1s-.448-1-1-1-1 .448-1 1 .448 1 1 1zm9.25 3.25c-.25-.334-1.334-1.25-3.25-1.25s-3 .916-3.25 1.25c-.083.111-.083.278 0 .389.083.111.25.139.389.083 1.056-.472 2.472-.472 3.528 0 .139.056.306.028.389-.083.083-.111.083-.278 0-.389z"/>
          </svg>
        </a>
        <!-- Telegram -->
        <a href="https://t.me/@devniqcommunity" class="icon-btn" target="_blank" title="Telegram">
          <svg viewBox="0 0 32 32" fill="none">
            <rect width="32" height="32" rx="16" />
            <path d="M23.872 8.425a1.127 1.127 0 0 0-1.17-.156L7.572 15.011c-.44.193-.67.543-.654 1.01.017.468.277.803.735.957l3.575 1.235c.245.085.478.013.694-.215l5.172-5.324c.094-.096.194-.09.293.018.099.108.096.212-.009.308l-4.179 3.901c-.094.088-.063.155.088.155h2.168c.393 0 .724.217.993.652l2.135 3.444c.174.28.41.42.71.42.185 0 .353-.064.504-.194a1.12 1.12 0 0 0 .385-.845V9.455c0-.378-.124-.66-.372-.83z"/>
          </svg>
        </a>
      </div>
      <ul class="community-list">
        <li>🌐 <a href="https://t.me/hakimastercoin" target="_blank">Telegram Main</a></li>
        <li>🌐 <a href="https://t.me/@devniqcommunity" target="_blank">Telegram Community</a></li>
        <li>🌐 <a href="https://x.com/devniqq" target="_blank">Twitter</a></li>
        <li>🌐 <a href="https://x.com/i/communities/1963034145736790347" target="_blank">X Community</a></li>
        <li>🌐 <a href="https://discord.com/invite/jSagY6e3" target="_blank">Discord</a></li>
      </ul>
    </div>
    <footer>
      🚨 Not financial advice. Just Haki, just fun, just memes.<br>
      Copyright 2025 HakiMaster ($HIM) ©
    </footer>
  </div>
  <script>
    // Particle SVG BG
    const p = document.querySelector('.bg-particles');
    function random(min, max) { return Math.random()*(max-min)+min; }
    p.innerHTML = Array.from({length: 40}, (_,i)=>`
      <circle cx="${random(0,100)}vw" cy="${random(0,100)}vh" r="${random(0.7,2.2)}vw"
        fill="#ffe440" opacity="${random(0.13,0.32)}">
        <animate attributeName="cx" values="0;100;0" dur="${random(9,21)}s" repeatCount="indefinite" begin="${i*0.6}s"/>
        <animate attributeName="cy" values="100;0;100" dur="${random(12,28)}s" repeatCount="indefinite" begin="${i*0.9}s"/>
      </circle>
    `).join('');
  </script>
</body>
</html>
