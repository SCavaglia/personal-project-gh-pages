<script setup lang="ts">
import MainNavigation from '../menus/MainNavigation.vue';
import Footer from '../landmarks/Footer.vue';

</script>

<template>
    <MainNavigation />
    <slot />
    <Footer />  
</template>