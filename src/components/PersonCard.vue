<template>
  <div>
    <div class="card" style="width: 18rem">
      <img :src="img" class="card-img-top" alt="..." />
      <div class="card-body">
        <h5 class="card-title">{{ props.name }}</h5>
        <p class="card-text">Edad: {{ age }}</p>
        <p class="card-text">Rol: {{ position }}</p>
        <p class="card-text">Curiosidad: {{ curiosities }}</p>
        <a :href="link" class="btn btn-primary">Mas info</a>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  name: String,
  age: String,
  position: String,
  curiosities: String,
  img: String,
  link: String,
})
</script>

<style scoped>
img {
  width: 100%;
  height: 300px;
  object-fit: cover;
}
.card-body {
    background-color: rgb(49, 49, 46);
    color: whitesmoke;
}
.card {
    transition: transform 0.3s ease-out ;
}
.card:hover {
    transform: scale(1.03);
}

</style>
