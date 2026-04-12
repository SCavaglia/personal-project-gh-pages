<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppLayout from './components/layouts/AppLayout.vue'

const isDark = window.matchMedia('(prefers-color-scheme: dark)').matches

if (isDark) {
  document.documentElement.classList.add('dark')
}
</script>

<template>
  <AppLayout>
    <RouterView />
  </AppLayout>
</template>
