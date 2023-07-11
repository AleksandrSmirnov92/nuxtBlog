<template>
  <div class="mt-7 mx-auto text-center card">
    <p class="mt-7 font-bold">{{ error.statusCode }}</p>
    <p class="mt-7">Произошла ошибка</p>
    <p class="mt-7">{{ error.message }}</p>
    <button
      @click="goHome"
      class="btn my-7 bg-green-500 px-2 rounded hover:bg-green-600"
    >
      Домой...
    </button>
  </div>
</template>

<script setup>
const goHome = () => {
  clearError({ redirect: "/" });
};
defineProps(["error"]);
</script>

<style scoped></style>
