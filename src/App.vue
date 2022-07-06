<template>
  <SliderVertify :on-success="onSuccess"></SliderVertify>
</template>
<script setup lang="ts">
import SliderVertify from './SliderVertify/index.vue'
function onSuccess() {
  console.log('success')
}
</script>
