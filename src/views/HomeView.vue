<script setup>
const openModal = (type) => {
  window.$memberstackDom.openModal(type)
}
</script>

<template>
  <main class="home">
    <h1>Home Page</h1>
    <span>Those buttons below invoke pre build ms modal without using ms attributes. But they have to use js methods</span>
    <button @click="openModal('SIGNUP')">Sign Up</button>
    <br>
    <button @click="openModal('LOGIN')">Log in</button>
    <br>
    <span>This is a link that invokes pre build ms modals using ms attributes: <a data-ms-modal="signup" class="m-link">Sign Up Link</a></span>
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
.m-link {
  color: blue;
  cursor: pointer;
}
</style>