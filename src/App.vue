<script setup>
import { ref } from 'vue'
import category from "@/assets/habitCategory.json"

const Category = ref(category)
//const parentMessage = ref('Parent')
//const items = ref([{ message: 'Foo' }, { message: 'Bar'}])
</script>

<template>
  <li v-for= "(item) in Category">
<br>
type: {{ item.type }} <br>
prefix: {{ item.prefix }} <br>
categorySubDivision: {{ item.categorySubDivision }} <br>
     <hr>
  </li>
</template>
