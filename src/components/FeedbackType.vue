<template>
		<TransitionGroup name="list" tag="div" class="max-w-lg mb-4 mx-auto" appear>
			<div v-if="activeButtons.length">
				<button
					v-if="activeButtons.length"
					v-for="type in activeButtons"
					:key="type"
					class="feedback-type"
					:class="type.name"
					@click="chooseFeedbackType(type)"
				>
					{{type.name}}
				</button>
			</div>
			<div v-else>
				<button
					:class="activeButton.name"
					class="feedback-type"
					@click="chooseFeedbackType(activeButton)"
				>
					{{activeButton.name}}
				</button>
			</div>
		</TransitionGroup>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue'

const buttonsArray = ref([
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
])

const activeButtons = computed(() => {
	return buttonsArray.value.some((button) => {
		return button.active
	}) ? [] : buttonsArray
})

const activeButton = computed(() => {
	return buttonsArray.value.find((button) => {
		return button.active
	})
})

const chooseFeedbackType = (type: any) => {
	type.active = !type.active;
}
</script>

<style lang="scss">
.list-enter-active,
.list-leave-active {
	transition: all 0.5s ease;
}
.list-enter-from,
.list-leave-to {
	opacity: 0;
}
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