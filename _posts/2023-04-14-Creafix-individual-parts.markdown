---
title:  "Creafix seperate parts!"
date:   2023-04-14 11:11:07 +0200
categories: jekyll update
permalink: "/Creafix/all-parts/"
---

<div id="carouselExampleDark" class="carousel carousel-dark slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="https://ingegno.be/img/realisations/creafix_03.jpg" alt="StartImage">
    </div>
	{% for image in site.static_files %}
  {% if image.path contains 'images/' %}
    <div class="carousel-item">
      <img src="{{ image.path }}" alt="Image">
    </div>
	{% endif %}
{% endfor %}
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </button>
</div>

<div class="image-row">
{% for partI in site.data.parts_individual %}
<div class="image-container">
	<a href="{{ partI.Link }}">
	<img src="{{ site.baseurl }}/assets/images/{{ partI.PartName | uri_escape }}.png" width=250px alt="Part image">
	</a>
	<div class="image-text">{{ partI.PartName }}</div>
	<div class="image-caption">{{ partI.PartName }}, Material thickness: {{ partI.Material_Thickness }}, Material(s): {{ partI.Materials }}, Construct via: {{ partI.Construction_Method }}, <a href="{{ partI.Link }}">Part Link</a></div>
</div>
{% endfor %}
</div>

{% for image in site.static_files %}
  {% if image.path contains 'images/' %}
    <img src="{{ image.path }}" alt="{{ image.name }}">
  {% endif %}
{% endfor %}