<template>
  <div><h1>ID</h1></div>
  <p>{{ id }}</p>
</template>
<script setup>
const { id } = useRoute().params;
</script>
