<script setup>


import AppHeader from '../components/AppHeader.vue'
import AppTasks from '../components/AppTasks.vue'
import AppAddTask from '../components/AppAddTask.vue'

import { reactive, ref } from 'vue'

const tasks = ref([
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
      reminder: false,

    },
    {
      id: 3,
      text: 'Food Shopping',
      day: 'March 3rd at 3:30pm',
      reminder: true,

    },
]
)

function deleteTask(id){

  if(confirm('Are you sure?')){
    tasks.value = tasks.value.filter((task) => task.id !== id)

console.log('task', id)
  }



}

function toggleReminder(id){

  tasks.value = tasks.value.map((task) => task.id === id ? {...task, reminder: !task.reminder } : task

  )
  console.log(id)
}



</script>


<template>
    <div >
        <div class="container flex flex-col border-2 border-black pb-16 max-w-2xl rounded-lg mt-16 m-auto">

        <AppHeader title="Task Tracker"/>
          <AppAddTask/>



          <div class="p-8">
            <AppTasks :tasks="tasks" @delete-task="deleteTask" @toggle-reminder="toggleReminder"/>
          </div>




        </div>


    </div>
</template>

<style scoped >

  .container {
    background-color: #f4d738;
    box-shadow: 4px 6px black;
  }

</style>
