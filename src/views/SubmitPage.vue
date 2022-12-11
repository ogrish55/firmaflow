<template>
  <div class="rounded-2xl py-12 px-4">
		<div class="instructions-container">
			<p>Angiv hvilken type feedback du ønsker at indsende, samt hvilken afdeling feedbacken er tilegnet. Skriv din feedback i tekstfeltet og tryk derefter indsend.</p>
		</div>
		<feedback-type/>
    <InputForm  v-model="textInput"/>
    <button @click="submitFeedback">Indsend feedback</button>
  </div>
</template>
<script setup lang="ts">
import InputForm from '../components/InputForm.vue'
import FeedbackType from '../components/FeedbackType.vue'
import { ref } from 'vue'


const textInput = ref('');
const submitFeedback = () => {
  textInput.value = ''
}
</script>
<style lang="scss" scoped>
.instructions-container {
	@apply mx-auto max-w-2xl mb-8;
}
</style>