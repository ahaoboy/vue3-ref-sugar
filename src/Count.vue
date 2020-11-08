<template>
  <div>count</div>
</template>

<script setup>
console.log(new Date().toLocaleString());
await new Promise((r) => setTimeout(r, 1000));
console.log(new Date().toLocaleString());
</script>

<style></style>
