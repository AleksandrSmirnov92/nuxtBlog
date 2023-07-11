<template>
  <div class="card text-center">
    <img :src="product.image" alt="" class="thumb" />
    <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
    <NuxtLink :to="`/product/${product.id}`">
      <button class="my-4">Просмотр</button>
    </NuxtLink>
  </div>
</template>
<script setup>
const { product } = defineProps(["product"]);
</script>
<style scoped>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>
