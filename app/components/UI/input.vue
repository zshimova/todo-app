<script setup>
    const props = defineProps({
        label: {
            type: String,
            default: "Add new task"
        },
        modelValue: {
            type: String,
            default: ""
        }
    });

    const emit = defineEmits(["update:modelValue"]);
</script>

<template>
    <input
        type="text"
        name="new-task"
        id="new-task"
        :placeholder="label"
        :value="modelValue"
        @input="emit('update:modelValue', $event.target.value)"
    />
</template>