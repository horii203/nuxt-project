<script setup>
import { ref } from "vue";

const fruit = ref("");

const fruits = ref(["りんご", "みかん"]);

const addFruit = () => {
  fruits.value.push(fruit.value);
  fruit.value = "";
};

const deleteFruit = (index) => {
  // splice は配列から要素を削除する
  fruits.value.splice(index, 1);
};
</script>

<template>
  <div>
    <h1>フルーツ一覧</h1>

    <input v-model="fruit" type="text" placeholder="フルーツを入力" />

    <button @click="addFruit">追加</button>

    <ul>
      <li v-for="(item, index) in fruits" :key="item">
        {{ item }}
        <button @click="deleteFruit(index)">削除</button>
      </li>
    </ul>
  </div>
</template>
