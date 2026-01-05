<script setup lang="ts">
import CardBody from '../card/cardBody.vue'

const { list } = defineProps<{ list: string[] }>()
</script>
<template>
  <body class="flex flex-col border border-gray-300 p-4 overflow-auto rounded h-full w-full">
    <CardBody v-for="(item, index) in list" :key="index" :text="item" />
  </body>
</template>
