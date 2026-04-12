<script setup lang="ts">
import { useRouter } from 'vue-router'
import { TriangleAlert } from 'lucide-vue-next';
import { Card, CardContent, CardDescription, CardFooter, CardHeader, CardTitle } from '@/components/ui/card';


const router = useRouter()


type Props = {
    link: string;
    headerTitle: string;
    headerDescription?: string;
    footerTitle?: string;
    footerDescription?: string;
};

defineProps<Props>();
</script>

<template>
    <Card
        @click="router.push(link)"
        class="h-128 w-full transform transition-transform hover:scale-105 hover:bg-muted dark:hover:bg-card-hover cursor-pointer"
    >
        <div class="ml-4 flex gap-2 font-bold text-amber-500 dark:text-amber-200">
            <TriangleAlert class="-mt-1" />
            Demo with fake data
        </div>
        <hr />
        <CardHeader class="flex flex-col items-center gap-2">
            <CardTitle class="flex items-center gap-2">
                <slot name="headerIcon"></slot>
                {{ headerTitle }}
            </CardTitle>
            <CardDescription>{{ headerDescription }}</CardDescription>
        </CardHeader>

        <CardContent class="flex min-h-64 items-center justify-center">
            <slot />
        </CardContent>

        <CardFooter class="flex-col items-start gap-2 text-sm">
            <div class="flex items-center gap-2 leading-none font-medium">
                {{ footerTitle }}
                <slot name="footerIcon"></slot>
            </div>
            <div class="leading-none text-muted-foreground">{{ footerDescription }}</div>
        </CardFooter>
    </Card>
</template>
