<script setup lang="ts">
const name = $ref('');

const router = useRouter();
const go = () => {
  if (name)
    router.push(`/hi/${encodeURIComponent(name)}`);
};
</script>

<template>
  <div>
    <i-carbon-campsite class="inline-block text-4xl" />
    <p>
      <a rel="noreferrer" href="https://github.com/antfu/vitesse-lite" target="_blank">
        Vitesse Lite
      </a>
    </p>
    <p>
      <em class="text-sm opacity-75">Opinionated Vite Starter Template</em>
    </p>

    <div class="py-4" />

    <input
      id="input"
      v-model="name"
      placeholder="What's your name?"
      type="text"
      autocomplete="false"
      class="py-2 px-4 w-[250px] text-center bg-transparent rounded border border-gray-200 dark:border-gray-700 outline-none active:outline-none"
      @keydown.enter="go"
    >

    <div>
      <button
        class="inline-block py-1 px-4 m-3 text-sm text-white bg-teal-600 hover:bg-teal-700 disabled:bg-gray-600 rounded disabled:opacity-50 cursor-pointer disabled:cursor-default"
        :disabled="!name"
        @click="go"
      >
        Go
      </button>
    </div>
  </div>
</template>
