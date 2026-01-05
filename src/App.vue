<script setup lang="ts">
import formHeader from './components/form/formHeader.vue'
import formBody from './components/form/formBody.vue'
import { reactive } from 'vue'
const listText = reactive<string[]>([])
</script>

<template>
  <div class="flex flex-col flex-nowrap h-screen w-screen p-8 space-y-4">
    <formHeader @add="listText.push($event)" />
    <formBody :list="listText" />
  </div>
</template>
