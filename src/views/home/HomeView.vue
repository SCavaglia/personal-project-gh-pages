<script setup lang="ts">
import H1 from '@/components/typography/H1.vue'
import HomeBio from './partials/HomeBio.vue'
import { Camera } from '@lucide/vue'
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'
import ProjectsMain from '../projects/partials/ProjectsMain.vue';
import ContactMain from '../contact/partials/ContactMain.vue';
</script>

<template>
  <H1 title="Sébastien Cavaglia" subtitle="Web Developer" />
  <HomeBio class="w-3/5 mx-auto" />
  <hr class="m-auto mt-12 w-1/2" />
  <ProjectsMain />
  <hr class="m-auto mt-12 w-1/2" />
 <ContactMain /> 
</template>
