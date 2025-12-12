<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>The Best Landing Page Ever</title>
  <style>
    :root{
      --bg1:#6a3df2;
      --bg2:#ff4f8b;
      --bg3:#ffb347;

      --cardRadius:26px;
      --shadow: 0 18px 60px rgba(0,0,0,.22);
      --textShadow: 0 10px 30px rgba(0,0,0,.25);

      --btn:#ff6b78;
      --btnHover:#ff5b6a;
      --btnText:#ffffff;
    }

    *{ box-sizing:border-box; }
    html,body{ height:100%; }
    body{
      margin:0;
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
      display:grid;
      place-items:center;
      background: #f2f2f2;
      padding: 24px;
    }

    .card{
      width:min(980px, 100%);
      min-height: min(640px, 80vh);
      border-radius: var(--cardRadius);
      box-shadow: var(--shadow);
      position:relative;
      overflow:hidden;
      background: linear-gradient(135deg, var(--bg1) 0%, var(--bg2) 45%, var(--bg3) 100%);
    }

    .content{
      position:absolute;
      inset:0;
      display:flex;
      flex-direction:column;
      align-items:center;
      justify-content:center;
      text-align:center;
      padding: clamp(24px, 6vw, 64px);
      gap: clamp(22px, 5vw, 42px);
    }

    h1{
      margin:0;
      color:#fff;
      font-weight: 900;
      letter-spacing: -0.02em;
      text-shadow: var(--textShadow);
      line-height: 0.95;
      font-size: clamp(44px, 7vw, 96px);
    }

    .cta{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap: 14px;
      padding: 18px 28px;
      border-radius: 14px;
      background: var(--btn);
      color: var(--btnText);
      font-weight: 800;
      font-size: clamp(18px, 2.2vw, 26px);
      text-decoration:none;
      box-shadow: 0 14px 30px rgba(255, 107, 120, .35);
      transform: translateZ(0);
      transition: transform .12s ease, background .12s ease, box-shadow .12s ease;
    }
    .cta:hover{
      background: var(--btnHover);
      transform: translateY(-2px);
      box-shadow: 0 18px 38px rgba(255, 107, 120, .42);
    }
    .cta:active{
      transform: translateY(0px) scale(.99);
    }

    .arrow{
      font-size: 1.1em;
      line-height: 1;
      transform: translateY(1px);
    }

    /* Optional: subtle border highlight like the mock */
    .card::before{
      content:"";
      position:absolute;
      inset:0;
      border-radius: var(--cardRadius);
      pointer-events:none;
      box-shadow: inset 0 0 0 1px rgba(255,255,255,.22);
    }
  </style>
</head>

<body>
  <main class="card" role="main" aria-label="Landing page">
    <section class="content">
      <h1>The Best<br/>Landing Page<br/>Ever</h1>

      <a class="cta" href="https://instagram.com/erickerivaux" target="_blank" rel="noopener noreferrer">
        Join me on Instagram <span class="arrow">→</span>
      </a>
    </section>
  </main>
</body>
</html>
