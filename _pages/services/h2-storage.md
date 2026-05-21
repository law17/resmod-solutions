---
layout: single
title: "Hydrogen Storage Simulation"
permalink: /services/h2-storage/
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
    <img src="{{ '/assets/images/h2-storage.jpg' | relative_url }}" alt="H₂ storage simulation">
  </div>
  <div class="service-text">
    <p><strong>Service overview:</strong><br>
    Design and optimisation of underground hydrogen storage (UHS) in depleted gas fields, aquifers, or caverns. We simulate cyclic operations, cushion gas requirements, and geochemical interactions that may impact deliverability.</p>

    <p><strong>Typical deliverables:</strong></p>
    <ul>
      <li>Dynamic simulation of injection/production cycles</li>
      <li>Cushion gas sizing and mixing analysis</li>
      <li>Geochemical reactivity (H₂-brine-rock)</li>
      <li>Pressure evolution and mechanical stability check</li>
    </ul>

    <p><strong>Software:</strong> MRST, OpenFOAM (for CFD aspects), Python utilities.</p>

    <p><a href="/resmod-solutions/contact/" class="btn btn--primary">Request a consultation →</a></p>
  </div>
</div>
