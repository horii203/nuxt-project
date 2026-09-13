<script setup>
const handleClick = () => {
  alert("ボタンがクリックされました");
};
</script>

<template>
  <div>
    <h1>index</h1>
    <MyButton text="クリックしてください" @click="handleClick" />
    <br />
    <NuxtLink to="/about"> Aboutページへ </NuxtLink>
  </div>
</template>
