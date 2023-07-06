<template>
  <div>
    <header>
      <div class="container mx-auto flex justify-between p-4 bg-gray-200">
        <h1 class="font-bold text-2xl">Title</h1>
        <nav>
          <ul class="flex gap-4">
            <li class="hover:text-gray-500 hover:underline">
              <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li class="hover:text-gray-500 hover:underline">
              <NuxtLink to="/about">About</NuxtLink>
            </li>
            <li class="hover:text-gray-500 hover:underline">
              <NuxtLink to="/product">Product</NuxtLink>
            </li>
          </ul>
        </nav>
      </div>
    </header>
    <div class="container mx-auto p-4"><slot /></div>
  </div>
</template>
<style scoped>
.router-link-exact-active {
  @apply text-green-500;
}
</style>
