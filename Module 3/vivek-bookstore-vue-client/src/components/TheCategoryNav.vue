<script setup lang="ts">
import { inject } from "vue";
import type { CategoryItem } from "@/types";
const categoryList = inject("categoryList") as CategoryItem[];
</script>

<style scoped>
.category-heading {
  background-color: var(--default-text-color);
  color: white;
  padding: 0.75rem;
  font-size: 2rem;
}

.category-buttons {
  display: flex;
  flex-direction: column;
  text-align: center;
  flex: 10%;
  font-size: 1.5rem;
  background-color: var(--secondary-color);
}

.button.category-button.router-link-active {
  background-color: white;
  color: black;
  border-radius: 20px;
  width: 100%;
}

.button.category-button.router-link-active:hover{
  background-color: white;
}

.button.category-button {
  background-color: var(--secondary-color);
  color: black;
  min-width:auto;
}

.button.category-button:hover,
.button.category-button:active {
  background-color: #96908a;
  color: black;
  border-radius: 20px;
  width: 100%;
}


.category-nav {
  background-color: var(--secondary-color);
}
</style>

<template>
  
    <ul class="category-buttons">
      <li class="category-heading">
        Category
      </li>
      <li v-for="category in categoryList" :key="category.categoryId">
        <router-link
          :to="'/category/' + category.name"
          class="button category-button"
        >
          {{ category.name }}
        </router-link>
      </li>
    </ul>
  
</template>
