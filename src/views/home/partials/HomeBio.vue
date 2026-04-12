<script setup lang="ts">
import LinkReveal from '@/components/hover/LinkReveal.vue'
import InertiaIcon from '@/components/icons/bio/InertiaIcon.vue'
import LaravelIcon from '@/components/icons/bio/LaravelIcon.vue'
import NextIcon from '@/components/icons/bio/NextIcon.vue'
import ReactIcon from '@/components/icons/bio/ReactIcon.vue'
import TailwindIcon from '@/components/icons/bio/TailwindIcon.vue'
import VueIcon from '@/components/icons/bio/VueIcon.vue'
</script>

<template>
  <div>
    <p class="py-2">
      Hi, I'm a junior full-stack web developer focused on building modern, performant, and
      user-friendly applications.
    </p>
    <p class="py-2">
      With a strong attention to detail and clean code practices, I aim to create reliable digital
      experiences that are both efficient and scalable.
    </p>
    <p class="py-2">
      Always curious and continuously learning, I stay up to date with the latest technologies to
      deliver high-quality work.
    </p>
    <p class="pt-8 pb-6">My favourite stack is VILT</p>
    <div class="flex flex-col gap-10 lg:flex-row lg:gap-4 justify-center items-center">
      <div class="flex gap-4">
        <LinkReveal link="vuejs.org" class="transition hover:text-vue">
          <div class="flex gap-4 transition group-hover:drop-shadow-[0_0_8px_var(--vue)]">
            Vue <VueIcon class="size-6" />
          </div>
        </LinkReveal>
        <LinkReveal link="inertiajs.com" class="transition hover:text-inertia">
          <div class="flex gap-4 transition group-hover:drop-shadow-[0_0_8px_var(--inertia)]">
            Inertia <InertiaIcon class="size-6" />
          </div>
        </LinkReveal>
      </div>

      <div class="flex gap-4">
        <LinkReveal link="laravel.com" class="transition hover:text-laravel">
          <div class="flex gap-4 transition group-hover:drop-shadow-[0_0_8px_var(--laravel)]">
            Laravel <LaravelIcon class="size-6" />
          </div>
        </LinkReveal>
        <LinkReveal link="tailwindcss.com" class="transition hover:text-tailwind">
          <div class="flex gap-4 transition group-hover:drop-shadow-[0_0_8px_var(--tailwind)]">
            Tailwind <TailwindIcon class="size-6" />
          </div>
        </LinkReveal>
      </div>
    </div>

    <p class="pt-16 pb-6">But I can also work with React and NextJS</p>
    <div class="flex gap-4 justify-center items-center">
      <LinkReveal link="react.dev" class="transition-all hover:text-react">
        <div class="flex gap-4 transition group-hover:drop-shadow-[0_0_8px_var(--react)]">
          React <ReactIcon class="size-6" />
        </div>
      </LinkReveal>
      <div>
        <LinkReveal link="nextjs.org">
          <div
            class="flex gap-4 transition group-hover:drop-shadow-[0_0_8px_rgba(0,0,0,0.8)] dark:group-hover:drop-shadow-[0_0_8px_rgba(255,255,255,0.8)]"
          >
            Next <NextIcon class="size-6" />
          </div>
        </LinkReveal>
      </div>
    </div>
  </div>
</template>
