<script setup>
import { ref } from "vue";

const items = [
    { 
        id: 1, 
        task: "have a shower", 
    },
    { 
        id: 2, 
        task: "buy fruits", 
    },
    { 
        id: 3, 
        task: "walk with a dog", 
    },
];
</script>
<template>
  <div class="todo-item" v-for="item in items" :key="item.id">
    <span class="todo-item__name">{{ item.task }}</span>
    <div class="todo-item__functions">
        <span class="todo-item__function --edit">редактировать</span>
        <span class="todo-item__function --delete">удалить</span>
        <span class="todo-item__function --done">готово</span>
    </div>
  </div>
</template>
