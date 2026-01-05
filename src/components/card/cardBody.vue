<script setup lang="ts">
const props = defineProps<{ text: string }>()
let colorClass = 'bg-gray-200 text-gray-800'
const textArr = props.text.split(' ')
const mainText = textArr.slice(1).join(' ')
const proiotyWord = textArr[0]
if (proiotyWord === '!!!:') {
  colorClass = 'bg-red-200 text-red-800'
} else if (proiotyWord === '!!:') {
  colorClass = 'bg-yellow-200 text-yellow-800'
} else {
  colorClass = 'bg-green-200 text-green-800'
}
</script>

<template>
  <div class="p-4 w-full rounded" :class="colorClass">
    <p>{{ mainText }}</p>
  </div>
</template>
