<template>
  <div>
    <div
      class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8"
    >
      <div v-for="item in products" :key="item.id" class="group relative">
        <NuxtLink :to="`/products/${item.id}`">
          <div
            class="min-h-80 aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-80"
          >
            <img
              :src="item.image"
              :alt="item.title"
              class="h-full w-full object-cover object-center lg:h-full lg:w-full"
            />
          </div>
          <div class="mt-4 flex justify-between">
            <div>
              <h3 class="text-sm text-gray-700">
                <span aria-hidden="true" class="absolute inset-0" />
                {{ item.title }}
              </h3>
              <p class="mt-1 text-sm text-gray-500">{{ item.category }}</p>
            </div>
            <p class="text-sm font-medium text-gray-900">${{ item.price }}</p>
          </div>
        </NuxtLink>
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
