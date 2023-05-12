<script setup>

defineProps({
  text: String,
  color: String
})

const emit = defineEmits(['toggle-add-task'])

function onClick(){
  emit('toggle-add-task')
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