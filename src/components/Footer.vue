<script setup lang="ts">
  import { isDark, toggleDark } from '~/composables'
</script>

<template>
  <nav text-xl mt-6 inline-flex gap-4>
    <button class="icon-btn !outline-none" @click="toggleDark()">
      <div v-if="isDark" i-carbon-moon />
      <div v-else i-carbon-sun />
    </button>

    <a
      class="icon-btn"
      i-carbon-logo-github
      href="https://github.com/nberlette/gitpod-vitesse-lite"
      rel="noopener noreferrer"
      target="_blank"
      title="View on GitHub"
    />
    <a
      class="icon-btn scale-[0.8]"
      i-simple-icons-gitpod
      href="https://gitpod.io/#https://github.com/nberlette/gitpod-vitesse-lite"
      rel="noopener noreferrer"
      target="_blank"
      title="Open in Gitpod!"
    />
  </nav>
</template>
