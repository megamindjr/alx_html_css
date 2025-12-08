<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Headphones — Landing Page</title>

  <!-- Fonts: Source Sans Pro from Google. Spin Cycle OT is a display font — place locally if not available. -->
  <link href="https://fonts.googleapis.com/css2?family=Source+Sans+3:ital,wght@0,300;0,400;0,700;1,400&display=swap" rel="stylesheet">

  <style>
    /* If you downloaded Spin Cycle OT, place it in /fonts and uncomment the @font-face below
    @font-face {
      font-family: 'Spin Cycle OT';
      src: url('./fonts/SpinCycleOT.woff2') format('woff2'),
           url('./fonts/SpinCycleOT.woff') format('woff');
      font-weight: 400 700;
      font-style: normal;
      font-display: swap;
    }
    */

    :root{
      --accent: #FF6565;
      --bg: #F7F7FB;
      --card: #FFFFFF;
      --muted: #6B7280;
      --max-width: 1000px;
      --gutter: 24px;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: 'Source Sans 3', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background:var(--bg);
      color:#111827;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:40px 20px;
      display:flex;
      justify-content:center;
    }

    /* Page container with constrained width */
    .container{
      width:100%;
      max-width:var(--max-width);
      margin:0 auto;
    }

    header{
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:16px;
      margin-bottom:36px;
    }

    .brand{
      display:flex;align-items:center;gap:12px;text-decoration:none;color:inherit
    }
    .logo{
      width:44px;height:44px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#FFB3B3);display:flex;align-items:center;justify-content:center;color:white;font-weight:700;font-size:20px
    }
    nav a{margin-left:18px;text-decoration:none;color:inherit;font-weight:600}
    nav a:hover{color:var(--accent)}

    /* HERO */
    .hero{
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:32px;
      align-items:center;
    }

    .hero-left{
      padding:28px;
      background:linear-gradient(180deg, rgba(255,255,255,0.6), rgba(255,255,255,0.3));
      border-radius:18px;
      box-shadow:0 8px 30px rgba(16,24,40,0.06);
    }

    h1{font-size:36px;margin:0 0 12px}
    p.lead{color:var(--muted);margin:0 0 20px}

    .cta-row{display:flex;gap:14px;align-items:center}
    .btn{
      display:inline-flex;align-items:center;gap:10px;padding:12px 18px;border-radius:12px;border:0;cursor:pointer;font-weight:700;text-decoration:none;
      background:var(--accent);color:white;box-shadow:0 6px 18px rgba(255,101,101,0.18);transition:opacity .18s ease,transform .12s ease
    }
    .btn:hover,.btn:active{opacity:0.9}

    .btn-outline{
      border:2px solid rgba(17,24,39,0.06);
      background:transparent;color:inherit;padding:10px 16px;border-radius:12px;font-weight:700
    }
    .btn-outline:hover{color:var(--accent)}

    /* product card */
    .product-card{
      background:var(--card);padding:18px;border-radius:14px;box-shadow:0 6px 20px rgba(12,18,31,0.06);display:flex;gap:16px;align-items:center
    }
    .product-thumb{width:120px;height:120px;border-radius:12px;background:linear-gradient(135deg,#fff,#f3f3f8);display:flex;align-items:center;justify-content:center;font-size:32px}
    .product-info h3{margin:0 0 6px}
    .price{font-weight:800}

    /* features grid */
    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:26px}
    .feature{background:var(--card);padding:16px;border-radius:12px;text-align:left;box-shadow:0 6px 18px rgba(12,18,31,0.04)}
    .feature h4{margin:0 0 8px}
    .feature p{margin:0;color:var(--muted);font-size:14px}

    /* testimonials / details */
    .details{display:flex;gap:20px;margin-top:28px}
    .specs, .gallery{flex:1}
    .specs ul{padding-left:18px;margin:0;color:var(--muted)}

    footer{margin-top:44px;padding:18px 0;color:var(--muted);font-size:14px;text-align:center}

    /* small screens: stack everything and switch to mobile layout */
    @media (max-width: 880px){
      .hero{grid-template-columns:1fr}
      .hero-left{order:2}
    }

    /* Mobile breakpoint per requirements: switch layout when width <= 480px */
    @media (max-width:480px){
      body{padding:20px}
      h1{font-size:26px}
      .hero{grid-template-columns:1fr;gap:16px}
      .features{grid-template-columns:1fr}
      nav a{display:none}
      header{align-items:flex-start;gap:10px}
      .product-card{flex-direction:row}
    }

    /* Accessibility and small details */
    a:focus{outline:3px solid rgba(255,101,101,0.18);outline-offset:3px}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <a class="brand" href="#">
        <div class="logo">HK</div>
        <div>
          <div style="font-weight:800">Headphones</div>
          <small style="color:var(--muted);font-size:12px">Premium audio</small>
        </div>
      </a>

      <nav aria-label="Main navigation">
        <a href="#features">Features</a>
        <a href="#specs">Specs</a>
        <a href="#buy">Buy</a>
      </nav>
    </header>

    <main>
      <section class="hero" aria-labelledby="hero-title">
        <div class="hero-left">
          <h1 id="hero-title">Hear every detail — <br>Comfort that lasts</h1>
          <p class="lead">Experience studio-quality sound, active noise cancellation, and a 40-hour battery life — built for everyday listening.</p>

          <div class="product-card" style="margin-bottom:18px">
            <div class="product-thumb">🎧</div>
            <div class="product-info">
              <h3>HK-1 Wireless</h3>
              <div style="display:flex;gap:10px;align-items:center">
                <div class="price">$199</div>
                <div style="color:var(--muted);font-size:14px">Free shipping</div>
              </div>
            </div>
          </div>

          <div class="cta-row">
            <a class="btn" href="#buy">Buy Now</a>
            <a class="btn-outline" href="#specs">See Specs</a>
          </div>

          <div class="features" id="features">
            <div class="feature">
              <h4>Active Noise Cancellation</h4>
              <p>Block the world and focus on what matters with adaptive ANC.</p>
            </div>
            <div class="feature">
              <h4>40 hr Battery</h4>
              <p>All-day listening on a single charge with quick-charge support.</p>
            </div>
            <div class="feature">
              <h4>Comfort Fit</h4>
              <p>Memory-foam earcups and lightweight construction for long sessions.</p>
            </div>
          </div>
        </div>

        <aside class="hero-right" style="display:flex;flex-direction:column;gap:18px">
          <div style="background:linear-gradient(180deg,#FFF,#F9FBFF);padding:20px;border-radius:14px;display:flex;flex-direction:column;gap:12px;align-items:center">
            <img src="./images/headphones-hero.png" alt="HK-1 Headphones" style="width:100%;max-width:320px;display:block;object-fit:contain">
            <div style="font-weight:700">HK-1 Series</div>
            <div style="color:var(--muted);font-size:14px;text-align:center">Refined sound for creators and listeners</div>
          </div>

          <div style="background:var(--card);padding:14px;border-radius:12px;box-shadow:0 6px 16px rgba(12,18,31,0.04)">
            <h4 style="margin:0 0 8px">In the box</h4>
            <ul style="margin:0;padding-left:18px;color:var(--muted);font-size:14px">
              <li>HK-1 Headphones</li>
              <li>USB-C Charging Cable</li>
              <li>Carrying Case</li>
            </ul>
          </div>
        </aside>
      </section>

      <section class="details" id="specs">
        <div class="specs">
          <h3>Technical Specifications</h3>
          <ul>
            <li>Driver: 40mm dynamic</li>
            <li>Battery life: 40 hours (ANC off)</li>
            <li>Connectivity: Bluetooth 5.3, aptX Adaptive</li>
            <li>Weight: 265g</li>
          </ul>

          <h4 style="margin-top:18px">Customer reviews</h4>
          <p style="color:var(--muted);">"Great soundstage and comfort — perfect for long edits." — Alex</p>
        </div>

        <div class="gallery">
          <h3>Gallery</h3>
          <div style="display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:10px">
            <div style="background:#fff;padding:10px;border-radius:10px;display:flex;align-items:center;justify-content:center;min-height:80px">Image 1</div>
            <div style="background:#fff;padding:10px;border-radius:10px;display:flex;align-items:center;justify-content:center;min-height:80px">Image 2</div>
          </div>
        </div>
      </section>
    </main>

    <footer>
      © <span id="year"></span> Headphones. Designed from a Figma file. All rights reserved.
    </footer>
  </div>

  <script>
    // small script to keep year current
    document.getElementById('year').textContent = new Date().getFullYear();

    // make all links with href starting with # smooth scroll
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', function(e){
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if(target) target.scrollIntoView({behavior:'smooth', block:'start'});
      });
    });
  </script>

</body>
</html>
