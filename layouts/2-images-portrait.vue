<script setup lang="ts">
import { handleBackground } from "../layoutHelper"
const props = defineProps({
	imageTop: {
		type: String,
	},
	imageBottom: {
		type: String,
	},
	caption1: {
		type: String,
	},
	caption2: {
		type: String,
	},
})
</script>

<template>
	<div class="grid grid-cols-[.8fr_3.2fr] w-full h-full py-18 pr-13 pl-28 overflow-hidden">
		<div class="caption relative">
			<div class="absolute right-0">
				<p>{{ props.caption1 }}</p>
				<p>{{ props.caption2 }}</p>
			</div>
		</div>
		<div class="grid grid-cols-2 gap-x-4">
			<div class="bg-green" :style="handleBackground(props.imageTop)"></div>
			<div class="bg-red" :style="handleBackground(props.imageBottom)"></div>
		</div>
	</div>
</template>

<style lang="scss">
.caption {
	p {
		@apply: text-left mr-5 max-w-150px text-xs pt-.5 mb-3;
		border-top: 0.3px solid black;
	}
}
</style>
