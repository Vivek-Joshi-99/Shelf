<script setup lang="ts">
import { defineProps } from "vue"; // needed if you don't want an error below
import type { BookItem } from "@/types";
import CategoryBookListItem from "@/components/CategoryBookListItem.vue";
const props = defineProps<{
  bookList: BookItem[];
}>();
</script>

<style scoped>
ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  overflow: auto;
  padding: 1em;
}
.category-book-list{
  flex:80%;
  /* background-image: url("/images/site/background_img.jpg");
  background-size: cover;
  background-position: center; */
  /* padding: 1rem; */
  /* background-color: white; */
}
</style>

<template>
  <ul class="category-book-list">
    <template v-for="book in props.bookList" :key="book.bookId">
      <category-book-list-item :book="book"></category-book-list-item>
    </template>
  </ul>
</template>
