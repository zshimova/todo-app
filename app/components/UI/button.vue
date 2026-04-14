<script setup>
   const props = defineProps({
        label: {
            type: String,
            default: "Button"
        },
    });
</script>
<template>
    <button class="button">{{ label }}</button>
</template>
