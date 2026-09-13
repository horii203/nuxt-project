<script setup>
defineProps({
  text: String,
});
const emit = defineEmits(["click"]);
</script>

<template>
  <button @click="emit('click')">{{ text }}</button>
</template>
