<script setup lang="ts">
import { RouterView } from 'vue-router'

const isDark = window.matchMedia('(prefers-color-scheme: dark)').matches

if (isDark) {
  document.documentElement.classList.add('dark')
}
</script>

<template>
  <RouterView />
</template>


