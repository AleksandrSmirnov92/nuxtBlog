<template>
  <ProductDetails :product="product" />
</template>
<script setup>
const { id } = useRoute().params;
const { data: product } = await useFetch(
  `https://fakestoreapi.com/products/${id}`,
  {
    key: id,
  }
);

if (!product.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Страница не найдена",
    fatal: true,
  });
}
</script>
