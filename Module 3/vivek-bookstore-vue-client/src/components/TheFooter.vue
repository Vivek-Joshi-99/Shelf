<script setup lang="ts"></script>

<style scoped>
footer {
  background: var(--default-text-color);
  display: flex;
  gap: 1em;
  color: white;
  font-family: var(--title-font-family);
  justify-content: space-between;
}

.links,
.social-media-icons {
  display: flex;
  flex-direction: row;
  color: white;
}
.links{
  justify-content: center;

}

.social-media-icons {
  align-self: right;
  gap: 0.25em;
  justify-content: flex-end;
}

footer > section {
  flex-basis: 30%;
}

</style>

<template>
  <footer class="container">
    <!-- <section class="links">
      <router-link to="/">about</router-link>
      <router-link to="/">contact</router-link>
      <router-link to="/">directions</router-link>
    </section>
    <section class="social-media-icons">
      <router-link to="/" class="button">Facebook</router-link>
      <router-link to="/" class="button">Twitter</router-link>
    </section> -->
    <section class="Copyright">
        <p><i class="fa-regular fa-copyright"></i> 2023 Shelf Booksellers,Inc.</p>
      </section>
      <section class="links">
        <router-link to="/">Directions</router-link>
        <p>&nbsp|&nbsp</p>
        <router-link to="/">Contact</router-link>
        <p>&nbsp|&nbsp</p>
        <router-link to="/">About</router-link>
      </section>
      <section class="social-media-icons">
        <router-link to="/" ><i class="fa-brands fa-facebook"></i></router-link>
        <router-link to="/" ><i class="fa-brands fa-instagram"></i></router-link>
        <router-link to="/" ><i class="fa-brands fa-twitter"></i></router-link>
      </section>
  </footer>
</template>
