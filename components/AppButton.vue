<script setup>

defineProps({
  text: String,
  color: String
})

function onClick(){
  console.log('click')
}


</script>

<template>

    <div class=" header-buttons  "  >

      <button @click="onClick()" :style="{background: color }" class="bg-black rounded-md p-2 text-white hover:shadow-xl" >{{ text }}</button>



    </div>
</template>

<style scoped>

</style>