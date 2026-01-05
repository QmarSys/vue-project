<script setup lang="ts">
import { ref } from 'vue'
const emit = defineEmits<{ (e: 'add', item: string): void }>()
const inputText = ref('')
const addItem = () => {
  inputText.value = inputText.value.trim()
  if (inputText.value) {
    emit('add', inputText.value)
    inputText.value = ''
  }
}
</script>
<template>
  <header
    class="flex flex-row flex-nowrap h-fit w-full px-8 py-4 items-center space-x-2 justify-between"
  >
    <input
      v-model="inputText"
      class="w-full outline-none border border-gray-300 rounded px-4 py-2"
      type="text"
    />
    <button
      @click="addItem"
      class="w-fit px-4 py-2 rounded-full bg-blue-300 cursor-pointer hover:bg-blue-400 active:bg-blue-500"
    >
      Add
    </button>
  </header>
</template>
