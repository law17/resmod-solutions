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
    text-align: justify !important;
  }

  .cta-section h2 {
    color: white;
    font-size: 2.2rem;
    margin-bottom: 1rem;
  }

  .cta-section p {
  max-width: 760px;
  margin: 0 0 1.8rem 0;
  font-size: 1.15rem;
  line-height: 1.7;
  text-align: justify !important;
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

  /* ========== AI SECTION ========== */
  .ai-section {
    background: linear-gradient(135deg, #071b2f 0%, #0a2540 55%, #143f2c 100%);
    color: white;
    padding: 4rem 1.5rem;
  }    

  .ai-header {
    max-width: 900px;
    margin-bottom: 2rem;
  }

  .ai-label {
    display: inline-block;
    color: #63b32e;
    font-weight: 800;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    font-size: 0.85rem;
    margin-bottom: 0.6rem;
  }

  .ai-header h2 {
    color: white;
    font-size: 2.2rem;
    margin-bottom: 1rem;
  }

  .ai-header p {
    font-size: 1.12rem;
    line-height: 1.75;
    text-align: justify;
    color: #e8eef5;
  }

  .ai-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }

  .ai-card {
    background: rgba(255, 255, 255, 0.08);
    border: 1px solid rgba(255, 255, 255, 0.16);
    border-radius: 16px;
    padding: 1.7rem;
    box-shadow: 0 14px 30px rgba(0,0,0,0.18);
  }

  .ai-icon {
    width: 46px;
    height: 46px;
    border-radius: 12px;
    background: linear-gradient(135deg, #63b32e, #2f7d32);
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.4rem;
    margin-bottom: 1rem;
  }

  .ai-card h3,
  .ai-applications h3,
  .ai-list-grid h4 {
  color: white;
}

  .ai-card p {
    color: #e8eef5;
    line-height: 1.65;
    text-align: justify;
  }

  .ai-applications {
    margin-top: 2.5rem;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.14);
    border-radius: 16px;
    padding: 2rem;
  }

  .ai-list-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.5rem;
    margin-top: 1rem;
  }

  .ai-list-grid ul {
    padding-left: 1.2rem;
    line-height: 1.75;
    color: #e8eef5;
  }

  .ai-list-grid li {
    text-align: left;
  }

  @media (max-width: 900px) {
    .ai-grid,
    .ai-list-grid {
      grid-template-columns: 1fr;
  }

  .ai-header h2 {
    font-size: 1.8rem;
  }
}
  
</style>

<!-- ========== HERO CAROUSEL SPLIT SECTION WITH TABS ========== -->
<style>
  .hero-split {
    background: linear-gradient(135deg, #f3f5f7 0%, #e9edf1 100%);
    padding: 4rem 1.5rem;
  }

  .hero-split-container {
    max-width: 1180px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 0.95fr 1.05fr;
    gap: 3rem;
    align-items: center;
  }

  .hero-tabs {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
    margin-bottom: 1.4rem;
  }

  .hero-tab {
    border: 1px solid #d9e2ec;
    background: white;
    color: #0a2540;
    padding: 0.5rem 0.8rem;
    border-radius: 999px;
    font-weight: 700;
    font-size: 0.82rem;
    cursor: pointer;
    transition: all 0.25s ease;
    white-space: nowrap;
  }

  .hero-tab.active,
  .hero-tab:hover {
    background: #63b32e;
    color: white;
    border-color: #63b32e;
  }

  .hero-label {
    color: #63b32e;
    font-weight: 800;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 0.8rem;
    font-size: 0.85rem;
  }

  .hero-title {
    font-size: 3rem;
    line-height: 1.08;
    color: #0a2540;
    margin: 0 0 1.2rem;
  }

  .hero-text {
    color: #4f5f6f;
    font-size: 1.18rem;
    line-height: 1.75;
    margin-bottom: 1.6rem;
    text-align: justify;
  }

  .hero-actions a {
    margin-right: 0.8rem;
    margin-bottom: 0.8rem;
  }

  .hero-image-wrap {
    background: white;
    padding: 0.7rem;
    border-radius: 22px;
    border: 1px solid #d9e2ec;
    box-shadow: 0 22px 45px rgba(10, 37, 64, 0.15);
  }

  .hero-image-wrap img {
    width: 100%;
    height: 430px;
    object-fit: cover;
    border-radius: 16px;
    display: block;
  }

  @media (max-width: 900px) {
    .hero-split-container {
      grid-template-columns: 1fr;
    }

    .hero-title {
      font-size: 2.25rem;
    }

    .hero-image-wrap img {
      height: 300px;
    }
  }
</style>

<!-- ========== BLUE GRADIENT, POSITIONING BAR ========== -->
<section class="sf-positioning sf-section" style="padding: 1.5rem 1.5rem; text-align: justify">
  <div class="sf-container">
    <p>
      StrataFlux Energy provides advanced subsurface modelling, simulation, and technical advisory services for subsurface energy operations.
    </p>
    <div style="margin-top:1.5rem;">
      <a href="/services/" class="btn btn--primary" style="margin-right: 1rem;">Explore Services</a>
      <a href="/contact/" class="btn btn--light-outline">Discuss a Project</a>
    </div>
  </div>
</section>

<!-- ========== HERO BAR ========== -->

<section class="hero-split">
  <div class="hero-split-container">

    <div class="hero-copy">
      <div class="hero-tabs">
        <button class="hero-tab active" data-service="co2">CO₂ Storage</button>
        <button class="hero-tab" data-service="h2">H₂ Storage</button>
        <button class="hero-tab" data-service="reservoir">Reservoir Forecasting</button>
      </div>

      <div class="hero-label" id="heroLabel">Carbon Storage</div>

      <h1 class="hero-title" id="heroTitle">
        Advanced CO₂ Storage Modelling
      </h1>

      <p class="hero-text" id="heroText">
        Science-driven modelling workflows for storage screening, plume migration, injectivity, trapping mechanisms, and long-term subsurface performance.
      </p>

      <div class="hero-actions">
        <a href="/services/co2-storage/" class="btn btn--primary" id="heroPrimary">
          Explore CO₂ Storage
        </a>
        <a href="/contact/" class="btn btn--primary">
          Discuss a Project
        </a>
      </div>
    </div>

    <div class="hero-image-wrap">
      <!--alt<img id="heroImage" src="/assets/images/co2-storage.jpg" alt="CO₂ storage modelling concept"> --> 
      <img id="heroImage" src="/assets/images/co2-storage.jpg"> 
    </div>

  </div>
</section>

<script>
  (function() {
    const heroData = {
      co2: {
        label: "Carbon Storage",
        title: "Advanced CO₂ Storage Modelling",
        text: "Science-driven modelling workflows for storage screening, plume migration, injectivity, trapping mechanisms, and long-term subsurface performance.",
        image: "/assets/images/co2-storage.jpg",
        <!--alt: "CO₂ storage modelling concept",-->
        link: "/services/co2-storage/",
        button: "Explore CO₂ Storage"
      },
      h2: {
        label: "Hydrogen Storage",
        title: "Underground H₂ Storage Simulation",
        text: "Technical modelling for cushion gas behaviour, cyclic injection and withdrawal, containment risk, geochemical reactivity, and storage performance.",
        image: "/assets/images/h2-storage.jpg",
        <!--alt: "Hydrogen storage simulation concept",-->
        link: "/services/h2-storage/",
        button: "Explore H₂ Storage"
      },
      reservoir: {
        label: "Upstream Oil & Gas",
        title: "Reservoir Performance Forecasting",
        text: "Integrated simulation, history matching, decline analysis, and uncertainty assessment to support better oil & gas reservoir decisions.",
        image: "/assets/images/reservoir-performance.jpg",
        <!--alt: "Reservoir performance forecasting concept",-->
        link: "/services/upstream-oil-gas/",
        button: "Explore Forecasting"
      }
    };

    const tabs = document.querySelectorAll(".hero-tab");
    const label = document.getElementById("heroLabel");
    const title = document.getElementById("heroTitle");
    const text = document.getElementById("heroText");
    const image = document.getElementById("heroImage");
    const primary = document.getElementById("heroPrimary");

    tabs.forEach(tab => {
      tab.addEventListener("click", () => {
        const key = tab.dataset.service;
        const item = heroData[key];

        tabs.forEach(t => t.classList.remove("active"));
        tab.classList.add("active");

        label.textContent = item.label;
        title.textContent = item.title;
        text.textContent = item.text;
        image.src = item.image;
        image.alt = item.alt;
        primary.href = item.link;
        primary.textContent = item.button;
      });
    });
  })();
</script>

<!-- ========== WHO WE ARE ========== -->
<section class="sf-section">
  <div class="sf-container who-grid">
    <div>
      <h2 class="sf-section-title">StrataFlux Energy</h2>
      <p class="sf-section-intro_2">
        We are an independent subsurface consultancy focused on advanced modelling, simulation, and technical analysis for carbon and hydrogen storage, as well as upstream oil & gas systems.
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

<!-- ========== AI-ASSISTED SUBSURFACE WORKFLOWS ========== -->
<section class="ai-section">
  <div class="sf-container">

    <div class="ai-header">
      <span class="ai-label">Computational Intelligence</span>
      <h2>AI-Assisted Subsurface Modelling & Decision Support</h2>
      <p>
        StrataFlux Energy combines physics-based simulation, computational automation, data-driven analysis, and AI-assisted workflows to improve the efficiency, interpretation, and reliability of subsurface energy studies.
      </p>
    </div>

    <div class="ai-grid">

      <div class="ai-card">
        <div class="ai-icon">⌁</div>
        <h3>Intelligent Forecasting</h3>
        <p>
          AI-assisted workflows can support CO₂ plume evolution analysis, hydrogen storage prediction, hydrocarbon production forecasting, and reservoir performance screening across multiple operating scenarios.
        </p>
      </div>

      <div class="ai-card">
        <div class="ai-icon">◎</div>
        <h3>Uncertainty & Risk Evaluation</h3>
        <p>
          Data-driven methods help identify dominant parameters, rank scenarios, screen uncertainty ranges, and support risk-informed decisions for storage security, injectivity, containment, and field performance.
        </p>
      </div>

      <div class="ai-card">
        <div class="ai-icon">▣</div>
        <h3>Workflow Automation</h3>
        <p>
          Computational automation improves simulation setup, batch processing, sensitivity analysis, result extraction, model comparison, and technical reporting for complex subsurface projects.
        </p>
      </div>

    </div>

    <div class="ai-applications">
      <h3>Where We Apply AI-Assisted Workflows</h3>

      <div class="ai-list-grid">
        <div>
          <h4>CO₂ Storage</h4>
          <ul>
            <li>Storage screening and site ranking</li>
            <li>Injectivity and pressure response evaluation</li>
            <li>Plume migration and trapping assessment</li>
            <li>Leakage risk and monitoring support</li>
          </ul>
        </div>

        <div>
          <h4>Hydrogen Storage</h4>
          <ul>
            <li>Cyclic injection and withdrawal forecasting</li>
            <li>Cushion gas and deliverability evaluation</li>
            <li>Containment and migration screening</li>
            <li>Operational scenario comparison</li>
          </ul>
        </div>

        <div>
          <h4>Oil & Gas Reservoirs</h4>
          <ul>
            <li>History matching support</li>
            <li>Production and decline forecasting</li>
            <li>EOR, waterflood and gas injection screening</li>
            <li>Reservoir surveillance and anomaly detection</li>
          </ul>
        </div>
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
    <h2>Looking for advanced subsurface modelling expertise?</h2>
    <p>
      Whether you are assessing CO₂ storage potential, evaluating underground hydrogen storage, forecasting reservoir performance, or developing a research workflow, StrataFlux Energy provides technically rigorous solutions for your complex subsurface energy challenges.
    </p>
    <a href="/contact/" class="btn btn--primary">Discuss Your Project</a>
  </div>
</section> 
