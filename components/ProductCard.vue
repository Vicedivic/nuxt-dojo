<template>
  <div class="card text-center">
    <img :src="product.image" :alt="product.title" class="thumb">
    <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
    <NuxtLink :to="`/products/${product.id}`">
      <span class="btn my-4">View Details</span>
    </NuxtLink>
  </div>
</template>

<script setup>
const { product } = defineProps({
  product: Object,
});
</script>

<style scoped>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>