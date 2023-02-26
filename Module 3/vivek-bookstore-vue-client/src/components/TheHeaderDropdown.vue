<script setup lang="ts">
import { inject } from "vue";
import type { CategoryItem } from "../types";
const categoryList = inject("categoryList") as CategoryItem[];
</script>

<style scoped>
.header-dropdown {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.categories-button , .categories-button:hover {
  background-color: var(--secondary-color);
  margin-top: 0.25em;
  
  border-color: var(--default-text-color);
  color: var(--default-text-color);
  /* padding: 1px 1px; */
  border-radius: 20rem;
  box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.5);
  min-width: max-content;
}



.header-dropdown ul {
  background-color: white;
  color: black;
  display: none;
  border-radius: 1rem;
}

.header-dropdown li {
  padding: 0.25em 0.5em;
}

.header-dropdown a {
  color: black;
  text-decoration: none;
}

.header-dropdown li:hover {
  background: var(--default-text-color);
  border-radius: 1rem;
}

.header-dropdown li:hover a{
  color: white;
}

.header-dropdown:hover ul {
  display: block;
  min-width: inherit;
  padding: inherit;
  margin:inherit;
  z-index: 1;
  cursor: pointer;
}
</style>

<template>
  <div class="header-dropdown">
    <button class="categories-button">Categories &nbsp;<i class="fa-solid fa-square-caret-down"></i></button>
    <ul class="category-dropdown">
      <li v-for="category in categoryList" :key="category.categoryId">
        <router-link :to="'/category/' + category.name">
          {{ category.name }}
        </router-link>
      </li>
    </ul>
  </div>
</template>
