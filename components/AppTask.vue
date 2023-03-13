<script setup>

defineProps({
  task: Object,
})

</script>

<template>
  <div>
    <h3 class="text-2xl ">{{task.text}}</h3>
    <strong> {{task.day}} </strong>
    <p>{{task.reminder}}</p>
  </div>
</template>

<style scoped>

</style>