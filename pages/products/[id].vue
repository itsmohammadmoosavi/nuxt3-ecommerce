<template>
  <div>
    <p>Product Details for {{ id }}</p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate hic
      facere veritatis tempora recusandae, aperiam excepturi dolores non itaque
      repudiandae natus autem neque cupiditate quas laboriosam iste similique
      et. Quidem.
    </p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>
