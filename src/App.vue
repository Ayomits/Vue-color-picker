<script setup lang="ts">
import { ref } from "vue";
import ColorInput from "./components/ColorInput/index.vue";
import ColorPanel from "./components/ColorPanel/index.vue";

const color = ref<string>("");

const changeColor = (event: { target: { value: string } }) => {
    color.value = event.target.value;
};
</script>

<template>
    <div class="app">
        <ColorPanel :color="color.length >= 1 ? color : '#333'" />
        <p style="font-size: 30px">Select a color</p>
        <ColorInput @color-picker="changeColor" />
    </div>
</template>

<style>
.app {
    display: flex;
    justify-content: center;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: center;
    color: black;
    font-family: "Roboto", sans-serif;
    font-weight: 500;
    font-style: normal;
    text-align: center;
}
</style>
