
<script setup>

useHead({
  title: 'My App',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],
  
  link: [     {
      rel: 'icons',
      href: 'https://fonts.googleapis.https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css'
    }, ]
})
</script>


<template>
  <div >
   <NuxtPage/>

  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Archivo:wght@300;400;700&display=swap');

body {
  font-family: 'Archivo', sans-serif;
  background-color: #FDFD96;
}
</style>
