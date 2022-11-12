<script setup lang="ts">
import { handleBackground } from '../layoutHelper'
const props = defineProps({
  imageLeft: {
    type: String,
  },
  imageTopRight: {
    type: String,
  },
  imageBottomRight: {
    type: String,
  },
})
</script>

<template>
  <div class="grid grid-cols-2 w-full h-full py-18 pr-13 pl-28">
    <div class="mr-4" :style="handleBackground(props.imageLeft)"></div>
    <div class="grid grid-row-2 gap-y-4">
      <div  :style="handleBackground(imageTopRight)"></div>
      <div  :style="handleBackground(imageBottomRight)"></div>
    </div>
  </div>
</template>
