---
layout: splash
permalink: /
header:
  overlay_color: "#1a1a2e"
  overlay_image: "{{ site.baseurl }}/assets/images/hero-co2-h2.png"
  caption: "Precision simulation for the subsurface energy transition."
  actions:
    - label: "Explore Services"
      url: "{{ site.baseurl }}/services/co2-storage/"
    - label: "Student Support"
      url: "{{ site.baseurl }}/services/student-projects/"
title: "ResMod Solutions"
excerpt: "Modelling CO₂ & H₂ storage, EOR, and reservoir performance. Open-source training for the next generation of engineers."
feature_row:
  - image_path: "{{ site.baseurl }}/assets/images/co2-storage.jpg"
    alt: "CO₂ Storage"
    title: "CO₂ Storage"
    excerpt: "Plume migration, trap integrity, geochemical trapping."
    url: "{{ site.baseurl }}/services/co2-storage/"
    btn_label: "Learn More"
    btn_class: "btn--primary"
  - image_path: "{{ site.baseurl }}/assets/images/h2-storage.jpg"
    alt: "H₂ Storage"
    title: "H₂ Storage"
    excerpt: "Cyclic injection, cushion gas, cushion integrity."
    url: "{{ site.baseurl }}/services/h2-storage/"
    btn_label: "Learn More"
    btn_class: "btn--primary"
  - image_path: "{{ site.baseurl }}/assets/images/eor.jpg"
    alt: "EOR"
    title: "EOR"
    excerpt: "Waterflood, gas injection, chemical EOR forecasting."
    url: "{{ site.baseurl }}/services/eor/"
    btn_label: "Learn More"
    btn_class: "btn--primary"
feature_row2:
  - image_path: "{{ site.baseurl }}/assets/images/reservoir-performance.jpg"
    alt: "Reservoir Performance"
    title: "Reservoir Performance"
    excerpt: "Decline curve analysis, history matching, field forecasts."
    url: "{{ site.baseurl }}/services/reservoir-performance/"
    btn_label: "Learn More"
    btn_class: "btn--primary"
  - image_path: "{{ site.baseurl }}/assets/images/student-project.jpg"
    alt: "Student Projects"
    title: "Student Project Assistance"
    excerpt: "BSc, MSc, PhD modelling help. Supervision & review."
    url: "{{ site.baseurl }}/services/student-projects/"
    btn_label: "Support"
    btn_class: "btn--primary"
  - image_path: "{{ site.baseurl }}/assets/images/training-workshop.jpg"
    alt: "Training"
    title: "Open-Source Training"
    excerpt: "MRST, PFLOTRAN, PHREEQC workshops. Hands-on online."
    url: "{{ site.baseurl }}/services/training/"
    btn_label: "View Workshops"
    btn_class: "btn--primary"
---

{% include feature_row %}

{% include feature_row id="feature_row2" %}
