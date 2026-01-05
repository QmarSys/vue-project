<script setup lang="ts">
import CardBody from '../card/cardBody.vue'

const { list } = defineProps<{ list: string[] }>()
</script>
<template>
  <body class="flex flex-col border border-gray-300 p-4 overflow-auto rounded h-full w-full">
    <div v-if="list.length !== 0">
      <CardBody v-for="(item, index) in list" :key="index" :text="item" />
    </div>
    <div class="text-gray-400 h-full w-full flex justify-center items-center" v-else>
      add !!!: for very important , !!: for important , else for normal items
    </div>
  </body>
</template>
