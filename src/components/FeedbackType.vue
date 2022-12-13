<template>
	<div class="mb-4 flex max-w-[500px] mx-auto justify-around">
		<button
			v-for="button in buttons"
			:key="button"
			class="feedback-type"
			:class="[button.name, button.active ? 'active' : '']"
			@click="chooseFeedbackType(button)"
		>
			{{button.name}}
		</button>
	</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const buttons = ref([
	{ name: 'ris', active: false },
	{ name: 'generelt', active: true },
	{ name: 'ros', active: false }
])

const chooseFeedbackType = (type: any) => {
	buttons.value.forEach((button) => {
		button.active = false;
	})
	type.active = true;
}
</script>

<style lang="scss" scoped>
.feedback-type {
	@apply min-w-[9rem] rounded-md focus:outline-none border border-transparent;
	&.ros {
		@apply bg-green-800;
	}
	&.ris {
		@apply bg-red-800;
	}
	&.generelt {
		@apply bg-gray-600;
	}
	&:not(.active) {
		@apply hover:border-transparent;
	}
	&.active {
		@apply border-sky-200 hover:border-sky-200;
	}
}
</style>