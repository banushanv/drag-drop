<!-- Please remove this file from your project -->
<template>
  <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
    <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
    
      <draggable v-model="myArray" group="people" @start="drag=true" @end="drag=false" class="list-group" tag="ul">
        <div v-for="element in myArray" :key="element.id">{{element.name}}</div>
    </draggable>
    </div>
  </div>
</template>

<script>
import draggable from 'vuedraggable';
export default {
  name: 'NuxtTutorial',
  components: {
            draggable,
  },
  data: () => ({
    myArray:[{id:1,name:'Javascript'},{id:2,name:'Typescript'},{id:3,name:'Vue'},{id:4,name:'React'},{id:5,name:'Angular'}]
  }) 
}
</script>
