<script setup>
import { reactive, computed, ref } from 'vue';

//reactive는 string, number는 잘 안들어감(tyod을 잘 가림)
//기본적으로 ref를 쓰고 어디서는 이렇게 다른데서는 뭘 쓴다 이정도만 알면 된다.
const author = ref({ // reactive를 사용하면 
  name: 'John Doe',
  books: [1, 2, 3]
});

const check  = computed(() => {
    return author.value.books.length > 2 ? 'yes' : 'no' // 여기서 value를 빼야 한다.
   // return ahthor.books.length > 2 ? 'yes' : 'no'
})
</script>

<template>
    <span>😊 :</span>
    <span>{{ author.books.length > 2 ? 'yes' : 'no' }} </span>
    <p>computed</p>
    <div>{{ check }}</div>
</template>


