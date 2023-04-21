<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="item in products">
        <NuxtLink :to="`/products/${p.id}`">{{ item.title }}</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
//Fetch the Products
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped></style>
