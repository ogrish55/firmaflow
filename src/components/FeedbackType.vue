<template>
	<div class="flex max-w-lg justify-around mx-auto mb-4">
		<button v-for="type in activeButtons" class="feedback-type" :class="type.name" @click="chooseFeedbackType(type)">
			{{type.name}}
		</button>
	</div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue'

const buttonsArray = [
	{
		name: 'ris',
		active: false
	},
	{
		name: 'generelt',
		active: false
	},
	{
		name: 'ros',
		active: false
	}
]

const activeButtons = computed(() => {
	return buttonsArray.find((button) => {
		return button.active
	}) ?? buttonsArray
})

const chooseFeedbackType = (type: any) => {
	console.log(type)
}
</script>

<style lang="scss">
.feedback-type {
	@apply min-w-[9rem] border rounded-md focus:outline-none;
	&.ros {
		@apply bg-green-800 hover:border-green-800;
	}
	&.ris {
		@apply bg-red-800 hover:border-red-800;
	}
	&.generelt {
		@apply bg-gray-600 hover:border-gray-600;
	}
	&.active {
		@apply border-none;
	}
}
</style>