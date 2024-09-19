<template>
  <div id="app">
    <h1>B7</h1>
    <header class="header">Header</header>
    <div class="content">
      <nav class="menu">Menu</nav>
      <main class="main">Main</main>
    </div>
    <footer class="footer">Footer</footer>
  </div>
</template>

<script setup>
// Không cần import các component con vì chúng đã được kết hợp trong file này
// Không cần định nghĩa components vì <script setup> tự động đăng ký các component được import

// Nếu bạn cần thêm logic, bạn có thể thêm ở đây
// Ví dụ:
// import { ref } from 'vue'
// const someData = ref('Example')
</script>

<style scoped>
body,
html {
  margin: 0;
  padding: 0;
  height: 100%;
  font-family: Arial, sans-serif;
}

#app {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.header {
  background-color: #f0f0f0;
  padding: 10px;
  text-align: center;
  
}

.content {
  display: flex;
  height: 100%;
  align-items: center;
}

.menu {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #1a4a9f;
  color: white;
  width: 200px;
  padding: 20px;
  height: 100%;
}

.main {
  display: flex;
  justify-content: center;
  align-items: center;
  flex: 1;
  padding: 20px;
}

.footer {
  background-color: #e0e0e0;
  padding: 10px;
  text-align: center;
}
</style>
