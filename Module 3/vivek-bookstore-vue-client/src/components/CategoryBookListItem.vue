<script setup lang="ts">
import { defineProps } from "vue";
import type { BookItem } from "../types";
const props = defineProps<{
  book: BookItem;
}>();
const bookImageFileName = function (book: BookItem): string {
  let name = book.title.toLowerCase();
  name = name.replace(/ /g, "-");
  name = name.replace(/'/g, "");
  return `${name}.gif`;
};
</script>
<style scoped>
.book-info {
  display: flex;
  flex-direction: column;
  flex: 50%;
  justify-content: space-between;
}

.book-box {
  /* font-size: 1.15rem; */
  display: flex;
  flex-direction: row;
  background-color: var(--card-background-color);
  padding: 1em;
  margin:1rem;
  justify-content: space-around;
  border-radius: 1rem;
  height: 15rem;
  flex-basis: 30%;


}
.book-image{
  flex:50%;
  /* position:relative; */
  margin-right: 0.15rem;
}


.book-image img{
  width: 8.5rem;
  height:13rem;
  display: block;
  border-radius: 10px;
}

.book-title-and-author{
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}

.book-title {
  font-weight: bold;
}

.book-author {
  /* font-style: italic; */
  font-family: var(--highlighted-font);
  /* font-size: larger; */
}

.category-book-list{
  flex:85%;
  /* background-image: url("/images/site/background_img.jpg");
  background-size: cover;
  background-position: center; */
  /* padding: 1rem; */
  /* background-color: white; */
}

.book-price {
  color: #1b8800;
  font-family: var(--title-font-family);
}

.button-book {
  border-radius: 8px;
}



.eye-button{
  background: black;
  border-radius: 2rem;
  padding: 0.5rem;
  /* position: absolute; */
  top: -0.5rem;
  right: 1.25rem;
  color: white;
  /* transform: translate(20px, -53px); */
}

.eye-button-pos{ /*Added to change position of eye button*/
  transform: translate(96px, -192px);
}
</style>

<template>
  <li class="book-box">
    <div class="book-image">
      <div>
        <img
        :src="'/book-images/' + bookImageFileName(props.book)"
        :alt="book.title"
      />
      </div>
      <div v-if="book.isPublic" class="eye-button-pos"><span class="eye-button" v-if="book.isPublic"><i class="fa-solid fa-eye"></i></span></div>
      
    </div>
    <div class="book-info">
      <div class="book-title-and-author">
        <div class="book-title">{{ book.title }}</div>
        <div class="book-author">{{ book.author }}</div>
      </div>

      <div>
      <div class="book-price">${{ (book.price / 100).toFixed(2) }}</div>
      <button class="button-book button"><i class="fa-solid fa-cart-shopping"></i>&nbspAdd to Cart</button>
    </div>

    </div>
    
  </li>
</template>
