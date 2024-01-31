<script setup>
import { ref } from 'vue'
import category from "@/assets/habitCategory.json"

const Category = ref(category)
//const parentMessage = ref('Parent')
//const items = ref([{ message: 'Foo' }, { message: 'Bar'}])


</script>
<template>
    <template v-for="(item) in Category">
    <li v-if="item.prefix == '건강한'">
    <br>
    type: {{ item.type }} <br>
    prefix: {{ item.prefix }} <br>
    categorySubDivision: {{ item.categorySubDivision }} <br>
     <hr>
  </li>
  </template>
</template>
