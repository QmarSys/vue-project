<script setup lang="ts">
const props = defineProps<{ text: string }>()
let colorClass = 'bg-gray-200 text-gray-800'
const textArr = props.text.split(' ')
const proiotyWord = textArr[textArr.length - 1]
if (proiotyWord?.includes('!!!')) {
  colorClass = 'bg-red-200 text-red-800'
} else if (proiotyWord?.includes('!!')) {
  colorClass = 'bg-yellow-200 text-yellow-800'
} else {
  colorClass = 'bg-green-200 text-green-800'
}
</script>

<template>
  <div class="p-4 w-full rounded" :class="colorClass">
    <p>{{ props.text }}</p>
  </div>
</template>
