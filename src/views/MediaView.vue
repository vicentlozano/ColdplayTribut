<template>
  <div>
    <div>
      <h3 class="section-title" id="concerts-heading" aria-labelledby="concerts-heading">CONCIERTOS</h3>
    </div>
    <section class="concerts" aria-labelledby="concerts-heading">
      <IframeCard class="max-width"
        video-url="https://www.youtube.com/watch?v=Fpn1imb9qZg&pp=ygUSY29uY2llcnRvIGNvbGRwbGF5"
        aria-label="Concierto de Coldplay en vivo, interpretación de su música."
      />
      <IframeCard class="max-width"
        video-url="https://www.youtube.com/watch?v=tPUd5iqq7wA&pp=ygUSY29uY2llcnRvIGNvbGRwbGF5"
        aria-label="Concierto de Coldplay, presentación de una de sus canciones."
      />
      <IframeCard class="max-width"
        video-url="https://www.youtube.com/watch?v=-Nwa2U-7sQA&pp=ygUSY29uY2llcnRvIGNvbGRwbGF5E"
        aria-label="Coldplay en concierto, una de sus interpretaciones en vivo."
      />
      <IframeCard class="max-width"
        video-url="https://www.youtube.com/watch?v=KyDQ7cBOS6I&pp=ygUSY29uY2llcnRvIGNvbGRwbGF5"
        aria-label="Presentación de Coldplay en un evento en vivo."
      />
      <IframeCard class="max-width"
        video-url="https://www.youtube.com/watch?v=rLm_aSP369M&list=PLsvoYlzBrLFBBe82GvEx6GQztG6m_Y2UD&index=1&pp=iAQB8AUB"
        aria-label="Concierto completo de Coldplay, interpretando sus éxitos."
      />
      <IframeCard class="max-width"
        video-url="https://www.youtube.com/watch?v=9ldOuVuas1c&list=PLsvoYlzBrLFBBe82GvEx6GQztG6m_Y2UD&index=2&pp=iAQB8AUB"
        aria-label="Coldplay en un evento en vivo, con su famosa música."
      />
      <IframeCard class="max-width"
        video-url="https://www.youtube.com/watch?v=mRP72Ib2e9I&list=PLsvoYlzBrLFBBe82GvEx6GQztG6m_Y2UD&index=3&pp=iAQB8AUB"
        aria-label="Interpretación de Coldplay en concierto, grabación en vivo."
      />
    </section>
    <h3 class="section-title" id="videos-heading" aria-labelledby="videos-heading">VIDEOS</h3>
    <section class="videos" aria-labelledby="videos-heading">
      <div>
        <h1>Scientist</h1>
        <video controls class="custom-video" id="video1" aria-label="Video oficial de 'Scientist' de Coldplay">
          <source
            src="../../public/video/Coldplay - The Scientist (Official 4K Video).mp4"
            type="video/mp4"
            class="custom-video"
          />
          Your browser does not support the video tag.
        </video>
      </div>
      <div>
        <h1>We Pray</h1>
        <video controls class="custom-video" id="video2" aria-label="Video oficial de 'We Pray' de Coldplay">
          <source
            src="../../public/video/coldplay-we-pray-tini-version-official_UhrrF6lT.mp4"
            type="video/mp4"
            class="custom-video"
          />
          Your browser does not support the video tag.
        </video>
      </div>
    </section>
    <h3 class="section-title" id="songs-heading" aria-labelledby="songs-heading">CANCIONES</h3>
    <section class="canciones" aria-labelledby="songs-heading">
      <AudioCard audio="../../public/audio/scientist.mp3" title="scientist" aria-label="Audio de la canción 'Scientist' de Coldplay" />
      <AudioCard
        audio="../../public/audio/Coldplay - AETERNA (Official Lyric Visualiser).mp3"
        title="AETERNA"
        aria-label="Audio de la canción 'AETERNA' de Coldplay"
      />
      <AudioCard
        audio="../../public/audio/Coldplay - Fix You (Official Video).mp3"
        title="Fix You"
        aria-label="Audio de la canción 'Fix You' de Coldplay"
      />
      <AudioCard audio="../../public/audio/Coldplay - Yellow (Official Video).mp3" title="Yellow" aria-label="Audio de la canción 'Yellow' de Coldplay" />
      <AudioCard
        audio="../../public/audio/Coldplay - Man in The Moon (Official Lyric Visualiser).mp3"
        title="Man in The Moon"
        aria-label="Audio de la canción 'Man in The Moon' de Coldplay"
      />
    </section>
  </div>
</template>


<script setup>
import AudioCard from '@/components/AudioCard.vue'
import IframeCard from '@/components/IframeCard.vue'
</script>

<style lang="scss" scoped>
.section-title {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 3em;
  font-weight: bold;
  height: 200px;
  width: 100%;
  background: -webkit-linear-gradient(90deg,#222120,#312e26,#45423a); /* Chrome 10-25, Safari 5.1-6 */ background: linear-gradient(90deg,#222120,#312e26,#45423a); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  border-bottom: 2px solid white;
  border-top: 2px solid white;

  text-align: center;
  letter-spacing: 0.1em;
}
.videos {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
  grid-auto-rows: auto;
  justify-items: center;
  gap: 4rem;
  padding: 1rem;
}
.custom-video {
  height: 80%;
  width: 100%;
}

.concerts {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-auto-rows: auto;
  gap: 1rem;
  padding: 1rem;
}
.canciones {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  grid-auto-rows: auto;
  gap: 4rem;
  padding: 1rem;
  margin-top: 2rem;
  justify-items: center;
  align-items: center;
  width: 100%;
}
@media (min-width: 700px) and (max-width: 1300px) {
  .concerts {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: auto;
    gap: 1rem;
    padding: 1rem;
  }
}
@media (max-width: 699px) {
  .concerts {
    display: grid;
    grid-template-columns: 1fr;
    grid-auto-rows: auto;
    gap: 1rem;
    padding: 1rem;
  }
  .videos {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-auto-rows: auto;
  justify-items: center;
  gap: 4rem;
  padding: 1rem;
}
.custom-video {
  height: 80%;
  width: 100%;
  max-width: 350px;
}
.max-width {
  max-width: 100%;
}
}
</style>
