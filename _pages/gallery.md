---
layout: page
title: gallery
permalink: /gallery/
description: Photos from conferences and research travels.
nav: true
nav_order: 4
---

{% assign cvpr2026_images = "01.jpg,02.jpg,03.jpg,04.png,06.jpg" | split: "," %}
{% assign temesvar2026_images = "01.jpg,02.jpg" | split: "," %}

<style>
  .photo-gallery {
    columns: 3 260px;
    column-gap: 1rem;
    margin-top: 1.25rem;
  }

  .photo-gallery figure {
    break-inside: avoid;
    margin: 0 0 1rem;
    position: relative;
  }

  .photo-gallery img {
    width: 100%;
    border-radius: 6px;
  }

  .photo-gallery figcaption {
    color: var(--global-text-color-light);
    font-size: 0.9rem;
    margin-top: 0.35rem;
  }

  .gallery-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin: 0.75rem 0 0;
  }

  .gallery-badge {
    border: 1px solid var(--global-theme-color);
    border-radius: 999px;
    color: var(--global-theme-color);
    font-size: 0.85rem;
    font-weight: 600;
    line-height: 1;
    padding: 0.4rem 0.65rem;
  }

  .gallery-note {
    margin-top: 0.5rem;
  }

  .gallery-section {
    margin-top: 2.5rem;
  }
</style>

## CVPR 2026

Denver, Colorado.

Our paper "Global-Aware Edge Prioritization for Pose Graph Initialization" was selected as a CVPR 2026 Award Candidate, and we were featured by [CVNews](https://rsipvision.com/CVPR2026-Sunday/).

<div class="gallery-badges">
  <span class="gallery-badge">Oral Presentation</span>
  <span class="gallery-badge">Award Candidate</span>
</div>

{% if cvpr2026_images.size > 0 %}
<div class="photo-gallery">
  {% for image in cvpr2026_images %}
    <figure>
      <a href="{{ '/assets/img/cvpr2026/' | append: image | relative_url }}">
        <img src="{{ '/assets/img/cvpr2026/' | append: image | relative_url }}" alt="CVPR 2026 photo {{ forloop.index }}">
      </a>
      {% if forloop.first %}
        <figcaption>Oral presentation and Award Candidate poster session.</figcaption>
      {% endif %}
    </figure>
  {% endfor %}
</div>
{% else %}
<p class="gallery-note">Photos coming soon.</p>
{% endif %}

<div class="gallery-section">

## Temesvar VRG Meetup & Team Building

June 21, 2026.

<div class="photo-gallery">
  {% for image in temesvar2026_images %}
    <figure>
      <a href="{{ '/assets/img/temesvar2026/' | append: image | relative_url }}">
        <img src="{{ '/assets/img/temesvar2026/' | append: image | relative_url }}" alt="Temesvar VRG Meetup and Team Building photo {{ forloop.index }}">
      </a>
    </figure>
  {% endfor %}
</div>

</div>
