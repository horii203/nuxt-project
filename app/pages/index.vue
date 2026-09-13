<script setup lang="ts">
const { data } = await useFetch("/api/hello");
</script>

<template>
  <div>
    <h1>トップページ</h1>

    <p>{{ data?.message }}</p>
    <p>{{ data?.name }}</p>
  </div>
</template>
