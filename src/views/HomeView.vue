<script setup>
const openModal = (type) => {
  window.$memberstackDom.openModal(type)
}
</script>

<template>
  <main class="home">
    <h1>Home Page</h1>
    <button data-ms-modal="signup" @click="openModal('SIGNUP')">Sign Up</button>
    <br>
    <button data-ms-modal="login" @click="openModal('LOGIN')">Log in</button>
    <br>
    <a href="" data-ms-modal="signup">Sign Up Link</a>
  </main>
</template>

<style scoped>
.home {
  width: 100%;
  height: 80vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>