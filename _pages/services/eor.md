---
layout: single
title: "Enhanced Oil Recovery (EOR)"
permalink: /services/eor/
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
    <img src="{{ '/assets/images/eor.jpg' | relative_url }}" alt="EOR">
  </div>
  <div class="service-text">
    <p><strong>Service overview:</strong><br>
    History‑matched models and forecast scenarios for mature fields considering waterflood, gas injection, smart-water flood, and chemical EOR. We help you understand recovery factors, sweep efficiency, and economics.</p>

    <p><strong>Typical deliverables:</strong></p>
    <ul>
      <li>Black‑oil and compositional simulation</li>
      <li>Streamline analysis and well pattern optimisation</li>
      <li>Sensitivity on injection rate, WAG cycles, polymer concentration</li>
      <li>Recovery factor prediction under different development plans</li>
    </ul>

    <p><strong>Software:</strong> MRST, open‑source compositional simulators, Python.</p>

    <p><a href="/strataflux-energy/contact/" class="btn btn--primary">Request a consultation →</a></p>
  </div>
</div>
