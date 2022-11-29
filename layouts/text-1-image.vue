<script setup lang="ts">
import { handleBackground } from "../layoutHelper"
const props = defineProps({
	image: {
		type: String,
	},
	caption: {
		type: String,
	},
	linkSrc: {
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
			<div v-if="props.caption" class="absolute right-0">
				<p>{{ props.caption }}<br/>
					<a :href="props.linkSrc" target="_blank" alt="test">{{props.linkSrc.slice(0, 15)}}...</a>
				</p>
			</div>
		</div>
		<div class="grid grid-row-2 gap-y-4">
			<div class="transform hover:(scale-101 rotate-2) transition-transform duration-200" :style="handleBackground(props.image)">
				<a class="w-full h-full absolute " :href="props.linkSrc" target="_blank" alt="test"></a>
			</div>
			<div class="bg-white"></div>
		</div>
	</div>
</template>

<style lang="scss">
.caption {
	p {
		@apply text-left mr-5 w-200px text-xs pt-1 mb-3;
		border-top: 0.3px solid gray;
	}
}
</style>
