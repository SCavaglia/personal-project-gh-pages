<script setup lang="ts">
type Props = {
    title: string;
    subtitle?: string;
};

defineProps<Props>();
</script>
<template>
    <div class="my-16 space-y-4 text-center text-balance">
        <h1 class="text-4xl font-bold tracking-tight">
            {{ title }}
        </h1>
        <p v-if="subtitle" class="text-xl text-muted-foreground">
            {{ subtitle }}
        </p>
    </div>
</template>
