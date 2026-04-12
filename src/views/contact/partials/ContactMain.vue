<script setup lang="ts">
import H1 from '@/components/typography/H1.vue';
import DisponibilityParagraph from './DisponibilityParagraph.vue';
import LinksList from './LinksList.vue';

</script>

<template>
    <H1 title="Contact" />
            <div class="flex flex-col items-center justify-center gap-18">
            <div class="space-y-8">
                <DisponibilityParagraph/>
                <LinksList/>
            </div>
        </div>
</template>