<script setup>

    import {reactive} from 'vue'


   defineProps({
        title: String,


    })

    const state = reactive({ count: 0 })

    function increment() {
  state.count++
}

    


</script>

<template>
    <div class=" flex border-b-2 border-black w-full py-16">

        <button class="bg-green-900 rounded-full p-2 text-white" @click="increment()">{{ state.count }}</button>


        
    </div>
</template>