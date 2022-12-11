<template>
  <div>
    <textarea
      rows="6"
      cols="50"
      class="p-4 resize-none border-none outline-none"
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