<script setup lang="ts">
import H1 from '@/components/typography/H1.vue'
import RepoCard from './RepoCard.vue'
import ProjectCard from './ProjectCard.vue'
import { ChartLine } from 'lucide-vue-next'
</script>

<template>
  <H1 title="Projects" />

  <div class="flex flex-col items-center gap-6 lg:flex-row mx-auto justify-center">
    <div class="w-md">
      <RepoCard link="github.com/SCavaglia" />
      <ProjectCard
        link="/stocks"
        headerTitle="Stock App"
        headerDescription="Monitor your stock portfolio"
      >
        <template #headerIcon> <ChartLine /> </template>
        <p>stock graph</p>
      </ProjectCard>
    </div>
    <div class="w-md">
      <RepoCard link="github.com/SCavaglia" />
      <ProjectCard
        link="/stocks"
        headerTitle="Weather App"
        headerDescription="Monitor your weather conditions"
      >
        <template #headerIcon> <ChartLine /> </template>
        <p>weather forecast</p>
      </ProjectCard>
    </div>
  </div>
</template>
