<script setup>
import { emit } from 'process';


defineProps({
  task: Object,
})




</script>

<template>
  <div :class="[task.reminder ?  'reminder' : '', 'task']">
    <h3 class="text-2xl space-between flex align-center ">{{task.text}}
    <span class="text-red-500 ml-auto border-2 border-black rounded-md p-2 " @click="$emit('delete-task', id)">Delete</span>

    </h3>
    <strong> {{task.day}} </strong>

  </div>
</template>
 
<style scoped>

.task {


  cursor: pointer;
}

.task.reminder {
  border-left: 5px solid green;
}

h3 > span {
  background-color: #FDFD96;
  font-size: 1.2rem;
}

h3>span:hover {
  box-shadow: 4px 6px black;
  transform: translateX(-2px) translateY(-2px);
  transition: all 350ms;
}

</style>