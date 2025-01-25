<template>
  <div class="about">
    <div class="paralax"></div>
    <h3>COMPONENTES</h3>
    <section class="components">
      <PersonCard
        name="Chris Martin"
        age="46"
        position="Vocalista y pianista"
        curiosities="Lider de la banda, exesposo de Gwyneth Paltrow."
        img="../../public/chrisMartins.jpg"
        link="https://es.wikipedia.org/wiki/Chris_Martin"
      />
      <PersonCard
        name="Jonny Buckland"
        age="47"
        position="Guitarrista"
        curiosities="Fundador de la banda junto con Chris Martin."
        img="../../public/jonny.jpg"
        link="https://es.wikipedia.org/wiki/Jonny_Buckland"
      />
      <PersonCard
        name="Will Champion"
        age="46"
        position="Baterista"
        curiosities="Miembro más experimentado de la banda."
        img="../../public/WillChampion.jpg"
        link="https://es.wikipedia.org/wiki/Will_Champion"
      />
      <PersonCard
        name="Guy Berryman"
        age="47"
        position="Bajista"
        curiosities="Es un gran amante del diseño y la fotografía."
        img="../../public/GuyBerryman.jpg"
        link="https://es.wikipedia.org/wiki/Guy_Berryman"
      />
    </section>
    <section class="history">
      <h3>HISTORIA DEL GRUPO</h3>
      <div class="information">
        <p>
          Coldplay es una banda británica de rock alternativo formada en Londres en 1997. Está
          integrada por Chris Martin (vocalista principal y pianista), Jonny Buckland (guitarrista),
          Guy Berryman (bajista), Will Champion (baterista y vocalista secundario) y Phil Harvey
          (director creativo). Se conocieron en el University College London y comenzaron a tocar
          música juntos desde 1997 hasta 1998, inicialmente llamándose a sí mismos Big Fat Noises y
          luego Starfish.
        </p>
        <p>
          Después de lanzar de forma independiente un EP, Safety (1998), Coldplay firmó con
          Parlophone en 1999. El álbum debut de la banda, Parachutes (2000), incluyó su exitoso
          sencillo «Yellow» y recibió un Brit Award por Álbum Británico del Año, un Premio Grammy al
          Mejor Álbum de Música Alternativa y nominación al Premio Mercury. Su segundo álbum, A Rush
          of Blood to the Head (2002), ganó los mismos elogios e incluyó los sencillos «The
          Scientist» y «Clocks», y este último ganó un premio Grammy por Grabación del año.
        </p>
        <p>
          Desde entonces, Coldplay diversificó aún más su sonido con los lanzamientos posteriores
          Mylo Xyloto (2011), Ghost Stories (2014), A Head Full of Dreams (2015), Everyday Life
          (2019) y Music of the Spheres (2021). Cada álbum presentaba un tema único y añadía nuevos
          estilos musicales al repertorio original de la banda, incluyendo electrónica, ambient,
          pop, R&B, funk, clásica, jazz fusión y rock progresivo.
        </p>
        <p>
          Con más de 100 millones de álbumes vendidos en todo el mundo, Coldplay es el acto más
          exitoso del siglo xxi y uno de los actos musicales más vendidos de todos los tiempos.
          Coldplay también se considera una de las bandas más influyentes del siglo xxi, y Forbes
          los describe como el estándar para la escena alternativa actual.
        </p>
      </div>
    </section>
  </div>
</template>
<script setup lang="ts">
import PersonCard from '@/components/PersonCard.vue'
</script>
<style scoped>
.paralax {
  display: flex;
  width: 100%;
  height: 70vh;
  background-image: url('../assets/coldplaybib.jpg');
  background-attachment: fixed;
  background-position: center;
  background-color: black;
  background-repeat: no-repeat;
  background-size: contain;
  background-position-x: center;
}
.components {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-auto-flow: row;
  align-items: center;
  margin: 3rem 0;
  gap: 2rem;
  justify-items: center;
}
.about {
  display: flex;
  flex-direction: column;
}
h3 {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 3em;
  font-weight: 900;
  height: 200px;
  width: 100%;
  border-top: 2px solid white;
  border-bottom: 2px solid white;
  text-align: center;
  letter-spacing: 0.1em;
}
.information p {
  padding: 2em;
  font-size: larger;
  text-align: justify;
}

@media (max-width: 1200px) {
  .components {
    grid-template-columns: repeat(2, 1fr); /* 2 columnas en pantallas medianas */
  }
}

@media (max-width: 768px) {
  .components {
    grid-template-columns: 1fr; /* 1 columna en pantallas pequeñas */
  }
  h3 {
    font-size: 2em;
  }
  .paralax {
    height: 30vh;
    background-position-y: 20%;
  }
}
</style>
