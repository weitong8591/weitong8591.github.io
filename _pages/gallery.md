---
layout: page
title: gallery
permalink: /gallery/
description: Photos from conferences and research travels.
nav: true
nav_order: 4
---

{% assign cvpr2026_images = site.static_files | where_exp: "file", "file.path contains '/assets/img/cvpr2026/' and file.name != '.gitkeep'" %}
{% assign cvpr2026_images = cvpr2026_images | sort: "name" %}

<style>
  .photo-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
    margin-top: 1.25rem;
  }

  .photo-gallery figure {
    margin: 0;
  }

  .photo-gallery img {
    width: 100%;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    border-radius: 6px;
  }

  .gallery-note {
    margin-top: 0.5rem;
  }
</style>

## CVPR 2026

Denver, Colorado.

Our paper "Global-Aware Edge Prioritization for Pose Graph Initialization" was selected as a CVPR 2026 Award Candidate, and we were featured by [CVNews](https://rsipvision.com/CVPR2026-Sunday/).

{% if cvpr2026_images.size > 0 %}
<div class="photo-gallery">
  {% for image in cvpr2026_images %}
    <figure>
      <a href="{{ image.path | relative_url }}">
        <img src="{{ image.path | relative_url }}" alt="CVPR 2026 photo {{ forloop.index }}">
      </a>
    </figure>
  {% endfor %}
</div>
{% else %}
<p class="gallery-note">Photos coming soon.</p>
{% endif %}
