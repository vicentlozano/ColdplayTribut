<script setup>
// import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <section class="principal-grid">
    <header>
      <nav class="nav">
        <h1>Coldplay Tribut</h1>
        <RouterLink class="link" to="/">Home</RouterLink>
        <RouterLink class="link" to="/about">About</RouterLink>
        <RouterLink class="link" to="/media">Media</RouterLink>
      </nav>
    </header>
    <main>
      <RouterView />
    </main>
    <footer>
      <div id="footer">
        <h3>Vilodev@Copyright</h3>

        <div class="icons">
          <a href="https://github.com/vicentlozano">
            <img
              src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/github.svg"
              alt="GitHub"
              width="32"
              height="32"
          /></a>
          <a href="mailto:lozanodroid@gmail.com">
            <img
              src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/gmail.svg"
              alt="Gmail"
              width="32"
              height="32"
          /></a>
          <a href="https://www.instagram.com/vicentlozano94">
            <img
              src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/instagram.svg"
              alt="Instagram"
              width="32"
              height="32"
            />
          </a>
        </div>
      </div>
    </footer>
  </section>
</template>

<style scoped>
#app,
header {
  display: flex;
  flex-direction: column;
  background-color: rgba(37, 43, 41, 0.323);
}
.principal-grid {
  display: grid;
  grid-template-rows: minmax(100px, auto) 1fr minmax(60px, auto);
  width: 100%;
  height: 100%;
}
main {
  width: 100%;
  height: 100%;
}
footer {
  display: inline;
  border-top: 2px solid white;
}
.nav {
  display: grid;
  grid-template-columns: 4fr 1fr 1fr 1fr;
  justify-items: center;
  align-items: center;
  width: 100%;
  border-bottom: 2px solid white;
  gap: 2px;
}
.link {
  color: white;
  text-decoration: none;
  width: 50%;
  height: fit-content;
  padding: 0.6rem;
  border-radius: 25px;
}
.link:hover {
  background-color: white;
  color: black;
  transition: 0.5s ease;
}
#footer {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0 2em;
  height: 100%;
  justify-content: space-evenly;
  gap: 10rem;
  width: 100%;
}
.icons {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  align-items: center;
}
a,
img {
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.8s ease;
}
.icons img:hover {
  background-color: rgb(22, 158, 221);
  border-radius: 40%;
  padding: 0.2rem;
}
h1 {
  padding: 1rem;
  letter-spacing: 0.3em;
}
h3 {
  font-size: larger;
  padding: 0.3rem;
  margin: 0;
}
@media (max-width: 600px) {
  #footer {
    gap: 1rem;
  }
  .nav {
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1.5fr 1fr;
    gap: 0;
  }
  h1 {
    margin-bottom: 0;
  }
  .link {
    padding: 0.1rem;
  }
  .icons img {
    width: 26px;
    height: 26px;
  }
  h3 {
    font-size: medium;
  }
  h1 {
    grid-column: 1 / -1;
  }
}
</style>
