<script setup>
import { ref } from 'vue'

const parentMessage = ref('Parent')
const items = ref([{ message: '박민희' }, { message: '24'}])
</script>

<template>
<li v-for ="(item, index) in items">
    {{ parentMessage }} - {{ index }} - {{ item.message }}
</li>
</template>
