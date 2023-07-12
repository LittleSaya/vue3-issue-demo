<template>
  <span>nothing here</span>
</template>

<script setup lang="ts">
import { watch } from 'vue';

const props = defineProps<{
  a: number[];
  b: number[];
  c: number;
}>();

watch(
  () => props.c,
  () => {
    alert('dbg watch c');
  },
);

watch(
  () => props.b,
  () => {
    alert('dbg watch b');
  },
);

watch(
  () => props.a,
  () => {
    alert('dbg watch a');
  },
);
</script>
