<script setup>

import AppTask from '../components/AppTask.vue'
defineProps({
  tasks: Array,
})

defineEmits(['delete-task'])



</script>

<template>
  <div class="  ease-out duration-500 divide-y divide-gray-100 py-6 space-y-4" v-for="task in tasks" :key="task.id">

<AppTask :task="task" @delete-task="$emit('delete-task', task.id)" />
  </div>
</template>

<style scoped>

</style>