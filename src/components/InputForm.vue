<template>
  <div class="flex flex-col max-w-[500px] mx-auto">
    <textarea
      rows="6"
      cols="50"
      class="p-4 resize-none border-none outline-none text-area"
			:class="{'fade-out': fadeOut}"
			v-model="input"
    />
		<button
			class="button mt-4 w-40 mx-auto focus:outline-none"
			@click="submitFeedback"
		>
			Indsend
		</button>
	</div>
</template>
<script setup lang="ts">
import { ref } from 'vue'

const fadeOut = ref(false)
const input = ref('')

const submitFeedback = () => {
	fadeOut.value = true
	setTimeout(() => {
		input.value = ''
		fadeOut.value = false
	}, 500)
}
</script>
<style scoped lang="scss">
.text-area {
	transition: color 0.5s;
	&.fade-out {
		color: transparent;
	}
}
</style>