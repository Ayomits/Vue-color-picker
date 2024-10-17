<template>
    <input type="color" @input="colorPicker" />
</template>

<script lang="ts" setup>
const emit = defineEmits(["colorPicker"]);

function colorPicker(event: any) {
    emit("colorPicker", event);
}
</script>

<style></style>
