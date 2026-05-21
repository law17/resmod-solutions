---
layout: single
title: "Student Project Support"
permalink: /services/student-projects/
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
  /* Two-column layout: image (1/2) and text (1/2) */
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
    <img src="{{ '/assets/images/student-project.jpg' | relative_url }}" alt="Student project support">
  </div>
  <div class="service-text">
    <p><strong>Are you a BSc, MSc, or PhD student struggling with simulation setup, debugging, or result interpretation?</strong></p>
    
    <p>We provide technical modelling support, training, and advisory services for academic research. We offer:</p>
    <ul>
      <li>Simulation workflow guidance</li>
      <li>Model setup assistance</li>
      <li>Software troubleshooting</li>
      <li>Data interpretation</li>
      <li>Coding support</li>
      <li>Research training</li>
      <li>Publication technical review</li>
    </ul>
    <p><strong>Important</strong></p>We do not write your thesis for you; we teach you to build models with confidence<p>

    <p><a href="{{ '/contact/' | relative_url }}" class="btn btn--primary">Book a session →</a></p>

