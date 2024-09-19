<template>
  <div class="app-container">
    <h1>B8</h1>
    <header>Header</header>
    <nav>Navigation</nav>
    <div class="content">
      <aside class="menu">Menu</aside>
      <main class="cart-grid">
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
        <div class="cart">Cart</div>
      </main>
      <aside class="article">Article</aside>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  setup() {
    // Component logic can be added here if needed
  },
});
</script>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  height: 100vh;
  font-family: Arial, sans-serif;
}

header,
nav {
  background-color: #f0f0f0;
  padding: 10px;
  text-align: center;
}

.content {
  display: flex;
  flex: 1;
}

.menu {
  background-color: #4caf50;
  color: white;
  width: 200px;
  padding: 20px;
}

.cart-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  padding: 20px;
  flex: 1;
  background-color: #fff0f0;
}

.cart {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  border: 1px solid #ddd;
  padding: 20px;
  text-align: center;
}

.article {
  background-color: #87ceeb;
  width: 200px;
  padding: 20px;
    display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 768px) {
  .content {
    flex-direction: column;
  }

  .menu,
  .article {
    width: 100%;
  
  }

  .cart-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
.menu{
      display: flex;
    justify-content: center;
    align-items: center;
}
</style>
