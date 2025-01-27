<template>
  <div class="auto-scroll">
    <ul>
      <li>
        <strong>2002:</strong> Grammy Award - Mejor Álbum de Música Alternativa por
        <em>Parachutes</em>.
      </li>
      <li>
        <strong>2004:</strong> Brit Award - Álbum Británico del Año por
        <em>A Rush of Blood to the Head</em>.
      </li>
      <li><strong>2009:</strong> Grammy Award - Canción del Año por <em>"Viva la Vida"</em>.</li>
      <li>
        <strong>2009:</strong> Grammy Award - Mejor Álbum de Rock por
        <em>Viva la Vida or Death and All His Friends</em>.
      </li>
      <li><strong>2012:</strong> Brit Award - Mejor Grupo Británico.</li>
      <li><strong>2014:</strong> MTV Europe Music Award - Mejor Rock.</li>
      <li><strong>2017:</strong> American Music Award - Artista Favorito de Rock Alternativo.</li>
      <li>
        <strong>2020:</strong> Billboard Music Award - Mejor Álbum de Rock por
        <em>Everyday Life</em>.
      </li>
      <li>
        <strong>2008:</strong> MTV Video Music Award - Mejor Dirección Artística por
        <em>"Viva la Vida"</em>.
      </li>
      <li><strong>2013:</strong> Billboard Music Award - Mejor Artista de Rock.</li>
      <li>
        <strong>2015:</strong> Teen Choice Award - Mejor Canción de Rock con
        <em>"A Head Full of Dreams"</em>.
      </li>
      <li>
        <strong>2021:</strong> MTV Video Music Awards - Nominación a Mejores Efectos Visuales con
        <em>"Higher Power"</em>.
      </li>
    </ul>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.auto-scroll {
  height: 100%; /* Altura del contenedor */
  overflow: hidden; /* Oculta el contenido fuera del contenedor */
  padding: 1rem;
  background-color: #343030;
  font-size: 2.5rem; /* Tamaño más grande del texto */
  color: whitesmoke;
  line-height: 3.5rem; /* Espaciado entre líneas */
  position: relative;
}

.auto-scroll ul {
  list-style: none; /* Sin puntos de lista */
  padding: 0;
  margin: 0;
}

.auto-scroll li {
  margin-bottom: 1.5rem; /* Espaciado entre los elementos */
  margin-left: 1em;
  margin-right: 1em;
}

.auto-scroll ul {
  position: absolute;
  animation: scroll-up 30s linear infinite; /* Animación continua */
}

@keyframes scroll-up {
  0% {
    transform: translateY(30%); /* Empieza fuera del contenedor */
  }
  100% {
    transform: translateY(-100%); /* Termina fuera por la parte superior */
  }
}
@media (max-width: 768px) {
  .auto-scroll {
    font-size: 1.5rem; /* Tamaño más grande del texto */
  }
  .auto-scroll ul {
  animation: scroll-up 35s linear infinite; /* Animación continua */
}
}
@media (min-width: 769px) and (max-width: 1300px) {
  .auto-scroll {
    font-size: 2rem; /* Tamaño más grande del texto */
  }
}
</style>
