---
layout: single
title: "Upstream Oil & Gas Solutions"
permalink: /services/upstream-oil-gas/
---

<style>
  * {
    text-align: justify !important;
  }
  h1, h2, h3, h4, h5, h6, .btn, nav, .masthead, .page__hero-caption {
    text-align: left !important;
  }
  .page__title {
    display: none;
  }
  /* Two-column layout for the service page */
  .service-layout {
    display: flex;
    gap: 2rem;
    align-items: flex-start;
    flex-wrap: wrap;
  }
  .service-image {
    flex: 1 1 40%;
    max-width: 400px;
  }
  .service-text {
    flex: 1 1 55%;
  }
  .service-image img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  }
  @media (max-width: 768px) {
    .service-layout {
      flex-direction: column;
    }
    .service-image {
      max-width: 100%;
    }
  }
</style>

<div class="service-layout">
  <div class="service-image">
    <img src="{{ '/assets/images/eor.jpg' | relative_url }}" alt="Upstream Oil & Gas simulation">
  </div>
  <div class="service-text">
    <p><strong>Enhanced Oil Recovery (EOR)</strong><br>
    We design and simulate advanced recovery methods including waterflood, gas injection, and chemical EOR. Our models help you understand sweep efficiency, recovery factors, and economics to maximise asset value.</p>

    <p><strong>Typical EOR deliverables:</strong></p>
    <ul>
      <li>Black‑oil and compositional simulation</li>
      <li>Streamline analysis and well pattern optimisation</li>
      <li>Sensitivity on injection rate, WAG cycles, polymer concentration</li>
      <li>Recovery factor prediction under different development plans</li>
    </ul>

    <p><strong>Reservoir Performance Predictions</strong><br>
    Independent production forecasting using analytical and numerical methods. Ideal for reserves estimation, field development planning, and investment decisions.</p>

    <p><strong>Typical reservoir performance deliverables:</strong></p>
    <ul>
      <li>Decline curve analysis (Arps, Fetkovich, etc.)</li>
      <li>Material balance and dynamic simulation scenarios</li>
      <li>History matching to production data</li>
      <li>Probabilistic forecasting (Monte Carlo)</li>
      <li>Custom dashboards and reports</li>
    </ul>

    <p><strong>Software:</strong> MRST, open‑source compositional simulators, Python (scipy, pandas), Excel (structured).</p>

    <p><a href="{{ '/contact/' | relative_url }}" class="btn btn--primary">Request a consultation →</a></p>
  </div>
</div>
