<template>
  <div>
    <InputForm  v-model="textInput"/>
    <HelloWorld :msg="textInput" />
    <button @click="submitFeedback">Indsend feedback</button>
  </div>
</template>
<script setup lang="ts">
import InputForm from '../components/InputForm.vue'
import HelloWorld from '../components/HelloWorld.vue'
import { ref } from 'vue'


const textInput = ref('');
const submitFeedback = () => {
  textInput.value = ''
}
</script>