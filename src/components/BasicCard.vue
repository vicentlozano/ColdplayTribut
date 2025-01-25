<template>
  <div class="card">
    <img :alt="props.title" :src="props.img" class="img-disc" />
    <div class="info">
      <button class="open" v-if="!bool" @click="bool = !bool">
        <img src="../../public/plus_120249.png" /><span>Mas info</span>
      </button>
      <!-- Lista de bootstrap -->
      <div :class="bool ? 'show' : 'no-show'">
        <ul class="list-group">
          <li class="list-group-item">{{ title }}</li>
          <li class="list-group-item">{{ price }}</li>
          <li class="list-group-item">{{ year }}</li>
          <li class="list-group-item"><a :href="link">Comprar</a></li>
          <li class="list-group-item">
            <button @click="bool = !bool" class="close">volver</button>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const props = defineProps({
  img: String,
  title: String,
  price: String,
  year: String,
  link: String,
})
const bool = ref(false)
</script>

<style lang="scss" scoped>
.card {
  display: grid;
  border: 2px solid white;
  grid-template-columns: 1fr 1fr;
  border-radius: 20px;
  justify-content: center;
  height: fit-content;
  width: 100%;
  height: 100%;
  box-shadow: 1px 4px 10px 0px rgb(85, 88, 85);
  text-align: center;
  background-color: rgb(49, 49, 46);
  color: black;
  border-bottom-left-radius: 0px;
  border-bottom-right-radius: 0px;
}
.img-disc {
  height: 100%;
  width: 200px;
  min-height: 200px;
  border-top-left-radius: 25px;
}
h5 {
  display: flex;
  color: whitesmoke;
  justify-content: center;
  gap: 1rem;
  letter-spacing: 0.1em;
  margin: 0;
}
.open {
  text-align: center;
  width: 100%;
  border-top-right-radius: 20px;
  border-color: transparent;
}
.no-show {
  display: none;
  transition: all 1s ease;
  opacity: 0;
}
.show {
  display: flex;
  transition: all 1s ease;
  opacity: 1;
}

p {
  width: 100%;
  height: fit-content;
  margin: 0;
}
.info {
  display: grid;
  grid-template-rows: 1fr;
  transition: all 1s ease;
}
.open:hover {
  background-color: rgb(127, 144, 138);
}

ul,
li {
  width: 100%;
  border-radius: 0px;
  background-color: transparent;
  height: 100%;
  color: whitesmoke;
}

li:first-child {
  border-top-right-radius: 18px;
}
.open {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  background-color: transparent;
  color: white;
  transition: all 1s ease;
}
.close {
  background-color: transparent;
  padding: 0 1rem;
  border: 1px solid white;
  border-radius: 10px;
  color: rgb(59, 134, 195);
  transition: all 0.6s ease;
}
.close:hover {
  background-color: white;
  color: black;
}
a {
    text-decoration: none;
}
</style>
