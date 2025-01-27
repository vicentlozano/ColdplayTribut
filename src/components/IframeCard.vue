<template>
  <div class="youtube-container">
    <div class="d-flex justify-content-center align-items-center" v-if="!bool">
      <div class="spinner-border" role="status">
        <span class="visually-hidden">Loading...</span>
      </div>
    </div>
    <iframe
      v-show="bool"
      :src="embedUrl"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </div>
</template>

<script setup>
import { computed, ref, onMounted } from 'vue'

// Definimos la prop que recibirá el enlace del video de YouTube.
const props = defineProps({
  videoUrl: {
    type: String,
    required: true,
  },
})

// Computamos el enlace del iframe (formato embed).
const embedUrl = computed(() => {
  const videoId = props.videoUrl.split('v=')[1]?.split('&')[0] // Extraemos el ID del video.
  return `https://www.youtube.com/embed/${videoId}`
})

const bool = ref(false)

onMounted(() => {
  setTimeout(() => {
    bool.value = true // Después de 3 segundos, se oculta el spinner.
  }, 1000) // 3000 milisegundos = 3 segundos
})
</script>

<style lang="scss" scoped>
.youtube-container {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  width: 100%;
  padding-bottom: 56.25%; /* Mantiene la relación de aspecto 16:9 */
  height: 0;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.youtube-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.d-flex {
  position: absolute; /* Asegura que se posicione dentro del contenedor */
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%); /* Centra el spinner */
}
</style>
