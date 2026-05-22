---
layout: splash
title: ""
header:
  overlay_color: "#1a1a2e"
  # No overlay_image – we use canvas instead
feature_row:
  - image_path: /resmod-solutions/assets/images/co2-storage.jpg
    alt: "CO₂ Storage"
    title: "CO₂ Storage"
    excerpt: '<span class="service-tag co2-tag">CO₂ Storage</span> Reduce leakage risk by up to 40% with certified plume migration and geochemical trapping models.'
    url: /resmod-solutions/services/co2-storage/
    btn_label: "Learn More"
    btn_class: "btn--primary"
  - image_path: /resmod-solutions/assets/images/h2-storage.jpg
    alt: "H₂ Storage"
    title: "H₂ Storage"
    excerpt: '<span class="service-tag h2-tag">H₂ Storage</span> Optimise cushion gas and maintain integrity through advanced cyclic injection simulation.'
    url: /resmod-solutions/services/h2-storage/
    btn_label: "Learn More"
    btn_class: "btn--primary"
  - image_path: /resmod-solutions/assets/images/eor.jpg
    alt: "EOR"
    title: "EOR"
    excerpt: '<span class="service-tag eor-tag">EOR</span> Increase recovery factors by 15–34% with waterflood, gas injection, and chemical EOR forecasting.'
    url: /resmod-solutions/services/eor/
    btn_label: "Learn More"
    btn_class: "btn--primary"
feature_row2:
  - image_path: /resmod-solutions/assets/images/reservoir-performance.jpg
    alt: "Reservoir Performance"
    title: "Reservoir Performance"
    excerpt: '<span class="service-tag reservoir-tag">Reservoir Performance</span> Improve field development decisions with decline curve analysis and history matching.'
    url: /resmod-solutions/services/reservoir-performance/
    btn_label: "Learn More"
    btn_class: "btn--primary"
  - image_path: /resmod-solutions/assets/images/student-project.jpg
    alt: "Student Projects"
    title: "Student Project Assistance"
    excerpt: '<span class="service-tag student-tag">Student Support</span> One-on-one modelling mentorship for BSc, MSc, and PhD researchers.'
    url: /resmod-solutions/services/student-projects/
    btn_label: "Support"
    btn_class: "btn--primary"
  - image_path: /resmod-solutions/assets/images/training-workshop.jpg
    alt: "Training"
    title: "Open-Source Training"
    excerpt: '<span class="service-tag training-tag">Training</span> Hands‑on MRST, PFLOTRAN, and PHREEQC workshops – online & live.'
    url: /resmod-solutions/services/training/
    btn_label: "View Workshops"
    btn_class: "btn--primary"
---

<style>
  /* Global justification – but keep headings and buttons left */
  * {
    text-align: justify !important;
  }
  h1, h2, h3, h4, h5, h6, .btn, nav, .masthead, .page__hero-caption {
    text-align: left !important;
  }

  /* ========== SERVICE CARD ENHANCEMENTS ========== */
  .feature__item {
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    border-radius: 12px;
    overflow: hidden;
  }
  .feature__item:hover {
    transform: translateY(-6px);
    box-shadow: 0 12px 24px rgba(0,0,0,0.1);
  }

  /* Service tag base style */
  .service-tag {
    display: inline-block;
    font-size: 0.7rem;
    font-weight: bold;
    padding: 0.2rem 0.7rem;
    border-radius: 20px;
    margin-bottom: 0.6rem;
    letter-spacing: 0.5px;
    color: white;
  }

  /* Color variants per service */
  .co2-tag { background-color: #2c7da0; }
  .h2-tag { background-color: #61a5c2; }
  .eor-tag { background-color: #89c2d9; }
  .reservoir-tag { background-color: #a9d6e5; color: #1a1a2e; }
  .student-tag { background-color: #5f7f9e; }
  .training-tag { background-color: #3a6b8f; }

  /* Ensure excerpt text aligns nicely */
  .feature__item .archive__item-excerpt {
    margin-top: 0.5rem;
  }

  /* Hero text overlay on canvas – we'll manually add below canvas */
</style>

<!-- ========== DYNAMIC PARTICLE HERO (Canvas) ========== -->
<canvas id="heroCanvas" style="width:100%; height:500px; display:block; background:#0a1a2a;"></canvas>
<div style="background: linear-gradient(135deg, #0a1a2a 0%, #1a2a3a 100%); color: white; padding: 2rem; text-align: center; margin-top: -5px;">
  <h1 style="margin:0; font-size: 2.5rem;">ResMod Solutions</h1>
  <p style="font-size:1.2rem; max-width: 800px; margin: 1rem auto;">Precision simulation for subsurface energy systems – CO₂ geosequestration, H₂ storage, EOR, and reservoir performance.</p>
  <div style="margin-top:1.5rem;">
    <a href="/resmod-solutions/services/" class="btn btn--primary" style="margin-right: 1rem;">Explore Services</a>
    <a href="/resmod-solutions/services/student-projects/" class="btn btn--light-outline">Student Support</a>
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
      const count = Math.floor(width * height / 4000); // adaptive density
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
        // update
        p.x += p.vx;
        p.y += p.vy;
        // wrap around with subtle bounce? simpler: wrap
        if (p.x < 0) p.x = width;
        if (p.x > width) p.x = 0;
        if (p.y < 0) p.y = height;
        if (p.y > height) p.y = 0;
      }
      requestAnimationFrame(draw);
    }

    window.addEventListener('resize', () => { resizeCanvas(); });
    resizeCanvas();
    draw();
  })();
</script>

<!-- ========== CUSTOM SECOND HEADER (Original style but cleaner) ========== -->
<div style="background-color: #f8f9fa; padding: 2rem; margin-bottom: 2rem; border-radius: 8px; text-align: justify;">
  <h2 style="margin-bottom: 0.5rem;">Empowering Engineers Through Open‑Source Training</h2>
  <p style="font-size: 1.1rem; margin-bottom: 1rem;">We combine deep industry experience with practical, hands‑on workshops in MRST, PFLOTRAN, and PHREEQC.</p>
  <div>
    <a href="/resmod-solutions/training-hub/" class="btn btn--primary">View Workshops</a>
  </div>
</div>

<!-- Testimonials section -->
<h2 style="text-align: center; margin-top: 2rem;">What our clients say</h2>
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

<!-- Clients & Partners section -->
<h2 style="text-align: center; margin-top: 3rem;">Clients & Partners</h2>
<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2rem; align-items: center; margin: 2rem 0;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 1" style="max-width: 120px; height: auto;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 2" style="max-width: 120px; height: auto;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 3" style="max-width: 120px; height: auto;">
  <img src="/resmod-solutions/assets/images/logo.jpg" alt="Client 4" style="max-width: 120px; height: auto;">
</div>
