# Ex02 Commercial Website
## NAME: DHANAAAKHAASH S.T
## REG NO: 212224240032

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM



    /* ---------- COLORS & UTILS ---------- */
    :root{
      --accent:#0f766e; /* teal-ish */
      --accent-2:#f97316; /* orange */
      --muted:#6b7280;
      --card-bg:#fff;
      --glass: rgba(255,255,255,0.6);
      --maxw:1200px;
    }

    .container{width:90%;max-width:var(--maxw);margin:0 auto}

    /* ---------- HEADER ---------- */
    header{
      background:linear-gradient(90deg, rgba(15,118,110,0.06), rgba(249,115,22,0.03));
      position:sticky;top:0;z-index:50;backdrop-filter: blur(6px);
      border-bottom:1px solid rgba(0,0,0,0.04);
    }
    .topbar{display:flex;align-items:center;justify-content:space-between;padding:16px 0}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:44px;height:44px;border-radius:8px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;color:white;font-weight:700}
    nav{display:flex;gap:18px;align-items:center}
    .cta{padding:8px 14px;border-radius:10px;background:var(--accent);color:white;font-weight:600}

    /* ---------- HERO ---------- */
    .hero{display:flex;gap:32px;align-items:center;padding:56px 0}
    .hero-left{flex:1;min-width:260px}
    .eyebrow{font-size:13px;color:var(--accent);font-weight:700;margin-bottom:12px}
    .hero h1{font-size:34px;line-height:1.05;margin-bottom:18px}
    .sub{color:var(--muted);margin-bottom:22px}
    .hero-cta{display:flex;gap:12px}
    .btn{padding:12px 18px;border-radius:10px;font-weight:700}
    .btn-primary{background:var(--accent);color:white}
    .btn-outline{border:2px solid var(--accent);color:var(--accent);background:transparent}

    .hero-right{flex:1;display:flex;align-items:center;justify-content:center}
    .mockup{width:320px;height:420px;border-radius:16px;background:linear-gradient(180deg,#fff,#f7f7f9);box-shadow:0 14px 30px rgba(15,118,110,0.08);display:flex;flex-direction:column;overflow:hidden}
    .mockup .image{flex:1;background:linear-gradient(135deg,#fde68a,#fb923c);display:flex;align-items:center;justify-content:center;font-size:22px;color:#222}
    .mockup .info{padding:14px;border-top:1px solid rgba(0,0,0,0.04)}

    /* ---------- PRODUCT GRID ---------- */
    .products{padding:36px 0}
    .products-header{display:flex;align-items:center;justify-content:space-between;margin-bottom:18px}
    .grid{display:flex;flex-wrap:wrap;gap:18px}
    .card{flex:1 1 calc(33.333% - 18px);background:var(--card-bg);border-radius:12px;overflow:hidden;box-shadow:0 8px 20px rgba(13,18,25,0.03);min-width:230px}
    .card .thumb{height:180px;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#fca5a5,#fbcfe8);font-weight:700}
    .card .body{padding:14px}
    .price-row{display:flex;align-items:center;justify-content:space-between;margin-top:8px}
    .price{font-weight:800}
    .tag{font-size:12px;color:var(--muted);padding:6px 8px;border-radius:8px;border:1px solid rgba(0,0,0,0.04)}

    /* ---------- FEATURES / ABOUT ---------- */
    .features{display:flex;gap:18px;align-items:stretch;padding:18px 0}
    .feature{flex:1;background:linear-gradient(180deg,#fff,#fcfcfd);padding:18px;border-radius:12px;display:flex;gap:12px;align-items:flex-start}
    .feature .icon{width:44px;height:44;border-radius:10px;background:var(--glass);display:flex;align-items:center;justify-content:center}

    /* ---------- FOOTER ---------- */
    footer{padding:32px 0;border-top:1px solid rgba(0,0,0,0.04);margin-top:24px}
    .foot-grid{display:flex;flex-wrap:wrap;gap:18px}
    .col{flex:1 1 200px}

    /* ---------- RESPONSIVE ---------- */
    @media(max-width:880px){
      .hero{flex-direction:column}
      .card{flex:1 1 calc(50% - 18px)}
      .mockup{width:260px;height:340px}
    }
    @media(max-width:560px){
      nav{display:none}
      .card{flex:1 1 100%}
      .topbar{padding:12px 0}
      .hero{padding:28px 0}
      .hero h1{font-size:26px}
    }

    /* ---------- SMALL HELPERS ---------- */
    .muted{color:var(--muted)}
    .center{text-align:center}
 

      <nav>
        <a href="#products">Products</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
        <a class="cta" href="#checkout">Cart (0)</a>
      </nav>
    </div>
  
      <div class="hero-right">
        <div class="mockup" role="img" aria-label="product mockup">
          <div class="image">Featured Jacket</div>
          <div class="info">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div>
                <div style="font-weight:800">CityTrail Jacket</div>
                <div class="muted" style="font-size:13px">Windproof · Water resistant</div>
              </div>
              <div style="text-align:right">
                <div style="font-weight:800">₹3,299</div>
                <div style="font-size:12px;color:var(--muted)">Limited</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- PRODUCTS -->
    <section id="products" class="products">
      <div class="products-header">
        <h2>Popular items</h2>
        <div class="muted">Showing 6 items</div>
      </div>

      <div class="grid">
        <!-- Card 1 -->
        <article class="card">
          <div class="thumb">Classic Tee</div>
          <div class="body">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:700">Classic Logo Tee</div>
              <div class="tag">S-XL</div>
            </div>
            <div class="price-row">
              <div class="price">₹799</div>
              <a class="btn btn-outline" href="#checkout">Buy</a>
            </div>
          </div>
        </article>

        <!-- Card 2 -->
        <article class="card">
          <div class="thumb">Hoodie</div>
          <div class="body">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:700">Oversized Hoodie</div>
              <div class="tag">Unisex</div>
            </div>
            <div class="price-row">
              <div class="price">₹1,499</div>
              <a class="btn btn-outline" href="#checkout">Buy</a>
            </div>
          </div>
        </article>

        <!-- Card 3 -->
        <article class="card">
          <div class="thumb">Sneakers</div>
          <div class="body">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:700">Retro Runner</div>
              <div class="tag">Limited</div>
            </div>
            <div class="price-row">
              <div class="price">₹3,999</div>
              <a class="btn btn-outline" href="#checkout">Buy</a>
            </div>
          </div>
        </article>

        <!-- Card 4 -->
        <article class="card">
          <div class="thumb">Jacket</div>
          <div class="body">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:700">CityTrail Jacket</div>
              <div class="tag">Waterproof</div>
            </div>
            <div class="price-row">
              <div class="price">₹3,299</div>
              <a class="btn btn-outline" href="#checkout">Buy</a>
            </div>
          </div>
        </article>

        <!-- Card 5 -->
        <article class="card">
          <div class="thumb">Cap</div>
          <div class="body">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:700">Everyday Cap</div>
              <div class="tag">Adjustable</div>
            </div>
            <div class="price-row">
              <div class="price">₹499</div>
              <a class="btn btn-outline" href="#checkout">Buy</a>
            </div>
          </div>
        </article>

        <!-- Card 6 -->
        <article class="card">
          <div class="thumb">Backpack</div>
          <div class="body">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div style="font-weight:700">Daypack</div>
              <div class="tag">20L</div>
            </div>
            <div class="price-row">
              <div class="price">₹2,199</div>
              <a class="btn btn-outline" href="#checkout">Buy</a>
            </div>
          </div>
        </article>
      </div>
    </section>

    <!-- FEATURES / ABOUT -->
    <section id="about">
      <h2>Why choose Stumps?</h2>
      <div class="features" style="margin-top:12px">
        <div class="feature">
          <div class="icon">✓</div>
          <div>
            <div style="font-weight:700">Sustainable materials</div>
            <div class="muted" style="font-size:13px">We use recycled fibers and low-impact dyes.</div>
          </div>
        </div>

        <div class="feature">
          <div class="icon">⚡</div>
          <div>
            <div style="font-weight:700">Fast shipping</div>
            <div class="muted" style="font-size:13px">Ships within 24–48 hours across India.</div>
          </div>
        </div>

        <div class="feature">
          <div class="icon">🔁</div>
          <div>
            <div style="font-weight:700">Easy returns</div>
            <div class="muted" style="font-size:13px">30-day no-questions returns policy.</div>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT / FOOTER -->
    <section id="contact" style="margin-top:28px">
      <div style="display:flex;gap:18px;align-items:flex-start;flex-wrap:wrap">
        <form style="flex:1;min-width:260px;background:linear-gradient(180deg,#fff,#fbfbfd);padding:18px;border-radius:10px">
          <h3>Contact us</h3>
          <p class="muted" style="margin-bottom:10px">Questions about sizing, shipping, or wholesale?</p>
          <label style="display:block;margin-bottom:8px;font-size:13px">Your name</label>
          <input type="text" placeholder="Name" style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.06);margin-bottom:10px" />
          <label style="display:block;margin-bottom:8px;font-size:13px">Email</label>
          <input type="email" placeholder="you@example.com" style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.06);margin-bottom:10px" />
          <label style="display:block;margin-bottom:8px;font-size:13px">Message</label>
          <textarea rows="4" placeholder="How can we help?" style="width:100%;padding:10px;border-radius:8px;border:1px solid rgba(0,0,0,0.06);"></textarea>
          <div style="margin-top:12px;text-align:right"><button class="btn btn-primary">Send message</button></div>
        </form>

        <div style="flex:1;min-width:260px">
          <h3>Store Info</h3>
          <p class="muted">Stumps Clothing Co.<br/>Chennai, India<br/>support@stumps.co</p>

          <h4 style="margin-top:14px">Opening hours</h4>
          <p class="muted">Mon—Sat: 10:00 — 19:00<br/>Sun: Closed</p>
        </div>
      </div>
    </section>

    <footer>
      <div class="container foot-grid">
        <div class="col">
          <div style="font-weight:800">STUMPS</div>
          <div class="muted" style="font-size:13px;margin-top:8px">© 2025 Stumps Clothing Co. All rights reserved.</div>
        </div>
        <div class="col">
          <div style="font-weight:700">Company</div>
          <div class="muted" style="margin-top:8px">About · Careers · Press</div>
        </div>
        <div class="col">
          <div style="font-weight:700">Support</div>
          <div class="muted" style="margin-top:8px">Contact · Shipping · Returns</div>
        </div>
      </div>
    </footer>
  
</html>



## OUTPUT

<img width="1409" height="979" alt="Screenshot 2025-08-13 213609" src="https://github.com/user-attachments/assets/f61edc7d-f7be-4834-87b3-425b233a0e10" />

<img width="1329" height="893" alt="Screenshot 2025-08-13 213622" src="https://github.com/user-attachments/assets/176dc3d1-94e5-4908-85f5-9391a64a752c" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
