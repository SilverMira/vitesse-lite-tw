<script setup lang="ts">
const props = defineProps<{ name: string }>();
const router = useRouter();
</script>

<template>
  <div>
    <i-carbon-pedestrian class="inline-block text-4xl" />
    <p>Hi, {{ props.name }}</p>
    <p class="text-sm opacity-50">
      <em>Dynamic route!</em>
    </p>

    <div>
      <button class="inline-block py-1 px-4 m-3 mt-8 text-sm text-white bg-teal-600 hover:bg-teal-700 disabled:bg-gray-600 rounded disabled:opacity-50 cursor-pointer disabled:cursor-default" @click="router.back()">
        Back
      </button>
    </div>
  </div>
</template>
