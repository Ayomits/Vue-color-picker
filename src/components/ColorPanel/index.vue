<template>
    <div class="color-panel" :style="{ backgroundColor: props.color }">
      <div class="color-panel-content">
        <p>Selected color: {{ color }}</p>
      </div>
    </div>
</template>

<script setup lang="ts">
interface ColorPanelProps {
    color: string;
}

const props = defineProps<ColorPanelProps>();
</script>

<style>
.color-panel {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 400px;
    height: 400px;
    border-radius: 20px;
    font-size: 30px;
}
.color-panel-content {
  color: white;
  font-weight: 700;
}
</style>
