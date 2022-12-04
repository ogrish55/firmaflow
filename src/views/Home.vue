<template>
  <div>
    <InputForm  v-model="textInput"/>
    <HelloWorld :msg="textInput" />
    <button @click="submitFeedback">Submit</button>
  </div>
</template>
<script setup lang="ts">
import { ref } from 'vue'
import HelloWorld from '../components/HelloWorld.vue'
import InputForm from '../components/InputForm.vue'

const textInput = ref('');
const submitFeedback = () => {
  textInput.value = ''
}
</script>
