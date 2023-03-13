<script setup>

import AppTask from '../components/AppTask.vue'
defineProps({
  tasks: Array,
})
</script>

<template>
  <div class="divide-y divide-gray-100 py-6 space-y-4" v-for="task in tasks" :key="task.id">

<AppTask :task="task" />
  </div>
</template>

<style scoped>

</style>