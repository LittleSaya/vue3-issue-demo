<template>
  <Comp :a="[1, 2]" :b="b" :c="-1" />
  <button @click="fn">fn</button>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import Comp from './Comp.vue';

const b = ref<number[]>([]);

function fn() {
  b.value = [3, 4];
}
</script>
