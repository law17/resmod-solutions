---
layout: single
title: "Open‑Source Software Training"
permalink: /services/training/
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
  /* Two-column layout: image and text */
  .service-layout {
    display: flex;
    gap: 2rem;
    align-items: flex-start;
    flex-wrap: wrap;
  }
  .service-image {
    flex: 1 1 50%;
    max-width: 500px;
  }
  .service-text {
    flex: 1 1 45%;
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
    <img src="{{ '/assets/images/training-workshop.jpg' | relative_url }}" alt="Training workshop">
  </div>
  <div class="service-text">
    <p><strong>Workshops we offer (all online, live):</strong></p>
    <ul>
      <li><strong>PFLOTRAN Essentials for CO₂ Storage</strong> – grid setup, fluid models, injection scenarios</li>
      <li><strong>Reservoir Simulation with MRST</strong> – traditional oil recovery and CO2 storage training</li>
      <li><strong>Geochemical modelling with PHREEQC</strong></li>
      <li><strong>Python for Reservoir Engineers</strong> – data processing, automation, visualisation</li>
    </ul>
    <p>Each workshop includes real‑data exercises, script sharing, and post‑workshop support. University group packages available.</p>
    <p><a href="{{ '/training-hub/' | relative_url }}" class="btn btn--primary">See upcoming dates & register →</a></p>
  </div>
</div>
