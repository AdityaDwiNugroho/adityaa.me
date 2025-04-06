<script setup lang="ts">
import { useWindowScroll } from '@vueuse/core'

function scrollToTop() {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}

const { y: scroll } = useWindowScroll()
</script>

<template>
  <header class="header z-40">
    <RouterLink
      class="w-12 h-12 absolute xl:fixed m-5 select-none outline-none"
      to="/"
      focusable="false"
      >Logo</RouterLink
    >

    <button
      title="Scroll to top"
      fixed
      right-3
      bottom-3
      w-10
      h-10
      hover:op100
      rounded-full
      hover-bg-hex-8883
      transition
      duration-300
      z-100
      print:hidden
      :class="scroll > 300 ? 'op30' : 'op0! pointer-events-none'"
      @click="scrollToTop()"
    >
      <h1>Scroll Up</h1>
    </button>
  </header>
</template>
