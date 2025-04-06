<script setup lang="ts">
import { RouterLink, RouterView, useRoute } from 'vue-router'
import NavBar from './components/NavBar.vue'

const route = useRoute()
</script>

<template>
  <NavBar />
  <main class="px-7 py-10 overflow-x-hidden">
    <RouteView />
  </main>
</template>
