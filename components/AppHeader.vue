<script setup>

    import {reactive} from 'vue'


   defineProps({
        title: String,



    })








</script>

<template>
  <div class=" flex  border-b-2 border-black w-full py-16 justify-between px-16 items-center" >
    <h1 class="py-8 text-2xl font-bold">{{ title  }}</h1>

    <AppButton text="Add Task" color="green"/>
  </div>

</template>
