<template>
  <header class="header">
    <slot></slot>
  </header>
</template>

<script setup>

</script>

<style scoped>
  .header {
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-bottom: 1px solid grey;
  }
</style>