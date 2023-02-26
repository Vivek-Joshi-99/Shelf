<script setup lang="ts"></script>

<style scoped>
  .search-bar {
  /* position: relative; */
  padding: 0.5em;
  border-radius: 20px 0px 0px 20px;
  border-color: var(--default-text-color);
  background-color: var(--secondary-color);
  width: 90%;
  border-right: 0px;

}




.search-button {
  /* font-size: 1.25rem; */
  padding: 0.5em;
  /* position: absolute; */
  /* background: none; */
  border: none;
  /* right: 25rem;
  top: 1.4rem; */
  cursor: pointer;
  border-radius: 0px 20px 20px 0px;
  color: white;
  background-color: var(--default-text-color);
  border-color: var(--default-text-color);
  border: 2px solid var(--default-text-color);
  /* height: 2.25rem; */
  /* width: 10%; */
  z-index: 2;
  width: 10%;
}


</style>

<template>
  <section>
      <form action="/" class="search-bar-and-button">
        <input type="text" placeholder="Browse For Books......" class="search-bar" />
        <button type="submit" class="search-button" value="Search">
          <i class="fa-solid fa-magnifying-glass"></i>
        </button>
      </form>
    </section>
</template>
