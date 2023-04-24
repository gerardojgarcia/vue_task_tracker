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

      <button @click="onClick()" :style="{background: color }" class="bg-black rounded-md p-2 text-black duration-200 border-2 border-black  " >{{ text }}</button>



    </div>
</template>

<style scoped>





button:hover {

  box-shadow: 4px 6px black;

}

</style>