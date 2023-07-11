<template>
  <div>
    <h1 class="text-gray-500 text-2xl font-bold mb-4">Product</h1>
    <div>
      <div class="w-full bg-gray-300">
        <div class="grid grid-cols-4 gap-5">
          <div v-for="product in products">
            <ProductCard :product="product" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>
