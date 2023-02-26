<script setup lang="ts">
import router from "@/router";

const jump = function () {
  router.push("/category/Classics")
}
</script>

<style scoped>
.home-page {
  display: flex;
  background-image: url("../public/site-images/background_img.jpg");
  background-size: cover;
  background-position: center;
  /* height: 100vh; */
  flex-direction: column;
  align-items: flex-end;
  flex-grow: 3;
  /* height: 84vh; */
}

.welcome-text {
  width: 20em;
  margin: 2rem;
  background-color: var(--secondary-color);
  border-radius: 2rem;
  font-family: var(--title-font-family);
  /* flex-grow: 1; */
  display: flex;
  flex-direction: column;
  /* width: 40%; */
  font-size: 1.5rem;
  line-height: 1.25;
  /* max-height: 8em; */
  /* overflow: auto; */
}

.author-spotlight {
  margin-top: 0px;
  align-items: center;
  text-align: center;
}

.category-image-items {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 1em;
}

.category-image-items a {
  text-align: center;
  cursor: pointer;
}

.category-image-items div {
  padding: 0.5em 0;
  background: rgba(0, 0, 0, 0.5);
  /* last # is percent opacity */
  color: white;
  transform: translateY(-2.25em);
  margin-bottom: -2em;
}

.call-to-action {
  box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.5);
  border-radius: 1rem;
  width: 70%;
  align-self: center;

}



.books-home {
  display: flex;
  flex-direction: row;
  /* gap:1rem; */
  justify-content: space-around;
}

.books-images-home {
  border-radius: 0.5rem;
  margin: 1rem;
}
</style>
<template>
  <div class="home-page">
    <div class="welcome-text flow-content container">
      <p>Find your next read, from our vast selection of fiction, fantasy, mystery books and more...</p>
      <button @click="jump" class="button call-to-action ">SHOP FOR BOOKS!</button>
    </div>


    <div class="author-spotlight welcome-text flow content container">
      <p>Today's Spotlight: <br />MYSTERY</p>
      <div class="books-home">
        <img class="books-images-home" src="/book-images/hb1.gif" alt="The Mystery of Mrs. Christie" />
        <img class="books-images-home" src="/book-images/hb2.gif" alt="The Mystery of the Blue Train" />
        <img class="books-images-home" src="/book-images/hb3.gif" alt="The Hardy Boys" />
      </div>
    </div>




    <!-- <div>
          <ul>
            <li>
              <div class="book-image">
              <img
                :src="'/book-images/' + bookImageFileName(props.book)"
                :alt="book.title"
              />
               </div>
            </li>
          
          </ul>
        </div> -->

  </div>
</template>
