<template>
  <div class="mt-7 max-w-sm mx-auto text-center card">
    <h1 class="mt-7 text-7xl font-bold">{{ error.statusCode }}</h1>
    <h2 class="mt-7 text-6xl">Ooops.</h2>
    <p class="mt-7">{{ error.message }}</p>
    <button class="btn my-7" @click="handleClearError">Go Home…</button>
  </div>
</template>

<script setup>
const { error } = defineProps({
  error: Error,
});

const handleClearError = () => {
  clearError({ redirect: '/' });
};
</script>