<script setup>
import { ref } from 'vue'
import category from "@/assets/habitCategory.json"

const Category = ref(category)
//const parentMessage = ref('Parent')
//const items = ref([{ message: 'Foo' }, { message: 'Bar'}])
</script>

<template>
  <li v-for= "(item) in Category">
     {{ item.type }} {{ item.prefix }} {{ item.categorySubDivision }} 
     <hr>
  </li>
</template>
