---
layout: splash
title: ""
feature_row: []
feature_row2: []
---

<style>
  .splash .page__title,
  .splash .page__hero h1,
  .splash .page__hero .page__title {
    display: none !important;
  }

  :root {
    --sf-navy: #0a2540;
    --sf-blue: #1a3a5a;
    --sf-green: #63b32e;
    --sf-cyan: #2c7da0;
    --sf-light: #f3f5f7;
    --sf-text: #1f2933;
    --sf-muted: #5f6b7a;
    --sf-border: #d9e2ec;
  }

  .sf-section {
    padding: 3.5rem 1.5rem;
  }

  .sf-container {
    max-width: 1180px;
    margin: 0 auto;
  }

  .sf-section-title {
    font-size: 2rem;
    margin-bottom: 1rem;
    color: var(--sf-navy);
  }

  .sf-section-intro {
    font-size: 1.12rem;
    color: var(--sf-muted);
    max-width: 850px;
    line-height: 1.7;
  }

    .sf-section-intro_2 {
    font-size: 1.12rem;
    color: var(--sf-muted);
    max-width: 850px;
    line-height: 1.7;
    text-align: justify;
  }

  .carousel-container {
    position: relative;
    width: 100%;
    height: 560px;
    overflow: hidden;
    background: #0a1a2a;
  }

  .carousel-slide {
    position: absolute;
    inset: 0;
    opacity: 0;
    transition: opacity 1s ease-in-out;
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
  }

  .carousel-slide::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(90deg, rgba(5, 20, 36, 0.88), rgba(5, 20, 36, 0.35), rgba(5, 20, 36, 0.05));
  }

  .carousel-slide.active {
    opacity: 1;
  }

  .carousel-caption {
    position: relative;
    z-index: 2;
    color: white;
    max-width: 680px;
    padding: 4rem;
  }

  .carousel-caption h1 {
    font-size: 3.2rem;
    line-height: 1.05;
    margin-bottom: 1rem;
    color: white;
  }

  .carousel-caption p {
    font-size: 1.25rem;
    line-height: 1.6;
    margin-bottom: 1.5rem;
  }

  .sf-eyebrow {
    color: var(--sf-green);
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
  }

  .carousel-dots {
    position: absolute;
    bottom: 22px;
    left: 4rem;
    z-index: 10;
  }

  .carousel-dot {
    display: inline-block;
    width: 13px;
    height: 13px;
    border-radius: 50%;
    background: rgba(255,255,255,0.45);
    margin-right: 8px;
    cursor: pointer;
  }

  .carousel-dot.active {
    background: var(--sf-green);
  }

  .sf-hero-buttons a {
    margin-right: 0.8rem;
    margin-bottom: 0.8rem;
  }

  .sf-positioning {
    background: linear-gradient(135deg, #0a2540 0%, #1a3a5a 100%);
    color: white;
  }

  .sf-positioning p {
    font-size: 1.25rem;
    line-height: 1.7;
    max-width: 980px;
    margin: 0;
  }

  .who-grid {
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 2.5rem;
    align-items: center;
  }

  .who-card {
    background: white;
    border: 1px solid var(--sf-border);
    border-radius: 16px;
    padding: 2rem;
    box-shadow: 0 12px 30px rgba(10, 37, 64, 0.08);
  }

  .who-card h3 {
    margin-top: 0;
    color: var(--sf-navy);
  }

  .who-card ul {
    margin: 0;
    padding-left: 1.2rem;
    line-height: 1.8;
  }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }

  .service-card {
    background: white;
    border: 1px solid var(--sf-border);
    border-radius: 16px;
    overflow: hidden;
    text-decoration: none;
    color: inherit;
    display: flex;
    flex-direction: column;
    box-shadow: 0 10px 24px rgba(10, 37, 64, 0.07);
    transition: all 0.25s ease;
  }

  .service-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 18px 34px rgba(10, 37, 64, 0.13);
  }

  .service-card img {
    width: 100%;
    height: 210px;
    object-fit: cover;
  }

  .service-card-body {
    padding: 1.4rem;
  }

  .service-card h3 {
    margin-top: 0;
    color: var(--sf-navy);
  }

  .service-card p {
    color: var(--sf-muted);
    line-height: 1.65;
  }

  .metric {
    display: inline-block;
    margin-top: 0.5rem;
    background: #eef7ee;
    color: #2f7d32;
    font-size: 0.82rem;
    font-weight: 700;
    padding: 0.35rem 0.75rem;
    border-radius: 999px;
  }

  .why-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }

  .why-card {
    background: #ffffff;
    border: 1px solid var(--sf-border);
    border-radius: 16px;
    padding: 1.7rem;
    box-shadow: 0 10px 24px rgba(10, 37, 64, 0.06);
  }

  .why-icon {
    width: 46px;
    height: 46px;
    border-radius: 12px;
    background: linear-gradient(135deg, var(--sf-green), #2f7d32);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.4rem;
    margin-bottom: 1rem;
  }

  .why-card h3 {
    margin-top: 0;
    color: var(--sf-navy);
  }

  .why-card p {
    color: var(--sf-muted);
    line-height: 1.65;
  }

  .support-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }

  .support-card {
    background: #f8fafc;
    border: 1px solid var(--sf-border);
    border-radius: 16px;
    padding: 2rem;
  }

  .support-card h3 {
    color: var(--sf-navy);
    margin-top: 0;
  }

  .support-card p {
    color: var(--sf-muted);
    line-height: 1.65;
  }

  .cta-section {
    background: linear-gradient(135deg, #071b2f 0%, #0a2540 55%, #143f2c 100%);
    color: white;
    text-align: center;
    padding: 4rem 1.5rem;
    border-radius: 0;
    text-align: justify;
  }

  .cta-section h2 {
    color: white;
    font-size: 2.2rem;
    margin-bottom: 1rem;
  }

  .cta-section p {
    max-width: 760px;
    margin: 0 auto 1.8rem;
    font-size: 1.15rem;
    line-height: 1.7;
  }

  @media (max-width: 900px) {
    .carousel-container {
      height: 520px;
    }

    .carousel-caption {
      padding: 2rem;
    }

    .carousel-caption h1 {
      font-size: 2.3rem;
    }

    .who-grid,
    .services-grid,
    .why-grid,
    .support-grid {
      grid-template-columns: 1fr;
    }

    .carousel-dots {
      left: 2rem;
    }
  }
</style>

<!-- ========== HERO CAROUSEL ========== -->
<div class="carousel-container" id="conceptCarousel">

  <div class="carousel-slide" style="background-image: url('/assets/images/co-storage.png');">
    <div class="carousel-caption">
      <div class="sf-eyebrow">Carbon Storage</div>
      <h1>Advanced CO₂ Storage Modelling</h1>
      <p>Science-driven modelling workflows for storage screening, plume migration, injectivity, trapping mechanisms, and long-term subsurface performance.</p>
      <div class="sf-hero-buttons">
        <a href="/services/co2-storage/" class="btn btn--primary">Explore CO₂ Storage</a>
        <a href="/contact/" class="btn btn--light-outline">Discuss a Project</a>
      </div>
    </div>
  </div>

  <div class="carousel-slide" style="background-image: url('/assets/images/h2-storage.png');">
    <div class="carousel-caption">
      <div class="sf-eyebrow">Hydrogen Storage</div>
      <h1>Underground H₂ Storage Simulation</h1>
      <p>Technical modelling for cushion gas behaviour, cyclic injection and withdrawal, containment risk, geochemical reactivity, and storage performance.</p>
      <div class="sf-hero-buttons">
        <a href="/services/h2-storage/" class="btn btn--primary">Explore H₂ Storage</a>
        <a href="/contact/" class="btn btn--light-outline">Request Support</a>
      </div>
    </div>
  </div>

  <div class="carousel-slide" style="background-image: url('/assets/images/reservoir_performance.png');">
    <div class="carousel-caption">
      <div class="sf-eyebrow">Upstream Oil & Gas</div>
      <h1>Reservoir Performance Forecasting</h1>
      <p>Integrated simulation, history matching, decline analysis, EOR evaluation, and uncertainty assessment to support better reservoir decisions.</p>
      <div class="sf-hero-buttons">
        <a href="/services/upstream-oil-gas/" class="btn btn--primary">Explore Forecasting</a>
        <a href="/contact/" class="btn btn--light-outline">Contact Us</a>
      </div>
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

    if (dotsContainer) dotsContainer.innerHTML = '';

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
      showSlide((current + 1) % slides.length);
    }

    function startInterval() {
      interval = setInterval(nextSlide, 6000);
    }

    const container = document.getElementById('conceptCarousel');
    if (container) {
      container.addEventListener('mouseenter', () => clearInterval(interval));
      container.addEventListener('mouseleave', startInterval);
    }

    showSlide(0);
    startInterval();
  })();
</script>

<!-- ========== BLUE GRADIENT, POSITIONING BAR ========== -->
<section class="sf-positioning sf-section" style="padding: 1.5rem 1.5rem; text-align: justify">
  <div class="sf-container">
    <p>
      StrataFlux Energy provides advanced subsurface modelling, simulation, and technical advisory services for carbon storage, hydrogen storage, upstream oil and gas, and reservoir performance forecasting.
    </p>
    <div style="margin-top:1.5rem;">
      <a href="/services/" class="btn btn--primary" style="margin-right: 1rem;">Explore Services</a>
      <a href="/contact/" class="btn btn--light-outline">Discuss a Project</a>
    </div>
  </div>
</section>

<!-- ========== WHO WE ARE ========== -->
<section class="sf-section">
  <div class="sf-container who-grid">
    <div>
      <h2 class="sf-section-title">Who We Are</h2>
      <p class="sf-section-intro_2">
        StrataFlux Energy is an independent subsurface consultancy focused on advanced modelling, simulation, and technical analysis for carbon and hydrogen storage, as well as upstream oil & gas systems.
      </p>
      <p class="sf-section-intro_2">
        We deliver scientifically rigorous reservoir simulation, reactive transport modelling, geochemical analysis, and computational workflows that support informed decision-making across the energy sector. Our work helps clients evaluate subsurface performance, reduce uncertainty, and better understand complex flow and storage processes.
      </p>
    </div>

    <div class="who-card">
      <h3>Technical Focus</h3>
      <ul>
        <li>Reservoir simulation and forecasting</li>
        <li>CO₂ storage performance assessment</li>
        <li>Underground hydrogen storage modelling</li>
        <li>Reactive transport and geochemical analysis</li>
        <li>Uncertainty and sensitivity evaluation</li>
      </ul>
    </div>
  </div>
</section>

<!-- ========== CORE SERVICES ========== -->
<section class="sf-section" style="background: var(--sf-light);">
  <div class="sf-container">
    <h2 class="sf-section-title">Core Consultancy Services</h2>
    <p class="sf-section-intro_2">
      We provide specialist modelling and simulation support for complex subsurface energy challenges, from early-stage screening to technical decision support and performance forecasting.
    </p>

    <div class="services-grid">

      <a href="/services/co2-storage/" class="service-card">
        <img src="/assets/images/co2_storage.png" alt="CO₂ storage modelling">
        <div class="service-card-body">
          <h3>CO₂ Storage Modelling</h3>
          <p>Storage screening, injectivity assessment, plume migration, trapping mechanisms, caprock considerations, and long-term storage performance.</p>
          <span class="metric">Modelling & Simulation</span>
        </div>
      </a>

      <a href="/services/h2-storage/" class="service-card">
        <img src="/assets/images/h2_storage.png" alt="Hydrogen storage simulation">
        <div class="service-card-body">
          <h3>Hydrogen Storage Simulation</h3>
          <p>Underground H₂ storage modelling, cushion gas behaviour, cyclic operation, containment risk, geochemical reactivity, and performance evaluation.</p>
          <span class="metric">Storage Performance</span>
        </div>
      </a>

      <a href="/services/upstream-oil-gas/" class="service-card">
        <img src="/assets/images/reservoir_performance.png" alt="Reservoir performance forecasting">
        <div class="service-card-body">
          <h3>Upstream Oil & Gas</h3>
          <p>EOR studies, reservoir forecasting, history matching, decline curve analysis, field performance evaluation, and development scenario testing.</p>
          <span class="metric">Forecasting & Optimization</span>
        </div>
      </a>

    </div>
  </div>
</section>

<!-- ========== WHY CHOOSE STRATAFLUX ENERGY ========== -->
<section class="sf-section">
  <div class="sf-container">
    <h2 class="sf-section-title">Why Choose StrataFlux Energy?</h2>
    <p class="sf-section-intro_2">
      Our approach combines technical depth, scientific rigor, and practical engineering insight to deliver modelling outcomes that clients can trust.
    </p>

    <div class="why-grid">

      <div class="why-card">
        <div class="why-icon">▣</div>
        <h3>Advanced Technical Expertise</h3>
        <p>Delivering high-quality subsurface modelling, reactive transport simulation, and reservoir forecasting grounded in scientific and engineering rigor.</p>
      </div>

      <div class="why-card">
        <div class="why-icon">⌁</div>
        <h3>Decision-Focused Modelling</h3>
        <p>Simulation workflows designed to support technical decision-making, uncertainty evaluation, risk reduction, and reservoir performance optimization.</p>
      </div>

      <div class="why-card">
        <div class="why-icon">◎</div>
        <h3>Collaborative Technical Support</h3>
        <p>Working closely with clients, researchers, and technical teams through transparent communication, tailored workflows, and practical technical guidance.</p>
      </div>

    </div>
  </div>
</section>

<!-- ========== TRAINING AND RESEARCH SUPPORT ========== -->
<section class="sf-section" style="background: var(--sf-light);">
  <div class="sf-container">
    <h2 class="sf-section-title">Training, Research Support, and Capacity Development</h2>
    <p class="sf-section-intro_2">
      Beyond consultancy, StrataFlux Energy supports technical capacity development through applied training, mentoring, and modelling guidance for professionals, researchers, and students.
    </p>

    <div class="support-grid">

      <div class="support-card">
        <h3>Open-Source Modelling Training</h3>
        <p>Hands-on training in reservoir simulation, geochemical modelling, reactive transport workflows, and open-source tools including PFLOTRAN, PHREEQC, MRST, and Python-based modelling workflows.</p>
        <a href="/services/training/" class="btn btn--primary">View Training</a>
      </div>

      <div class="support-card">
        <h3>Research & Student Support</h3>
        <p>Technical mentoring, modelling guidance, workflow development, troubleshooting, and research support for BSc, MSc, PhD, and early-career researchers working on subsurface energy projects.</p>
        <a href="/services/student-projects/" class="btn btn--primary">Explore Support</a>
      </div>

    </div>
  </div>
</section>

<!-- ========== INSIGHTS SECTION ========== -->
<section class="sf-section">
  <div class="sf-container">
    <h2 class="sf-section-title">Technical Insights</h2>
    <p class="sf-section-intro">
      Insights and technical resources focused on advanced subsurface modelling, energy storage systems, reactive transport processes, and reservoir performance forecasting.
    </p>
    <a href="/blog/" class="btn btn--primary">Visit Insights</a>
  </div>
</section>

<!-- ========== FINAL CTA ========== -->
<section class="cta-section">
  <div class="sf-container">
    <h2>Need technical support for a subsurface modelling project?</h2>
    <p>
      Whether you are assessing CO₂ storage potential, evaluating underground hydrogen storage, forecasting reservoir performance, or developing a research workflow, StrataFlux Energy provides technically rigorous solutions for your complex subsurface energy challenges.
    </p>
    <a href="/contact/" class="btn btn--primary">Discuss Your Project</a>
  </div>
</section> 
