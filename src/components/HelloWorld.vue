<template>
  <h1>{{ msg }}</h1>
  <div class="card text-2xl">
    <button type="button" @click="count++">count is {{ count }}</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>
<style scoped>
.read-the-docs {
  color: #888;
}
</style>
