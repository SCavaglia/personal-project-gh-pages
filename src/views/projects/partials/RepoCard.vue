<script setup lang="ts">
import LinkExternal from '@/components/hover/LinkExternal.vue';
import { Card, CardContent, CardHeader, CardTitle } from '@/components/ui/card';
// import ExternalHoverLink from '@/custom/misc/ExternalHoverLink.vue';
type Props = {
    link: string;
};

defineProps<Props>();
</script>
<template>
    <Card class="w-full">
        <CardHeader>
            <CardTitle>Github repository</CardTitle>
        </CardHeader>
        <CardContent class="-mt-4">
            <LinkExternal :href="'https://' + link">{{ link }}</LinkExternal>
        </CardContent>
    </Card>
</template>
