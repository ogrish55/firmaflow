<template>
  <div>
    <textarea
      placeholder="Insert your feedback to the company here..."
      rows="6"
      cols="50"
      class="p-4 resize-none"
      :value="modelValue"
      @input="emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>
<script setup lang="ts">
defineProps<{
  modelValue: string,
}>()

const emit = defineEmits<{
  (event: 'update:modelValue', payload: string): void;
}>();

</script>