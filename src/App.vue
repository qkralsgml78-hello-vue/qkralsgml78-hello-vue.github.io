<script setup>
import { ref, onMounted } from 'vue'

//reactive state
const count = ref({
	cnt: 0,
	name: "Park",
	age: 20
})//초기값을 1로 세팅

// functions that mutate state and trigger updates
function increment(){ //반응형 선택 함수
    count.value.cnt++
    count.value.name = count.value.name.split('').reverse().join('')
    count.value.age = count.value.age + 3
}

//lifecycle hooks
onMounted(() => console.log(`Theinitial count is ${count.value}.`))
</script>


<template>
    <button @click="increment">Count is : {{ count.cnt }} {{ count.name }} {{ count.age }} </button>
</template>

<style scoped>
button {
    font-weight: bold;
}
</style>

