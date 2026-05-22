---
layout: splash
title: ""
header:
  overlay_color: "#1a1a2e"
feature_row: []
feature_row2: []
---

<style>
  /* Global justification – but keep headings and buttons left */
  * {
    text-align: justify !important;
  }
  h1, h2, h3, h4, h5, h6, .btn, nav, .masthead, .page__hero-caption {
    text-align: left !important;
  }

  /* ========== SERVICE CARD STYLES ========== */
  .service-card {
    flex: 1;
    min-width: 250px;
    background: white;
    border: 1px solid #e0e0e0;
    border-radius: 12px;
    padding: 1.5rem;
    transition: all 0.3s ease;
    cursor: pointer;
    text-decoration: none;
    color: inherit;
    display: block;
  }
  .service-card:hover {
    transform: translateY(-8px);
    background-color: #e6f0fa;
    box-shadow: 0 12px 24px rgba(0,0,0,0.1);
  }
  .service-card h3 {
    margin-top: 0;
    color: #1a3a5a;
    transition: color 0.2s;
  }
  .service-card:hover h3 {
    color: #0a2540;
  }
  .service-card .metric {
    font-size: 0.85rem;
    font-weight: bold;
    color: #2c7da0;
    margin-top: 0.5rem;
    display: inline-block;
    background: #eef2f7;
    padding: 0.2rem 0.6rem;
    border-radius: 20px;
  }
  .service-card:hover .metric {
    background: white;
  }

  /* ========== ROTATOR STYLES ========== */
  .rotator-container {
    background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
    border-radius: 12px;
    padding: 2rem;
    margin: 2rem 0;
    text-align: center;
    position: relative;
    min-height: 180px;
  }
  .rotator-item {
    display: none;
    animation: fadeIn 0.8s ease;
  }
  .rotator-item.active {
    display: block;
  }
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .rotator-dots {
    margin-top: 1rem;
  }
  .dot {
    display: inline-block;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: #ccc;
    margin: 0 5px;
    cursor: pointer;
    transition: background 0.2s;
  }
  .dot.active {
    background: #1a3a5a;
  }

  /* Ensure cards layout */
  .services-grid {
    display: flex;
    gap: 2rem;
    flex-wrap: wrap;
    justify-content: center;
    margin: 2rem 0;
  }
</style>

<!-- ========== HERO: ANIMATED PARTICLE CANVAS ========== -->
<canvas id="heroCanvas" style="width:100%; height:500px; display:block; background:#0a1a2a;"></canvas>
<div style="background: linear-gradient(135deg, #0a2540 0%, #1a3a5a 100%); color: white; padding: 2rem; text-align: center; margin-top: -5px;">
  <h1 style="margin:0; font-size: 2.5rem;">ResMod Solutions</h1>
  <p style="font-size:1.2rem; max-width: 800px; margin: 1rem auto;">Precision simulation for subsurface energy systems – CO₂ geosequestration, H₂ storage, EOR, and reservoir performance.</p>
  <div style="margin-top:1.5rem;">
    <a href="/resmod-solutions/services/" class="btn btn--primary" style="margin-right: 1rem;">Explore Services</a>
    <a href="/resmod-solutions/contact/" class="btn btn--light-outline">Contact Us</a>
  </div>
</div>

<script>
  (function() {
    const canvas = document.getElementById('heroCanvas');
    if (!canvas) return;
    const ctx = canvas.getContext('2d');
    let width, height;
    let particles = [];

    function resizeCanvas() {
      width = canvas.clientWidth;
      height = canvas.clientHeight;
      canvas.width = width;
      canvas.height = height;
      initParticles();
    }

    function initParticles() {
      particles = [];
      const count = Math.floor(width * height / 4000);
      for (let i = 0; i < count; i++) {
        particles.push({
          x: Math.random() * width,
          y: Math.random() * height,
          radius: Math.random() * 3 + 1,
          vx: (Math.random() - 0.5) * 0.8,
          vy: (Math.random() - 0.5) * 0.8 + 0.3,
          color: `hsl(${200 + Math.random() * 40}, 80%, 60%)`
        });
      }
    }

    function draw() {
      ctx.clearRect(0, 0, width, height);
      for (let p of particles) {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
        ctx.fillStyle = p.color;
        ctx.fill();
        p.x += p.vx;
        p.y += p.vy;
        if (p.x < 0) p.x = width;
        if (p.x > width) p.x = 0;
        if (p.y < 0) p.y = height;
        if (p.y > height) p.y = 0;
      }
      requestAnimationFrame(draw);
    }

    window.addEventListener('resize', () => resizeCanvas());
    resizeCanvas();
    draw();
  })();
</script>

<!-- ========== ROTATING MISSION/VISION/VALUES ========== -->
<div class="rotator-container" id="rotator">
  <div class="rotator-item active" data-index="0">
    <h3>Our Mission</h3>
    <p style="font-size: 1.1rem;">To develop advanced modelling solutions and foster technical expertise for carbon storage, hydrogen storage, EOR, and reservoir management, while empowering engineers through open-source training.</p>
  </div>
  <div class="rotator-item" data-index="1">
    <h3>Our Vision</h3>
    <p style="font-size: 1.1rem;">To be a trusted global partner in delivering reliable, science-driven subsurface energy solutions that advance the energy transition.</p>
  </div>
  <div class="rotator-item" data-index="2">
    <h3>Our Core Values</h3>
    <p style="font-size: 1.1rem;">🔬 Scientific Excellence &nbsp;&nbsp;|&nbsp;&nbsp; 🔧 Innovation &nbsp;&nbsp;|&nbsp;&nbsp; 🤝 Collaborative Precision &nbsp;&nbsp;|&nbsp;&nbsp; 🌍 Impact</p>
  </div>
  <div class="rotator-dots" id="rotatorDots"></div>
</div>

<script>
  (function() {
    const items = document.querySelectorAll('.rotator-item');
    const dotsContainer = document.getElementById('rotatorDots');
    let current = 0;
    let interval;

    // Create dots
    items.forEach((_, idx) => {
      const dot = document.createElement('span');
      dot.classList.add('dot');
      if (idx === 0) dot.classList.add('active');
      dot.addEventListener('click', () => {
        clearInterval(interval);
        showItem(idx);
        startInterval();
      });
      dotsContainer.appendChild(dot);
    });

    function showItem(index) {
      items.forEach((item, i) => {
        item.classList.remove('active');
        if (dotsContainer.children[i]) dotsContainer.children[i].classList.remove('active');
      });
      items[index].classList.add('active');
      if (dotsContainer.children[index]) dotsContainer.children[index].classList.add('active');
      current = index;
    }

    function nextItem() {
      const next = (current + 1) % items.length;
      showItem(next);
    }

    function startInterval() {
      interval = setInterval(nextItem, 5000);
    }

    // Pause on hover
    const container = document.getElementById('rotator');
    container.addEventListener('mouseenter', () => clearInterval(interval));
    container.addEventListener('mouseleave', startInterval);

    startInterval();
  })();
</script>

<!-- ========== SERVICES SECTION (CLICKABLE CARDS WITH HOVER) ========== -->
<h2 style="text-align: center; margin: 3rem 0 1.5rem;">Our Core Services</h2>
<div class="services-grid">
  <a href="/resmod-solutions/services/co2-storage/" class="service-card">
    <h3>CO₂ Storage</h3>
    <p>Plume migration, trap integrity, geochemical trapping.</p>
    <span class="metric">↓ 40% leakage risk</span>
  </a>
  <a href="/resmod-solutions/services/h2-storage/" class="service-card">
    <h3>H₂ Storage</h3>
    <p>Cyclic injection, cushion gas, geochemical reactivity.</p>
    <span class="metric">↑ 25% efficiency</span>
  </a>
  <a href="/resmod-solutions/services/eor/" class="service-card">
    <h3>Enhanced Oil Recovery</h3>
    <p>Waterflood, gas injection, chemical EOR forecasting.</p>
    <span class="metric">↑ 34% recovery factor</span>
  </a>
  <a href="/resmod-solutions/services/reservoir-performance/" class="service-card">
    <h3>Reservoir Performance</h3>
    <p>Decline curve analysis, history matching, field forecasts.</p>
    <span class="metric">📈 Accurate forecasts</span>
  </a>
  <a href="/resmod-solutions/services/student-projects/" class="service-card">
    <h3>Student Project Support</h3>
    <p>BSc, MSc, PhD modelling help & mentorship.</p>
    <span class="metric">🎓 1-on-1 coaching</span>
  </a>
  <a href="/resmod-solutions/services/training/" class="service-card">
    <h3>Open‑Source Training</h3>
    <p>MRST, PFLOTRAN, PHREEQC workshops – online & live.</p>
    <span class="metric">💻 Hands‑on</span>
  </a>
</div>

<!-- ========== WHY CHOOSE US (Simple icons) ========== -->
<h2 style="text-align: center; margin: 3rem 0 1.5rem;">Why Choose ResMod?</h2>
<div style="display: flex; gap: 2rem; flex-wrap: wrap; justify-content: center; margin-bottom: 3rem;">
  <div style="flex: 1; min-width: 200px; text-align: center; padding: 1rem;">
    <div style="font-size: 2.5rem;">⚙️</div>
    <h3>Technical Excellence</h3>
    <p>Rigorous, defensible modelling and deep industry expertise.</p>
  </div>
  <div style="flex: 1; min-width: 200px; text-align: center; padding: 1rem;">
    <div style="font-size: 2.5rem;">📚</div>
    <h3>Open-Source Focus</h3>
    <p>Training and solutions built on accessible, cutting-edge tools.</p>
  </div>
  <div style="flex: 1; min-width: 200px; text-align: center; padding: 1rem;">
    <div style="font-size: 2.5rem;">🤝</div>
    <h3>Client Partnership</h3>
    <p>Collaborative and transparent processes with tangible results.</p>
  </div>
</div>

<!-- ========== TESTIMONIALS ========== -->
<h2 style="text-align: center; margin-top: 2rem;">What Our Clients Say</h2>
<div style="display: flex; gap: 2rem; flex-wrap: wrap; justify-content: center; margin: 2rem 0;">
  <div style="flex: 1; min-width: 250px; background: #f0f0f0; padding: 1.5rem; border-radius: 8px;">
    <p style="font-style: italic;">“ResMod’s simulation insights helped us reduce exploration uncertainty by 30%.”</p>
    <p style="margin-bottom: 0; font-weight: bold;">— Jones, Geoworks Ltd</p>
  </div>
  <div style="flex: 1; min-width: 250px; background: #f0f0f0; padding: 1.5rem; border-radius: 8px;">
    <p style="font-style: italic;">“The CO₂ storage modelling was precise and delivered ahead of schedule.”</p>
    <p style="margin-bottom: 0; font-weight: bold;">— Chen, Carbon Works</p>
  </div>
</div>

<!-- ========== CLIENTS & PARTNERS ========== -->
<h2 style="text-align: center; margin-top: 3rem;">Clients & Partners</h2>
<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2rem; align-items: center; margin: 2rem 0;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 1" style="max-width: 120px; height: auto;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 2" style="max-width: 120px; height: auto;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 3" style="max-width: 120px; height: auto;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 4" style="max-width: 120px; height: auto;">
</div>
