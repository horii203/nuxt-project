<script setup>
import { ref } from "vue";
const task = ref("");
const tasks = ref([
  {
    id: 1,
    title: "Nuxtを勉強する",
    completed: false,
  },
  {
    id: 2,
    title: "Vueを復習する",
    completed: true,
  },
]);

const addTask = () => {
  if (task.value === "") {
    return;
  }

  tasks.value.push({
    id: Date.now(),
    title: task.value,
    completed: false,
  });

  task.value = "";
};

const deteleTask = (index) => {
  tasks.value.splice(index, 1);
};
</script>

<template>
  <div>
    <h1>Todo List</h1>

    <input type="text" v-model="task" />
    <button @click="addTask">追加</button>

    <ul>
      <li v-for="(item, index) in tasks" :key="item.id">
        <label>
          <input type="checkbox" v-model="item.completed" />
          <span :class="{ completed: item.completed }">{{ item.title }}</span>
        </label>
        <button @click="deteleTask">削除</button>
      </li>
    </ul>
  </div>
</template>
<style scoped>
.completed {
  text-decoration: line-through;
}
</style>
