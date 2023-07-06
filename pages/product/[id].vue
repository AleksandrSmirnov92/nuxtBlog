<template>
  <p>{{ product.title }}</p>
  <p>{{ product.title }}</p>
  <p>{{ product.title }}</p>
</template>
<script setup>
const { id } = useRoute().params;
const { data: product } = useFetch(`https://fakestoreapi.com/products/${id}`);
console.log(product);
</script>
