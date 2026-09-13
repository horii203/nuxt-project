<script setup>
import { ref } from "vue";

const fruit = ref("");

const fruits = ref(["りんご", "みかん"]);

const addFruit = () => {
  fruits.value.push(fruit.value);
  fruit.value = "";
};
</script>

<template>
  <div>
    <h1>フルーツ一覧</h1>

    <input v-model="fruit" type="text" placeholder="フルーツを入力" />

    <button @click="addFruit">追加</button>

    <ul>
      <li v-for="item in fruits" :key="item">
        {{ item }}
      </li>
    </ul>
  </div>
</template>
