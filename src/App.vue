<script setup>
import memberstackDOM from "@memberstack/dom";
import { onMounted } from "vue";
import Header from './components/Header.vue'
import { RouterLink, RouterView } from 'vue-router'

onMounted(() => {
  memberstackDOM.init({
  publicKey: "pk_sb_8b5354f1cd14606d03e7",
});
})
</script>

<template>
  <Header>
     <RouterLink to="/" class="link">Home</RouterLink>
     <RouterLink to="/about" class="link">About</RouterLink>
     <RouterLink to="/secret" class="link">Secret</RouterLink>
  </Header>
  <RouterView />
</template>

<style scoped>
  .link {
    margin-right: 20px;
  }
</style>