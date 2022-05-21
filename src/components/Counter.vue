<script setup lang="ts">
const props = defineProps<{
  initial: number
}>();

const { count, inc, dec } = useCounter(props.initial);
</script>

<template>
  <div>
    {{ count }}
    <button inc @click="inc()">
      +
    </button>
    <button dec @click="dec()">
      -
    </button>
  </div>
</template>
