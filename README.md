<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>I Grew Teeth Where My Silence Was</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      scroll-behavior:smooth;
    }

    body{
      background:#040814;
      color:#d9e3ff;
      font-family:'Inter',sans-serif;
      overflow-x:hidden;
    }

    body::before{
      content:"";
      position:fixed;
      width:100%;
      height:100%;
      background:
      radial-gradient(circle at top, rgba(58,95,205,0.15), transparent 40%),
      radial-gradient(circle at bottom, rgba(10,20,50,0.9), #040814 70%);
      z-index:-2;
    }

    .stars{
      position:fixed;
      width:100%;
      height:100%;
      background:url('https://www.transparenttextures.com/patterns/stardust.png');
      opacity:0.2;
      z-index:-1;
      animation:moveStars 80s linear infinite;
    }

    @keyframes moveStars{
      from{
        transform:translateY(0);
      }
      to{
        transform:translateY(-1000px);
      }
    }

    header{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      padding:40px;
      position:relative;
    }

    .hero{
      max-width:900px;
    }

    .hero h1{
      font-family:'Cinzel',serif;
      font-size:5rem;
      letter-spacing:6px;
      color:#f0f4ff;
      text-shadow:0 0 25px rgba(125,160,255,0.4);
      line-height:1.2;
      margin-bottom:25px;
    }

    .hero p{
      font-size:1.2rem;
      line-height:1.8;
      color:#b8c3e0;
      margin-bottom:40px;
    }

    .buttons{
      display:flex;
      justify-content:center;
      gap:20px;
      flex-wrap:wrap;
    }

    .btn{
      padding:15px 35px;
      border:1px solid rgba(255,255,255,0.15);
      background:rgba(17,24,39,0.6);
      color:white;
      text-decoration:none;
      border-radius:50px;
      backdrop-filter:blur(10px);
      transition:0.4s;
      font-weight:500;
      letter-spacing:1px;
    }

    .btn:hover{
      transform:translateY(-5px);
      background:#0f3460;
      box-shadow:0 0 20px rgba(59,130,246,0.4);
    }

    section{
      padding:120px 10%;
    }

    .section-title{
      font-family:'Cinzel',serif;
      font-size:3rem;
      margin-bottom:25px;
      color:#eef3ff;
      text-align:center;
    }

    .section-sub{
      text-align:center;
      max-width:800px;
      margin:auto;
      margin-bottom:80px;
      color:#a8b3cf;
      line-height:1.9;
    }

    .poetry-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:35px;
    }

    .poem-card{
      background:rgba(9,15,30,0.8);
      border:1px solid rgba(255,255,255,0.08);
      border-radius:25px;
      padding:35px;
      transition:0.4s;
      position:relative;
      overflow:hidden;
    }

    .poem-card::before{
      content:"";
      position:absolute;
      width:300px;
      height:300px;
      background:radial-gradient(circle, rgba(59,130,246,0.15), transparent 70%);
      top:-100px;
      right:-100px;
    }

    .poem-card:hover{
      transform:translateY(-10px);
      border-color:#3b82f6;
      box-shadow:0 0 30px rgba(59,130,246,0.2);
    }

    .poem-card h3{
      font-family:'Cinzel',serif;
      margin-bottom:15px;
      color:#ffffff;
      font-size:1.5rem;
    }

    .poem-card p{
      color:#b8c3e0;
      line-height:1.8;
    }

    .merch{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:40px;
    }

    .merch-item{
      background:#0b1120;
      border-radius:25px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,0.08);
      transition:0.4s;
    }

    .merch-item:hover{
      transform:scale(1.03);
      box-shadow:0 0 25px rgba(59,130,246,0.25);
    }

    .merch-item img{
      width:100%;
      height:320px;
      object-fit:cover;
    }

    .merch-content{
      padding:25px;
    }

    .merch-content h4{
      font-family:'Cinzel',serif;
      margin-bottom:10px;
      font-size:1.3rem;
    }

    .merch-content p{
      color:#aab4d1;
      margin-bottom:20px;
      line-height:1.6;
    }

    .price{
      color:#7db0ff;
      font-weight:bold;
      font-size:1.2rem;
    }

    .quote-section{
      text-align:center;
      padding:140px 15%;
      position:relative;
    }

    .quote{
      font-size:2rem;
      line-height:1.8;
      font-family:'Cinzel',serif;
      color:#e5edff;
      text-shadow:0 0 15px rgba(59,130,246,0.2);
    }

    footer{
      padding:80px 10%;
      text-align:center;
      border-top:1px solid rgba(255,255,255,0.08);
    }

    footer h2{
      font-family:'Cinzel',serif;
      margin-bottom:20px;
      font-size:2rem;
    }

    footer p{
      color:#9eabc7;
      line-height:1.8;
      max-width:700px;
      margin:auto;
    }

    .moon{
      position:absolute;
      width:250px;
      height:250px;
      border-radius:50%;
      background:radial-gradient(circle,#dfe9ff,#839fff 70%);
      filter:blur(1px);
      opacity:0.08;
      top:8%;
      right:10%;
      box-shadow:0 0 120px rgba(130,160,255,0.5);
    }

    @media(max-width:768px){

      .hero h1{
        font-size:2.8rem;
      }

      .quote{
        font-size:1.4rem;
      }

      .section-title{
        font-size:2.2rem;
      }

      .btn{
        width:100%;
      }

      .buttons{
        flex-direction:column;
      }
    }

  </style>
</head>
<body>

<div class="stars"></div>

<header>
  <div class="moon"></div>

  <div class="hero">
    <h1>
      I GREW TEETH <br>
      WHERE MY SILENCE WAS
    </h1>

    <p>
      A poetry collection by <strong>Anvii Jain</strong>.<br>
      Love. Grief. Silence. Identity. Becoming.<br>
      Some wounds don’t bleed. They grow teeth.
    </p>

    <div class="buttons">
      <a href="#poetry" class="btn">Read Collection</a>
      <a href="#merch" class="btn">Shop Merch</a>
      <a href="#about" class="btn">About The Author</a>
    </div>
  </div>
</header>

<section id="about">
  <h2 class="section-title">About The Book</h2>

  <p class="section-sub">
    “I Grew Teeth Where My Silence Was” is a dark and introspective
    poetry collection exploring emotional survival, identity,
    heartbreak, memory, silence, and transformation.
    Through haunting imagery and raw vulnerability,
    Anvii Jain turns silence into something alive.
    Humanity really said “cope with trauma” and she answered
    with literature instead of property damage. Respect.
  </p>
</section>

<section id="poetry">

  <h2 class="section-title">Poetry Vault</h2>

  <p class="section-sub">
    Fragments of grief, longing, rage, and becoming.
  </p>

  <div class="poetry-grid">

    <div class="poem-card">
      <h3>The House Is on Fire</h3>
      <p>
        “The house is on fire,
        burning my soul.
        My bones are tired and broken now
        with all the mass of unspoken words.”
      </p>
    </div>

    <div class="poem-card">
      <h3>Consonant Sound</h3>
      <p>
        “would’ve
        could’ve
        should’ve
        my heart still aches
        at the consonant sound of your name.”
      </p>
    </div>

    <div class="poem-card">
      <h3>His Reflection</h3>
      <p>
        “Monsters don’t live under beds.
        They live in houses.
        They eat dinner.
        They raise daughters.”
      </p>
    </div>

    <div class="poem-card">
      <h3>Red Sweatshirt</h3>
      <p>
        “I only loved
        the version of you
        in my head.”
      </p>
    </div>

    <div class="poem-card">
      <h3>Result</h3>
      <p>
        “I only feel like a result.
        Everything I was
        got left in a test.”
      </p>
    </div>

    <div class="poem-card">
      <h3>Darkest Shade of Blue</h3>
      <p>
        “Once golden,
        now turning me
        into the darkest shade of blue.”
      </p>
    </div>

  </div>
</section>

<section class="quote-section">

  <div class="quote">
    “They mistook my silence for weakness.”
  </div>

</section>

<section id="merch">

  <h2 class="section-title">Merch Collection</h2>

  <p class="section-sub">
    Wear the poetry. Because apparently humans enjoy
    carrying emotional devastation as fashion accessories.
  </p>

  <div class="merch">

    <div class="merch-item">
      <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?q=80&w=1200&auto=format&fit=crop" alt="">
      <div class="merch-content">
        <h4>Darkest Shade Hoodie</h4>
        <p>
          Oversized navy hoodie with silver moon embroidery.
        </p>
        <div class="price">₹2,499</div>
      </div>
    </div>

    <div class="merch-item">
      <img src="https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?q=80&w=1200&auto=format&fit=crop" alt="">
      <div class="merch-content">
        <h4>The House Is on Fire Tee</h4>
        <p>
          Distressed black tee with blue flame artwork.
        </p>
        <div class="price">₹1,499</div>
      </div>
    </div>

    <div class="merch-item">
      <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?q=80&w=1200&auto=format&fit=crop" alt="">
      <div class="merch-content">
        <h4>Consonant Sound Tote</h4>
        <p>
          Minimal silver typography on deep navy canvas.
        </p>
        <div class="price">₹899</div>
      </div>
    </div>

  </div>

</section>

<footer>

  <h2>Anvii Jain</h2>

  <p>
    Writer. Poet. Observer of silence.<br><br>

    “This book is not just a collection of poems.
    It is a collection of moments I survived.”
  </p>

</footer>

</body>
</html>
