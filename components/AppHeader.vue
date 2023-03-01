<script setup>

    import {reactive} from 'vue'


   defineProps({
        title: String,


    })

    const actions = reactive([
      {
        id: 1,
        action: 'Add Task',

      },
      {
        id: 2,
        action: 'Remove Task'
      }
    ])






</script>

<template>
  <div class=" flex flex-col border-b-2 border-black w-full py-16 justify-evenly px-16" >
    <h1 class="py-8 text-2xl font-bold">Vue Task Tracker</h1>
    <div class=" header-buttons flex flex-row w-full space-x-16 "  >

        <button class="bg-green-900 rounded-full p-2 text-white" v-for="actions in actions" :key='actions.id'>{{ actions.action }}</button>



    </div>
  </div>

</template>
