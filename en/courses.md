---
layout: courses
lang: en
title: "Courses and Workshops"
permalink: "/en/courses/"
nav_active: courses
image_header: "/assets/images/logos/courses.svg"
---

In collaboration with our partners, we offer courses and workshops related to TDC.

The courses take place in the days following the conference. All courses are held in Trondheim, and the organisers are responsible for the venues and delivery. Follow the links below for more information and registration (external websites).

<div class="courses-grid mt-2">
  {% assign items = site.data.courses_en %}
  {% assign count = items | size %}
  {% if count > 0 %}
    {% for c in items %}
    <div>
      <div class="card course-card">
        <img src="{{ c.image | default: '/assets/images/standard/graphic1.png' }}" class="card-img-top" alt="{{ c.title }}">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">{{ c.title }}</h5>
          <p class="card-text">{{ c.description }}</p>
          <a class="mt-auto btn btn-outline-success" href="{{ c.url }}" target="_blank" rel="noopener">More info</a>
        </div>
      </div>
    </div>
    {% endfor %}
  {% else %}
    {% comment %} Dummy cards until we have a full list {% endcomment %}
    {% for i in (1..6) %}
    <div>
      <div class="card course-card">
        <img src="/assets/images/standard/graphic1.png" class="card-img-top" alt="Placeholder image">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">Course title {{ i }}</h5>
          <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          <a class="mt-auto btn btn-outline-success disabled" href="#" tabindex="-1" aria-disabled="true">Coming soon</a>
        </div>
      </div>
    </div>
    {% endfor %}
  {% endif %}
</div>
