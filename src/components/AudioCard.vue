<template>
  <div class="card-audio">
    <h5 class="mb-1 title-audio">{{ title }}</h5>
    <audio controls>
      <source :src="props.audio" type="audio/mp3" />
      Music Free
    </audio>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'

// Prop que acepta una URL de audio o un archivo.
const props = defineProps({
  audio: {
    type:  String, // Acepta tanto rutas como archivos.
    required: true,
  },
  title: String,
})

// Referencia reactiva para la fuente del audio.
const audioSrc = ref(null)

// Actualiza la fuente del audio según la prop.
watch(
  () => props.audio,
  (newAudio) => {
    if (newAudio instanceof File) {
      // Si es un archivo, crea una URL temporal.
      audioSrc.value = URL.createObjectURL(newAudio)
    } else if (typeof newAudio === 'string') {
      // Si es una URL, úsala directamente.
      audioSrc.value = newAudio
    }
  },
  { immediate: true },
)
</script>

<style lang="scss" scoped>
.audio-player {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  background-color: #f4f4f4;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
.card-audio {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    min-width: 300px;
    background-color: rgb(49, 47, 47);
    padding: 1rem;
    justify-content: center;
    align-items: center;
    border-radius: 25px;
}
.title-audio {
    letter-spacing: 0.1em;
    font-weight: bold;
    text-transform: uppercase;
}

audio {
  width: 100%;
  max-width: 600px;
  outline: none;
}
</style>
