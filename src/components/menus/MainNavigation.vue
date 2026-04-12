<script setup lang="ts">
import { Home, Lightbulb, Link, Menu, X } from 'lucide-vue-next'
import ThemeIcon from '../icons/misc/ThemeIcon.vue'
import { ref } from 'vue'

const isOpen = ref(false)

function closeMenu() {
  isOpen.value = false
}

function toggleTheme() {
  document.documentElement.classList.toggle('dark')
}
</script>

<template>
  <header class="border-b">
    <nav class="flex items-center justify-between px-6 py-4">
      <!-- LOGO -->
      <div class="py-2 flex items-center">
        <button @click="isOpen = !isOpen" class="lg:hidden cursor-pointer p-2">
          <Menu />
        </button>

        <RouterLink to="/" class="hidden lg:block font-bold px-4 rounded-2xl">
          Sébastien Cavaglia
        </RouterLink>
      </div>

      <!-- DESKTOP MENU -->
      <div class="gap-12 -ml-36 hidden lg:flex">
        <RouterLink to="/" class="flex items-center gap-2 hover:text-primary">
          <Home class="size-5" />
          Home
        </RouterLink>

        <RouterLink to="/projects" class="flex items-center gap-2 hover:text-primary">
          <Lightbulb class="size-5" />
          Projects
        </RouterLink>

        <RouterLink to="/contact" class="flex items-center gap-2 hover:text-primary">
          <Link class="size-5" />
          Contact
        </RouterLink>
      </div>

      <!-- THEME BUTTON -->
      <div @click="toggleTheme" class="cursor-pointer p-2">
        <ThemeIcon class="size-6 lg:size-5" />
      </div>
    </nav>
  </header>

  <!-- OVERLAY -->
  <div v-if="isOpen" @click="closeMenu" class="fixed inset-0 bg-black/50 z-40 lg:hidden" />

  <!-- SIDEBAR -->
  <aside
    class="fixed top-0 left-0 h-full w-64 bg-white dark:bg-neutral-900 shadow transform transition-transform duration-300 z-50 lg:hidden"
    :class="isOpen ? 'translate-x-0' : '-translate-x-full'"
  >
    <!-- Header sidebar -->
    <div class="flex items-center justify-between p-4 border-b">
      <span class="font-bold">Menu</span>
      <button @click="closeMenu" class="hover:text-primary cursor-pointer hover:bg-secondary transition rounded" >
        <X />
      </button>
    </div>

    <!-- Links -->
    <nav class="flex flex-col p-4 gap-2">
      <RouterLink
        @click="closeMenu"
        to="/"
        class="flex items-center gap-2 hover:text-primary hover:bg-secondary transition p-2 rounded-2xl"
      >
        <Home class="size-5" />
        Home
      </RouterLink>

      <RouterLink
        @click="closeMenu"
        to="/projects"
        class="flex items-center gap-2 hover:text-primary hover:bg-secondary transition p-2 rounded-2xl"
      >
        <Lightbulb class="size-5" />
        Projects
      </RouterLink>

      <RouterLink
        @click="closeMenu"
        to="/contact"
        class="flex items-center gap-2 hover:text-primary hover:bg-secondary transition p-2 rounded-2xl"
      >
        <Link class="size-5" />
        Contact
      </RouterLink>
    </nav>
  </aside>
</template>
