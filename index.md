---
layout: splash
title: ""
feature_row: []
feature_row2: []
---

<style>
  /* Global justification – but keep headings and buttons left */
  /** {
    text-align: justify !important;
  */}
  h1, h2, h3, h4, h5, h6, .btn, nav, .masthead, .page__hero-caption {
    text-align: left !important;
  }

  /* Hide any lingering page title on the splash layout */
  .splash .page__title {
    display: none !important;
  }

  /* Also hide any heading that might be inside .page__hero */
  .splash .page__hero h1,
  .splash .page__hero .page__title {
    display: none !important;
  }
</style>

<style>
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

  /* ========== CAROUSEL STYLES ========== */
  .carousel-container {
    position: relative;
    width: 100%;
    height: 500px;
    overflow: hidden;
    background: #0a1a2a;
  }
  .carousel-slide {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    transition: opacity 1s ease-in-out;
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .carousel-slide.active {
    opacity: 1;
  }
  .carousel-caption {
    background: rgba(0,0,0,0.6);
    color: white;
    padding: 1rem 2rem;
    border-radius: 8px;
    text-align: center;
    max-width: 80%;
  }
  .carousel-caption h2 {
    margin: 0 0 0.5rem;
    color: white;
  }
  .carousel-caption p {
    margin: 0;
  }
  .carousel-dots {
    position: absolute;
    bottom: 20px;
    left: 0;
    right: 0;
    text-align: center;
    z-index: 10;
  }
  .carousel-dot {
    display: inline-block;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: rgba(255,255,255,0.5);
    margin: 0 6px;
    cursor: pointer;
    transition: background 0.2s;
  }
  .carousel-dot.active {
    background: white;
  }
</style>

<!-- ========== HERO: AUTO-ROTATING CONCEPT CAROUSEL ========== -->
<div class="carousel-container" id="conceptCarousel">
  <div class="carousel-slide" style="background-image: url('/assets/images/co2_storage.png');">
    <div class="carousel-caption">
      <h2>CO₂ Storage Modelling</h2>
      <!--<p>Plume migration, trap integrity, geochemical trapping</p>
    </div>
  </div>
  <div class="carousel-slide" style="background-image: url('/assets/images/h2_storage.png');">
    <div class="carousel-caption">
      <h2>Hydrogen Storage Simulation</h2>
      <!--<p>Cyclic injection, cushion gas, geochemical reactivity</p>
    </div>
  </div>
  <div class="carousel-slide" style="background-image: url('/assets/images/reservoir_performance.png');">
    <div class="carousel-caption">
      <h2>Upstream Oil & Gas Solutions</h2>
      <!--<p>EOR, reservoir performance, decline curve analysis, history matching</p>
    </div>
  </div>
  <div class="carousel-dots" id="carouselDots"></div>
</div>

<script>
  (function() {
    const slides = document.querySelectorAll('.carousel-slide');
    const dotsContainer = document.getElementById('carouselDots');
    let current = 0;
    let interval;

    // Clear any existing dots (if re-running script)
    if (dotsContainer) dotsContainer.innerHTML = '';

    // Create dots
    slides.forEach((_, idx) => {
      const dot = document.createElement('span');
      dot.classList.add('carousel-dot');
      if (idx === 0) dot.classList.add('active');
      dot.addEventListener('click', () => {
        clearInterval(interval);
        showSlide(idx);
        startInterval();
      });
      dotsContainer.appendChild(dot);
    });

    function showSlide(index) {
      slides.forEach((slide, i) => {
        slide.classList.remove('active');
        if (dotsContainer.children[i]) dotsContainer.children[i].classList.remove('active');
      });
      slides[index].classList.add('active');
      if (dotsContainer.children[index]) dotsContainer.children[index].classList.add('active');
      current = index;
    }

    function nextSlide() {
      const next = (current + 1) % slides.length;
      showSlide(next);
    }

    function startInterval() {
      interval = setInterval(nextSlide, 5000);
    }

    const container = document.getElementById('conceptCarousel');
    if (container) {
      container.addEventListener('mouseenter', () => clearInterval(interval));
      container.addEventListener('mouseleave', startInterval);
    }

    // Show the first slide immediately
    showSlide(0);
    startInterval();
  })();
</script>

<!-- Blue gradient bar -->
<div style="background: linear-gradient(135deg, #0a2540 0%, #1a3a5a 100%); color: white; padding: 2rem; text-align: justify;">
  <p style="font-size:1.2rem; margin: 0; text-align: justify;">Precision simulation for subsurface energy systems. Empowering engineers through advanced modelling and open-source training.</p>
  <div style="margin-top:1.5rem; text-align: justify;">
    <a href="/services/" class="btn btn--primary" style="margin-right: 1rem;">Explore Services</a>
    <a href="/contact/" class="btn btn--light-outline">Contact Us</a>
  </div>
</div>

<!-- ========== ROTATING MISSION/VISION/VALUES ========== -->
<div class="rotator-container" id="rotator">
  <div class="rotator-item active" data-index="0">
    <h3 style="text-align: left;">Our Mission</h3>
    <p style="font-size: 1.1rem; text-align: justify;">To support informed subsurface decision-making through advanced modelling, simulation, and technical expertise across the energy sector.</p>
  </div>
  <div class="rotator-item" data-index="1">
    <h3 style="text-align: left;">Our Vision</h3>
    <p style="font-size: 1.1rem; text-align: justify;">To shape the future of subsurface energy through innovation, technical expertise, and scientifically grounded solutions.</p>
  </div>
  <div class="rotator-item" data-index="2">
    <div style="text-align: left;">
      <h3>Our Core Values</h3>
      <ul style="font-size: 1.1rem; text-align: left; list-style-type: none; padding-left: 0; margin: 0;">
        <li style="margin-bottom: 0.5rem;">Scientific Rigor</li>
        <li style="margin-bottom: 0.5rem;">Simulation Integrity</li>
        <li style="margin-bottom: 0.5rem;">Innovation</li>
        <li style="margin-bottom: 0.5rem;">Collaborative Excellence</li>
        <li>Practical Impact</li>
      </ul>
    </div>
  </div>
  <div class="rotator-dots" id="rotatorDots"></div>
</div>

<script>
  (function() {
    const items = document.querySelectorAll('.rotator-item');
    const dotsContainer = document.getElementById('rotatorDots');
    let current = 0;
    let interval;

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

    const container = document.getElementById('rotator');
    container.addEventListener('mouseenter', () => clearInterval(interval));
    container.addEventListener('mouseleave', startInterval);

    startInterval();
  })();
</script>

<!-- ========== SERVICES SECTION (CLICKABLE CARDS WITH HOVER) ========== -->
<h2 style="text-align: left; margin: 3rem 0 1.5rem;">Our Core Services</h2>
<div class="services-grid">
  <a href="/services/co2-storage/" class="service-card">
    <h3>CO₂ Storage</h3>
    <p>Plume migration, trap integrity, geochemical trapping.</p>
    <span class="metric">↓ 40% leakage risk</span>
  </a>
  <a href="/services/h2-storage/" class="service-card">
    <h3>H₂ Storage</h3>
    <p>Cyclic injection, cushion gas, geochemical reactivity.</p>
    <span class="metric">↑ 25% efficiency</span>
  </a>
  <a href="/services/upstream-oil-gas/" class="service-card">
    <h3>Upstream Oil & Gas</h3>
    <p>EOR, reservoir performance, decline curve analysis, history matching, field forecasts.</p>
    <span class="metric">↑ 34% recovery & accurate forecasts</span>
  </a>
  <a href="/services/student-projects/" class="service-card">
    <h3>Student Project Support</h3>
    <p>BSc, MSc, PhD modelling help & mentorship.</p>
    <span class="metric">🎓 1-on-1 coaching</span>
  </a>
  <a href="/services/training/" class="service-card">
    <h3>Open‑Source Training</h3>
    <p>MRST, PFLOTRAN, PHREEQC workshops – online & live.</p>
    <span class="metric">💻 Hands‑on</span>
  </a>
</div>

<!-- ========== WHY CHOOSE STRATAFLUX ENERGY ========== -->
<h2 style="text-align: center; margin: 3rem 0 1.5rem;">
  Why Choose StrataFlux Energy?
</h2>

<div style="display: flex; gap: 2rem; flex-wrap: wrap; justify-content: center; margin-bottom: 3rem;">

  <div style="flex: 1; min-width: 220px; text-align: center; padding: 1rem;">
    <div style="font-size: 2.5rem;">⬢</div>
    <h3>Advanced Technical Expertise</h3>
    <p>
      Delivering high-quality subsurface modelling, reactive transport simulation, and reservoir forecasting grounded in scientific and engineering rigor.
    </p>
  </div>

  <div style="flex: 1; min-width: 220px; text-align: center; padding: 1rem;">
    <div style="font-size: 2.5rem;">⬢</div>
    <h3>Decision-Focused Modelling</h3>
    <p>
      Simulation workflows are designed to support technical decision-making, uncertainty evaluation, risk reduction, and reservoir performance optimization.
    </p>
  </div>

  <div style="flex: 1; min-width: 220px; text-align: center; padding: 1rem;">
    <div style="font-size: 2.5rem;">⬢</div>
    <h3>Collaborative Technical Support</h3>
    <p>
      Working closely with clients, researchers, and students through transparent communication, tailored workflows, and practical technical guidance.
    </p>
  </div>
</div>

<!-- ========== TESTIMONIALS ========== -->
<!--<h2 style="text-align: center; margin-top: 2rem;">What Our Clients Say</h2>
<div style="display: flex; gap: 2rem; flex-wrap: wrap; justify-content: center; margin: 2rem 0;">
  <div style="flex: 1; min-width: 250px; background: #f0f0f0; padding: 1.5rem; border-radius: 8px;">
    <p style="font-style: italic;">“StrataFlux Energy’s simulation insights helped us reduce exploration uncertainty by 30%.”</p>
    <p style="margin-bottom: 0; font-weight: bold;">— Jones, Geoworks Ltd</p>
  </div>
  <div style="flex: 1; min-width: 250px; background: #f0f0f0; padding: 1.5rem; border-radius: 8px;">
    <p style="font-style: italic;">“The CO₂ storage modelling was precise and delivered ahead of schedule.”</p>
    <p style="margin-bottom: 0; font-weight: bold;">— Chen, Carbon Works</p>
  </div>
</div>-->

<!-- ========== CLIENTS & PARTNERS ========== -->
<!--<h2 style="text-align: center; margin-top: 3rem;">Clients & Partners</h2>
<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2rem; align-items: center; margin: 2rem 0;">
  <img src="/assets/images/logo.jpg" alt="Client 1" style="max-width: 120px; height: auto;">
  <img src="/assets/images/logo.jpg" alt="Client 2" style="max-width: 120px; height: auto;">
  <img src="/assets/images/logo.jpg" alt="Client 3" style="max-width: 120px; height: auto;">
  <img src="/assets/images/logo.jpg" alt="Client 4" style="max-width: 120px; height: auto;">
</div>-->
