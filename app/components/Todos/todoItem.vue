<script setup>
const props = defineProps({
    task: {
        type: Object,
    }
});

const buttonsConfig = [
    {
        label: "Edit",
        action: "Edit",
    },
    {
        label: "Delete",
        action: "Delete",
    },
    {
        label: "Done",
        action: "Done"
    }
]

</script>
<template>
  <div class="todo-item">
    <span class="todo-item__name">{{ task.title }}</span>
    <div class="todo-item__functions">
        <UIButton v-for="button in buttonsConfig" :key="button.action" :label="button.label"></UIButton>
    </div>
  </div>
</template>
