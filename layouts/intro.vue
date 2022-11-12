<template>
	<div class="slidev-layout w-full h-full intro-image" :style="style">
		<div class="absolute top-18 left-28">
			<h3>{{ header }}</h3>
		</div>
		<div class="absolute left-28 bottom-18">
			<h1>{{ projectTitle }}</h1>
			<h2>{{ subtitle }}</h2>
		</div>
	</div>
</template>

<script setup>
import { computed } from "vue"
import { handleBackground } from "../layoutHelper"
const props = defineProps({
	projectTitle: {
		type: String,
	},
	subtitle: {
		type: String,
	},
	header: {
		type: String,
	},
	image: {
		type: String,
	},
})
const style = computed(() => handleBackground(props.image))
</script>
