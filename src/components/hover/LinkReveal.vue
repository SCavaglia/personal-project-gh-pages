<script setup lang="ts">
import { ExternalLink } from '@lucide/vue';

type Props = {
    link: string;
};

defineProps<Props>();
</script>
<template>
    <div
        class="group relative inline-block w-fit cursor-pointer rounded-2xl border px-4 pt-2 text-center hover:rounded-b-none"
    >
        <!-- 👻 Élément fantôme (définit la largeur) -->
        <div class="pointer-events-none absolute opacity-0">
            <div class="flex items-center gap-2 p-4 text-xs whitespace-nowrap">
                {{ link }}
            </div>
        </div>

        <!-- Contenu réel -->
        <div>
            <!-- Bloc principal -->
            <div class="flex gap-4 px-4 py-2 font-bold">
                <slot />
            </div>

            <!-- Bloc caché -->
            <a
                :href="'https://' + link"
                target="_blank"
                rel="noopener noreferrer"
                class="absolute top-full left-0 block max-h-0 w-full overflow-hidden rounded-b-2xl border-t bg-muted opacity-0 shadow-lg transition-all duration-500 ease-out group-hover:max-h-20 group-hover:opacity-100"
            >
                <div
                    class="flex items-center justify-center gap-2 p-4 text-xs whitespace-nowrap text-black dark:text-muted-foreground border"
                >
                    {{ link }}

                    <ExternalLink class="size-3 shrink-0" />
                </div>
            </a>
        </div>
    </div>
</template>
