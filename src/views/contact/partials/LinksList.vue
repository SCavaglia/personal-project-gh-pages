<script setup lang="ts">
import DockerIcon from '@/components/icons/contact/DockerIcon.vue'
import { Github, Mail } from 'lucide-vue-next'
</script>

<template>
  <ol class="ml-16">
    <li
      class="rounded-tr-xl rounded-br-xl border-l-3 border-border transition hover:border-primary hover:bg-muted dark:hover:bg-background-hover"
    >
      <a
        href="mailto:contact@sebastiencavaglia.com"
        class="group flex cursor-pointer items-center gap-4 py-2 pl-6"
      >
        <Mail />
        <div class="flex flex-col gap-1 lg:flex-row">
          <span>Email :</span>
          <span class="relative inline-block">
            contact@sebastiencavaglia.com
            <span
              class="absolute -bottom-1 left-0 h-px w-0 bg-current transition-all duration-300 group-hover:w-full"
            ></span>
          </span>
        </div>
      </a>
    </li>

    <li
      class="rounded-tr-xl rounded-br-xl border-l-3 border-border transition hover:border-primary hover:bg-muted dark:hover:bg-background-hover"
    >
      <a
        href="https://github.com/SCavaglia"
        target="_blank"
        rel="noopener noreferrer"
        class="group flex cursor-pointer items-center gap-4 py-2 pl-6"
      >
        <Github />
        <div class="flex flex-col gap-1 lg:flex-row">
          <span>GitHub :</span>
          <span class="relative inline-block">
            github.com/SCavaglia
            <span
              class="absolute -bottom-1 left-0 h-px w-0 bg-current transition-all duration-300 group-hover:w-full"
            ></span>
          </span>
        </div>
      </a>
    </li>

    <li
      class="rounded-tr-xl rounded-br-xl border-l-3 border-border transition hover:border-primary hover:bg-muted dark:hover:bg-background-hover"
    >
      <a
        href="https://hub.docker.com/u/scavaglia"
        target="_blank"
        rel="noopener noreferrer"
        class="group flex cursor-pointer items-center gap-4 py-2 pr-8 pl-6"
      >
        <DockerIcon />
        <div class="flex flex-col gap-1 lg:flex-row">
          <span>DockerHub :</span>
          <span class="relative inline-block">
            hub.docker.com/u/scavaglia
            <span
              class="absolute -bottom-1 left-0 h-px w-0 bg-current transition-all duration-300 group-hover:w-full"
            ></span>
          </span>
        </div>
      </a>
    </li>
  </ol>
</template>
