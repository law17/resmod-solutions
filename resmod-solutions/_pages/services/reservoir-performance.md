---
layout: single
title: "Reservoir Performance Predictions"
permalink: /services/reservoir-performance/
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
  /* Two-column layout: image (1/3) and text (2/3) */
  .service-layout {
    display: flex;
    gap: 2rem;
    align-items: flex-start;
    flex-wrap: wrap;
  }
  .service-image {
    flex: 1 1 50%;        /* takes roughly 1/3 */
    max-width: 700px;
  }
  .service-text {
    flex: 2 1 60%;        /* takes roughly 2/3 */
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
    <img src="{{ '/assets/images/reservoir-performance.jpg' | relative_url }}" alt="CO₂ storage simulation">
  </div>
  <div class="service-text">
    <p><strong>Service overview:</strong><br>
    Independent production forecasting using analytical and numerical methods. Ideal for reserves estimation, field development planning, and investment decisions.</p>

    <p><strong>What we offer:</strong></p>
    <ul>
      <li>Decline curve analysis (Arps, Fetkovich, etc.)</li>
      <li>Material balance and dynamic simulation scenarios</li>
      <li>History matching to production data</li>
      <li>Probabilistic forecasting (Monte Carlo)</li>
      <li>Custom dashboards and reports</li>
    </ul>

    <p><strong>Software:</strong> Python (scipy, pandas), MRST, Excel (structured).</p>

    <p><a href="/resmod-solutions/contact/" class="btn btn--primary">Request a consultation →</a></p>
  </div>
</div>
