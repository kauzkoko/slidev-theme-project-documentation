<script setup lang="ts">
import { handleBackground } from "../layoutHelper"
const props = defineProps({
	image1: {
		type: String,
	},
	image2: {
		type: String,
	},
	image3: {
		type: String,
	},
	image4: {
		type: String,
	},
	caption1: {
		type: String,
	},
	caption2: {
		type: String,
	},
	caption3: {
		type: String,
	},
	caption4: {
		type: String,
	},
})
</script>

<template>
	<div class="grid grid-cols-[.8fr_1.6fr_1.6fr] w-full h-full py-18 pr-13 pl-28">
		<div class="caption relative grid grid-row-2 gap-y-4">
			<div>
				<div class="absolute right-0">
					<p>{{ props.caption1 }}</p>
					<p>{{ props.caption2 }}</p>
				</div>
			</div>
			<div>
				<div class="absolute right-0 top-50%">
					<p>{{ props.caption3 }}</p>
					<p>{{ props.caption4 }}</p>
				</div>
			</div>
		</div>
		<div class="grid grid-row-2 gap-y-4 mr-4">
			<div class="test" :style="handleBackground(props.image1)"></div>
			<div :style="handleBackground(props.image2)"></div>
		</div>
		<div class="grid grid-row-2 gap-y-4">
			<div :style="handleBackground(props.image3)"></div>
			<div :style="handleBackground(props.image4)"></div>
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
