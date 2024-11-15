---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Treatments
---
<section class="treatment-section py-5" id="treatments">
  <div class="container">
    <h2 class="text-center mb-4">Our Eye Treatments</h2>
    <div id="treatmentCarousel" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        {% for treatment in site.data.treatments %}
        <div class="carousel-item {% if forloop.first %}active{% endif %}">
          <div class="card mx-auto" style="max-width: 300px;">
            <img src="{{ treatment.image }}" class="card-img-top" alt="{{ treatment.name }}">
            <div class="card-body text-center">
              <h5 class="card-title">{{ treatment.name }}</h5>
              <p class="card-text">{{ treatment.description }}</p>
            </div>
          </div>
        </div>
        {% endfor %}
      </div>
      <!-- Carousel Controls -->
      <button class="carousel-control-prev" type="button" data-bs-target="#treatmentCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#treatmentCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
</section>

<style>
  .treatment-section .card {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border: none;
}

.treatment-section img {
  height: 200px;
  object-fit: cover;
}

.carousel-item {
  display: flex;
  justify-content: center;
}
</style>