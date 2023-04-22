<template>
  <div>
    <div
      class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8"
    >
      <div v-for="item in products" :key="item.id" class="group relative">
        <ProductCard :item="item" />
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});
//Fetch the Products
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped></style>
