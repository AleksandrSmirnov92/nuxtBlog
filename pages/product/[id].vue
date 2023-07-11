<template>
  <ProductDetails :product="product" />
</template>
<script setup>
const { id } = useRoute().params;
const { data: product } = useFetch(`https://fakestoreapi.com/products/${id}`, {
  key: id,
});
</script>
