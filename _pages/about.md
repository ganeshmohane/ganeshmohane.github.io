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
    <p class="home-role">ML Engineer · Privacy AI · Production Inference</p>
    <p class="home-summary">I build and deploy machine-learning systems that are fast, reliable, and useful in production. My work spans model optimization, privacy-focused computer vision, CUDA and TensorRT inference, and scalable ML infrastructure.</p>
    <div class="home-links">
      <span><i class="fas fa-location-dot"></i> Mumbai, India</span>
      <a href="mailto:ganeshmohane5@gmail.com"><i class="fas fa-envelope"></i> Email</a>
      <a href="https://github.com/ganeshmohane"><i class="fab fa-github"></i> GitHub</a>
      <a href="https://www.linkedin.com/in/ganeshmohane"><i class="fab fa-linkedin"></i> LinkedIn</a>
    </div>
  </section>

  <section class="home-section">
    <div class="section-heading"><h2>Latest Posts</h2><a href="{{ site.baseurl }}/year-archive/">View all posts →</a></div>
    <div class="post-grid">
      {% assign recent_posts = site.posts | sort: 'date' | reverse %}
      {% for post in recent_posts limit:4 %}
      <article class="post-card">
        <time class="post-card-date" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
        <div class="post-tags">
          {% for tag in post.tags limit:3 %}<span>{{ tag }}</span>{% endfor %}
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
        <h2>{{ project.title }}</h2>
        <p>{{ project.excerpt | strip_html | truncate: 160 }}</p>
        <a class="project-link" href="{{ project.url | relative_url }}">Explore project →</a>
      </article>
      {% endfor %}
    </div>
  </section>
</div>

