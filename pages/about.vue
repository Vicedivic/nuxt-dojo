<template>
  <h1>About</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laboriosam perspiciatis quasi tempore? Deserunt hic natus
    quas rem! Dolorum, natus, quaerat.</p>
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laboriosam perspiciatis quasi tempore? Deserunt hic natus
    quas rem! Dolorum, natus, quaerat.</p>
  <div>{{ data }}</div>
</template>

<script setup>
const { data } = await useFetch('/api/ninja?name=mario', {
  method: 'post',
  body: { age: 30 },
});
</script>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}

p {
  margin: 20px 0;
}
</style>