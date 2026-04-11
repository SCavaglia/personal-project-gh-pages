<script setup lang="ts">
import H1 from '@/components/typography/H1.vue';
import HomeBio from './partials/HomeBio.vue';
import { Camera } from '@lucide/vue';
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'

</script>

<template>
  <H1 title="Sébastien Cavaglia" subtitle="Web Developer" />
  <HomeBio />
  <hr class="m-auto mt-12 w-1/2" />
  


  <Card>
    <CardHeader>
      <CardTitle>Card Title</CardTitle>
      <CardDescription>Card Description</CardDescription>
    </CardHeader>
    <CardContent>
      <p>Card Content</p>
    </CardContent>
    <CardFooter>
      <p>Card Footer</p>
    </CardFooter>
  </Card>
  <p>dfgdfg</p>
  <p>TEST LIEN</p>
    <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/projects">Projects</RouterLink>
      </nav>
</template>

