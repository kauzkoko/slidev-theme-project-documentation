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
	linkSrc1: {
		type: String,
	},
	linkSrc2: {
		type: String,
	},
	linkSrc3: {
		type: String,
	},
	linkSrc4: {
		type: String,
	},
})
</script>

<template>
	<div class="grid grid-cols-[.8fr_1.6fr_1.6fr] w-full h-full py-18 pr-13 pl-28">
		<div class="caption relative grid grid-row-2 gap-y-4">
			<div>
				<div class="absolute right-0">
					<p>{{ props.caption1 }}<br/>
						<a v-if="props.linkSrc1" :href="props.linkSrc1" target="_blank" alt="test">{{  props.linkSrc1.slice(0, 15) + '...'}}</a>
					</p>
					<p>{{ props.caption2 }}<br/>
						<a v-if="props.linkSrc2" :href="props.linkSrc2" target="_blank" alt="test">{{ props.linkSrc2.slice(0, 15) + '...' }}</a>
					</p>
				</div>
			</div>
			<div>
				<div class="absolute right-0 t4p-50%">
					<p>{{ props.caption3 }}<br/>
						<a v-if="props.linkSrc3" :href="props.linkSrc3" target="_blank" alt="test">{{  props.linkSrc3.slice(0, 15) + '...'}}</a>
					</p>
					<p>{{ props.caption4 }}<br/>
						<a v-if="props.linkSrc4" :href="props.linkSrc4" target="_blank" alt="test">{{ props.linkSrc4.slice(0, 15) + '...' }}</a>
					</p>
				</div>
			</div>
		</div>
		<div class="grid grid-row-2 gap-y-4 mr-4">
			<div :class="props.linkSrc1 ? 'transform' : ''" class="hover:(scale-101 rotate-2) transition-transform duration-200" :style="handleBackground(props.image1)">
				<a v-if="props.linkSrc1" class="w-full h-full absolute " :href="props.linkSrc1" target="_blank" alt="test"></a>
			</div>
			<div :class="props.linkSrc2 ? 'transform' : ''" class="hover:(scale-101 rotate-2) transition-transform duration-200" :style="handleBackground(props.image2)">
				<a v-if="props.linkSrc2" class="w-full h-full absolute " :href="props.linkSrc2" target="_blank" alt="test"></a>
			</div>
		</div>
		<div class="grid grid-row-2 gap-y-4">
			<div :class="props.linkSrc3 ? 'transform' : ''" class="hover:(scale-101 rotate-2) transition-transform duration-200" :style="handleBackground(props.image3)">
				<a v-if="props.linkSrc3" class="w-full h-full absolute " :href="props.linkSrc3" target="_blank" alt="test"></a>
			</div>
			<div :class="props.linkSrc4 ? 'transform' : ''" class="hover:(scale-101 rotate-2) transition-transform duration-200" :style="handleBackground(props.image4)">
				<a v-if="props.linkSrc4" class="w-full h-full absolute " :href="props.linkSrc4" target="_blank" alt="test"></a>
			</div>
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
