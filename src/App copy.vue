<script setup>
import { computed, reactive, watch } from "vue";

ref: count = 0;
ref: doubled = computed(() => count * 2);

const inc = () => count++;
const dec = () => count--;

const r = reactive({ count: 0 });
watch(() => {
  r.count = count;
  r.doubled = 2 * count;
});

console.log(new Date().toLocaleString());
// await new Promise((r) => setTimeout(r, 1000));
console.log(new Date().toLocaleString());
</script>

<template>
  <div>{{ count }} * 2 = {{ doubled }}</div>
  <div>{{ r.count }} * 2 = {{ r.doubled }}</div>
  <button @click="dec">Dec</button>
  <button @click="inc">Inc</button>
</template>
