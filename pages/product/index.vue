<template>
  <div>
    <h1 class="text-gray-500 text-2xl font-bold mb-4">Product</h1>
    <div>
      <div class="w-full bg-gray-300">
        <div class="grid grid-cols-4 gap-5">
          <div v-for="product of products">
            <NuxtLink
              class="container hover:bg-gray-700 hover:text-green-500"
              :to="`product/${product.id}`"
              >{{ product.title }}</NuxtLink
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
let { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>
