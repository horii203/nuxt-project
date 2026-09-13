<script setup>
const fruits = ["りんご", "みかん", "バナナ"];
</script>

<template>
  <div>
    <ul>
      <li v-for="fruit in fruits" :key="fruit">{{ fruit }}</li>
    </ul>
  </div>
</template>
