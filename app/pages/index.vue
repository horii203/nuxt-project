<script setup>
import { ref } from "vue";
const count = ref(0);
const increment = () => {
  count.value++;
};
</script>

<template>
  <div>
    <p>カウント：{{ count }}</p>
    <button @click="increment">Increment</button>
    <p v-if="count >= 5">5以上になりました！</p>
    <p v-else>5未満です</p>
  </div>
</template>
