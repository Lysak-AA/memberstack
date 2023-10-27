<script setup>
import memberstackDOM from "@memberstack/dom";
import { onMounted } from "vue";
import Header from './components/Header.vue'
import { RouterLink, RouterView } from 'vue-router'

onMounted(() => {
  // first way to append script - this case let us use ms attributes
  const head = document.getElementsByTagName('head')[0]
  const script = window.document.createElement('script')
  script.setAttribute('data-memberstack-app', 'app_clo742yfn004u0szd1uff5flz')
  script.src = 'https://static.memberstack.com/scripts/v1/memberstack.js'
  script.type = 'text/javascript'
  head.appendChild(script)

  // second way - use js memberstack methods. pre build modals can be used only with js invocation methods
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