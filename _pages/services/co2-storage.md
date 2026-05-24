---
layout: single
title: "CO₂ Storage Modelling"
permalink: /services/co2-storage/
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
    <img src="{{ '/assets/images/co2-storage.jpg' | relative_url }}" alt="CO₂ storage simulation">
  </div>
  <div class="service-text">
    <p><strong>Service overview:</strong><br>
    We build predictive reservoir models for geological carbon storage. From regional screening to detailed site characterization, we help assess storage capacity, injectivity, plume migration, and long-term trapping mechanisms.</p>

    <p><strong>Typical deliverables:</strong></p>
    <ul>
      <li>3D static and dynamic models (structured/unstructured grids)</li>
      <li>Plume footprint and pressure front evolution</li>
      <li>Trap integrity and leakage risk analysis</li>
      <li>Geochemical reactions (dissolution, mineralization)</li>
      <li>Uncertainty quantification and sensitivity analysis</li>
    </ul>

    <p><strong>Software:</strong> MRST, PFLOTRAN, PHREEQC, CMG (on request), Python scripting for automation.</p>

    <p><a href="/contact/" class="btn btn--primary">Request a consultation →</a></p>
  </div>
</div>
