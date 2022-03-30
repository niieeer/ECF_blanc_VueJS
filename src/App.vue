<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
      <nav class="wrapper">
        <RouterLink to="/">Calculateur d’IMC</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
  </header>

  <RouterView />
</template>

<style>
.wrapper {
  display: flex;
  gap: 20px;
}
</style>
