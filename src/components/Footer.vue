<script setup lang="ts">
import { isDark, toggleDark } from '~/composables';
</script>

<template>
  <nav class="inline-flex gap-2 mt-6 text-xl">
    <button class="inline-block text-[0.9em] hover:text-teal-600 !outline-none opacity-75 hover:opacity-100 transition duration-200 ease-in-out cursor-pointer select-none" @click="toggleDark()">
      <i-carbon-moon v-if="isDark" />
      <i-carbon-sun v-else />
    </button>

    <a
      class="inline-block text-[0.9em] hover:text-teal-600 opacity-75 hover:opacity-100 transition duration-200 ease-in-out cursor-pointer select-none"
      rel="noreferrer" href="https://github.com/antfu/vitesse-lite" target="_blank" title="GitHub"
    >
      <i-carbon-logo-github />
    </a>
  </nav>
</template>
