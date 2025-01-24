<template>
  <div class="basic-container">
    <section class="cards p-4">
      <BasicCard />
      <BasicCard />
      <BasicCard />
      <BasicCard />
      <BasicCard />
      <BasicCard />
    </section>
    <section class="carrusel">
      <div
        id="carouselExampleCaptions"
        class="carousel slide carousel-fade custom"
        data-bs-ride="carousel"
      >
        <div class="carousel-indicators">
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="0"
            class="active"
            aria-current="true"
            aria-label="Slide 1"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="1"
            aria-label="Slide 2"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="2"
            aria-label="Slide 3"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="3"
            aria-label="Slide 4"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide-to="4"
            aria-label="Slide 5"
          ></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="../assets/coldplay1.jpg" class="custom-image" alt="..." />
            <div class="carousel-caption d-none d-md-block">
              <h5>First slide label</h5>
              <p>Some representative placeholder content for the first slide.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="../assets/coldplay2.jpg" class="custom-image" alt="..." />
            <div class="carousel-caption d-none d-md-block">
              <h5>Second slide label</h5>
              <p>Some representative placeholder content for the second slide.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="../assets/coldplay3.jpg" class="custom-image" alt="..." />
            <div class="carousel-caption d-none d-md-block">
              <h5>Third slide label</h5>
              <p>Some representative placeholder content for the third slide.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="../assets/coldplay4.jpg" class="custom-image" alt="..." />
            <div class="carousel-caption d-none d-md-block">
              <h5>Third slide label</h5>
              <p>Some representative placeholder content for the third slide.</p>
            </div>
          </div>
          <div class="carousel-item">
            <img src="../assets/coldplay5.jpg" class="custom-image" alt="..." />
            <div class="carousel-caption d-none d-md-block">
              <h5>Third slide label</h5>
              <p>Some representative placeholder content for the third slide.</p>
            </div>
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleCaptions"
          data-bs-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleCaptions"
          data-bs-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </section>
  </div>
</template>

<script setup>
import BasicCard from '@/components/BasicCard.vue'
</script>

<style scoped>
.basic-container {
  display: grid;
  grid-template-rows: 1fr 1fr;
  height: 100%;
  width: 100%;
}
.cards {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 2rem;
  height: 100%;
  width: 100%;
}
.disc {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  margin-bottom: 1rem;
}
.row {
  height: 100%;
  width: 100%;
  margin: 0;
}
.discographic {
  margin: 0;
  padding: 0;
}
.custom-image {
  height: 700px;
  width: 100%;
  padding: 2rem;
  border-radius: 100px;
}
@media (max-width: 576px) {
  .cards {
    grid-template-columns: 1fr;
    grid-template-rows: auto;
  }
  .custom-image {
    height: 400px;
    width: 100%;
    padding: 1rem;
    border-radius: 15%;
  }

}
@media (min-width: 577px) and (max-width: 768px) {
  .cards {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
  }
}
@media (min-width: 769px) {
  .cards {
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr;
  }
  img {
    width: 100%;
    height: 100%;
  }
}
</style>
