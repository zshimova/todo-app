<script setup>
const props = defineProps({
    tasks: { 
        type: Array,
    }
});
import TodoItem from './todoItem.vue';

</script>
<template>
    <TodoItem v-for="task in tasks" :key="task.id" :task="task"/>
</template>