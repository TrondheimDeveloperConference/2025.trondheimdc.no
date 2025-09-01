---
layout: courses
language: "no"
title: "Kurs og workshops"
permalink: "/courses/"
nav_active: courses
image_header: "/assets/images/logos/courses.svg"
---

I samarbeid med våre partnere, kan vi tilby kurs og workshops i forbindelse med TDC.

Kursene gjennomføres i dagene etter konferansen. Alle kurs holdes i Trondheim og det er arrangørene som står for lokaler og gjennomføring. Følg lenkene under for mer informasjon og påmelding (eksterne websider).

<div class="courses-grid mt-2">
  {% assign items = site.data.courses %}
  {% assign count = items | size %}
  {% if count > 0 %}
    {% for c in items %}
    <div>
      <div class="card course-card">
        <img src="{{ c.image | default: '/assets/images/standard/graphic1.png' }}" class="card-img-top" alt="{{ c.title }}">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">{{ c.title }}</h5>
          <p class="card-text">{{ c.description }}</p>
          <a class="mt-auto btn btn-outline-success" href="{{ c.url }}" target="_blank" rel="noopener">Mer info</a>
        </div>
      </div>
    </div>
    {% endfor %}
  {% else %}
    {% comment %} Dummy cards until we have a full list {% endcomment %}
    {% for i in (1..6) %}
    <div>
      <div class="card course-card">
        <img src="/assets/images/standard/graphic1.png" class="card-img-top" alt="Plassholderbilde">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">Kurs tittel {{ i }}</h5>
          <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          <a class="mt-auto btn btn-outline-success disabled" href="#" tabindex="-1" aria-disabled="true">Kommer snart</a>
        </div>
      </div>
    </div>
    {% endfor %}
  {% endif %}
</div>
