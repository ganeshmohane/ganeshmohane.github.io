---
permalink: /
title: "About"
layout: splash
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<div class="home-page">
  <section class="home-hero">
    <img class="home-photo" src="{{ site.baseurl }}/images/profile.png" alt="Ganesh Mohane">
    <h1>Ganesh Mohane</h1>
    <p class="home-role">ML Engineer · Privacy AI · Production Inference & Optimization</p>
    <div class="home-summary-wrap" style="width: 100%; text-align: center;">
      <p class="home-summary" style="display: block; width: 680px; max-width: calc(100% - 2rem); margin: 0 auto 1.35rem; text-align: center !important;">I build and deploy machine-learning systems that are fast, reliable, and useful in production. My work spans model optimization, privacy-focused computer vision, CUDA and TensorRT inference, and scalable ML infrastructure.</p>
    </div>
    <div class="home-links">
      <span><i class="fas fa-location-dot"></i> Navi Mumbai, India</span>
      <a class="home-contact-icon" href="mailto:ganeshmohane5@gmail.com" title="Email" aria-label="Email"><i class="fas fa-envelope"></i></a>
      <a class="home-contact-icon" href="https://github.com/ganeshmohane" title="GitHub" aria-label="GitHub"><i class="fab fa-github"></i></a>
      <a class="home-contact-icon" href="https://kaggle.com/ganeshmohane" title="Kaggle" aria-label="Kaggle"><i class="fab fa-kaggle"></i></a>
      <a class="home-contact-icon" href="https://www.linkedin.com/in/ganeshmohane" title="LinkedIn" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
    </div>
  </section>

  <section class="home-section">
    <div class="section-heading"><h2>Latest Posts</h2><a href="{{ site.baseurl }}/year-archive/">View all posts →</a></div>
    <div class="post-grid">
      {% assign recent_posts = site.posts | sort: 'date' | reverse %}
      {% for post in recent_posts limit:4 %}
      <article class="post-card">
        {% if post.header.teaser %}
        <a class="post-card-image-link" href="{{ post.url | relative_url }}" aria-label="Read {{ post.title }}">
          <img class="post-card-image" src="{% if post.header.teaser contains '://' %}{{ post.header.teaser }}{% else %}{{ post.header.teaser | prepend: '/images/' | relative_url }}{% endif %}" alt="{{ post.title }} preview">
        </a>
        {% endif %}
        <div class="post-card-content">
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        </div>
      </article>
      {% endfor %}
    </div>
  </section>

  <section class="home-section">
    <div class="section-heading"><h2>Selected Projects</h2><a href="{{ site.baseurl }}/portfolio/">View projects →</a></div>
    <div class="project-grid">
      {% for project in site.portfolio limit:2 %}
      <article class="project-card">
        {% if project.header.teaser %}
        <img class="project-card-image" src="{{ project.header.teaser | relative_url }}" alt="{{ project.title }} project graphic">
        {% endif %}
        <h2>{{ project.title }}</h2>
        <p>{{ project.excerpt | strip_html | truncate: 160 }}</p>
        <a class="project-link" href="{{ project.url | relative_url }}">Explore project →</a>
      </article>
      {% endfor %}
    </div>
  </section>
</div>
