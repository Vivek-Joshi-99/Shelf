<script setup lang="ts">
import TheHeaderDropdown from "../components/TheHeaderDropdown.vue";
import TheHeaderSearchBar from "./TheHeaderSearchBar.vue";
</script>

<style >
header {
  background: var(--header-bg-color);
  display: flex;
  padding: 1em;
  gap: 1em;
  justify-content: space-between;
  align-items: center;
  max-height: 5rem;
  /* flex-wrap: wrap; */
}

.bookstore-logo-and-title {
  display: flex;
  flex-direction: row;
  gap: 0.5rem;
}



section.text-logo>p {
  line-height: 1.3;
  font-size: 0.75rem;

}

section.text-logo>h1 {
  font-size: 1rem;
}


.text-logo {
  font-family: var(--title-font-family);
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.5);
}

header>section {
  flex-basis: 100%;
}

.search-bar-and-button {
  display: flex;
  /* text-align: center; */
  /* gap: 0px; */
  align-items: center;
  flex-basis: 100%;
  /* justify-content: spac; */
}


input:focus {
  color: var(--default-text-color);
  outline: none;
}



.login {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-width: max-content;
}

.header-buttons {
  display: flex;
  justify-content: right;
  gap: 20px;
  max-height: 3rem;
}

.cart {
  text-align: center;
}

.cart-count {
  color: white;
  transform: translateY(-50px);
  font-weight: bolder;
  background-color: red;
  border-radius: 15px;
  height: 0.75rem;
  font-size: 0.75rem;
  width: 0.75rem;
  transform: translate(20px, -53px);
}

.header-dropdown-and-cart {

  background-color: var(--secondary-color);
  margin-top: 0.25em;
  border-radius: 20rem;
  border-color: var(--default-text-color);
  color: var(--default-text-color);
  box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.5);
}


/* @media (max-width: 600px) {
  header {
    flex-direction: column;
  }
} */
</style>

<template>
  <header class="container">
    <!-- <section class="bookstore-logo">
        <router-link to="/">
          <img
            src="/site-images/bookstore-logo.png"
            alt="Another Bookstore Logo"
            width="150"
            height="auto"
          />
        </router-link>
      </section>
      <section class="title-and-search-bar">
        <h1>
          <router-link to="/" class="text-logo"> Another Bookstore </router-link>
        </h1>
        <form action="category.html">
          <input type="text" class="search-bar" /><br />
          <input type="submit" class="button search-button" value="Search" />
        </form>
      </section>
      <section class="header-dropdown-and-cart">
        <button class="button">cart (0)</button>
        <button class="button">login</button>
        <the-header-dropdown></the-header-dropdown>
      </section> -->
    <section class="bookstore-logo-and-title">
      <router-link to="/">
        <img src="/site-images/logo.png" alt="Shelf Logo" />
      </router-link>
      <section class="text-logo">
        <h1>SHELF</h1>
        <p>The Book</p>
        <p>Haven</p>
      </section>
    </section>
    <section>
      <the-header-search-bar></the-header-search-bar>
    </section>

    <section class="header-buttons">
      <the-header-dropdown></the-header-dropdown>
      <div class="cart">
        <button class="header-dropdown-and-cart">
          <i class="fa-solid fa-cart-shopping"></i>
        </button>
        <p>Cart</p>
        <div class="cart-count">2</div>
      </div>
      <div class="login">
        <button class="header-dropdown-and-cart">
          <i class="fa-solid fa-user"></i>
        </button>
        <p>Vivek&nbsp<i class="fa-solid fa-square-caret-down"></i></p>
      </div>



    </section>
  </header>
</template>
