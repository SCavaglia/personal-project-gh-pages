<script setup lang="ts">
defineProps<{
  href: string
}>()
</script>

<template>
<RouterLink
    :to="href"
    class="group flex items-center gap-4 rounded-tr-xl rounded-br-xl border-l-3 border-border py-2 pr-8 pl-6 transition hover:border-primary hover:bg-background-hover"
>
    <span class="relative inline-block">
        <slot />
        <span
            class="absolute -bottom-1 left-0 h-px w-0 bg-current transition-all duration-300 group-hover:w-full"
        ></span>
    </span>
</RouterLink>
</template>
