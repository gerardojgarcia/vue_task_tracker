<script setup>


import AppHeader from '../components/AppHeader.vue'
import AppTasks from '../components/AppTasks.vue'

import { reactive, ref } from 'vue'

const tasks = reactive([
      {
    id: 1,
    text: 'Doctors Appointment',
    day: 'March 1st at 2:30pm',
    reminder: true,

  },
    {
      id: 2,
      text: 'Meeting at School',
      day: 'March 3rd at 2:30pm',
      reminder: true,

    },
    {
      id: 3,
      text: 'Food Shopping',
      day: 'March 3rd at 3:30pm',
      reminder: false,

    },
]
)



</script>


<template>
    <div >
        <div class="container flex flex-col border-2 border-black pb-40  shadow-xl  m-auto rounded-lg mt-32">

        <AppHeader title="Task Tracker"/>


          <div class="p-8">
            <AppTasks :tasks="tasks"/>
          </div>


        </div>


    </div>
</template>
