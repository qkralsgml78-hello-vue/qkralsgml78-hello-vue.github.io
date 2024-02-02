<script setup>
import { ref } from 'vue'

const show = ref(true)
const list = ref([1, 2, 3])

const toggleList = () => {
  show.value = !show.value
}

const addToList = () => {
  list.value.push(Math.max(...list.value) + 1)
}

const removeFromList = () => {
  list.value.pop()
}

const reverseList = () => {
  list.value.reverse()
}
</script>

<template>
  <button @click="toggleList">List 렌더링 ON/OFF </button>
  <button @click="addToList">List 추가</button>
  <button @click="removeFromList">List 제거</button>
  <button @click="reverseList">List 뒤집기</button>

  <ul v-if="show">
    <li v-for="item in list" :key="item">{{ item }} </li>
  </ul>
  <p v-else-if="list.length">List is not empty, but hidden.</p>
  <p v-else>List is not empty.</p>
</template>

