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
	<div class="grid grid-cols-[2fr_.6fr_2fr] w-full h-full py-18 pr-13 pl-28 overflow-hidden">
		<div class="relative slidev-layout default">
			<div class="absolute bottom-0 left-0 pr-3">
				<slot />
			</div>
		</div>
		<div class="caption relative">
			<div class="absolute right-0">
				<p>{{ props.caption1 }}</p>
				<p>{{ props.caption2 }}</p>
			</div>
		</div>
		<div class="grid grid-row-2 gap-y-4">
			<div class="bg-green" :style="handleBackground(props.imageTop)"></div>
			<div class="bg-red" :style="handleBackground(props.imageBottom)"></div>
		</div>
	</div>
</template>

<style lang="scss">
.caption {
	p {
		@apply: text-left mr-5 w-200px text-xs pt-.5 mb-3;
		border-top: 0.3px solid black;
	}
}
</style>
