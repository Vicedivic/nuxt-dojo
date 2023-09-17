<template>
  <Head>
    <Title>Nuxt Dojo | Merch</Title>
    <Meta name="description" content="Nuxt 3 Merch" />
  </Head>

  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="product in productList">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products',
});

const { data: productList } = await useFetch('https://fakestoreapi.com/products');
</script>