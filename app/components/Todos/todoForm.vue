<script setup>
import { ref } from "vue";
import TodoList from "./todoList.vue";

const inputText = ref("Text new task")
const buttonText = ref("Add");
const newTaskTitle = ref("");
const addNewTask = () => {
  
  console.log(newTaskTitle.value)
};

const tasks = ref([
    { 
        id: 1, 
        title: "have a shower", 
    },
    { 
        id: 2, 
        title: "buy fruits", 
    },
    { 
        id: 3, 
        title: "walk with a dog", 
    },
]);


</script>
<template>
  <UIInput v-model="newTaskTitle" :label="inputText" />
  <UIButton :label="buttonText" @click="addNewTask"/>
  <TodoList :tasks="tasks"/>
</template>
  