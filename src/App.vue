<script setup>
// const userName = 'Sachi'
// console.log(userName)
import { ref, reactive } from 'vue'
const title = 'happy'
let price = ref(9.99)
function increment() {
  price.value += 1
  me.age -= 1
  console.log(price)
}

const info = ref({
  students: 1000,
  rating: 4,
})
console.log(info.value.students)

const me = reactive({
  name: 'happy',
  age: 29,
}) //引数にリアクティブにしたいオブジェクトを入れる
console.log(me)
</script>
<template>
  <h1>Title: {{ title }}</h1>
  <h3>Price: {{ price }}</h3>
  <h3>Info: {{ info.students }}</h3>
  <h3>Me: {{ me.age }}</h3>
  <button @click="increment">click</button>
</template>
<style>
h1 {
  color: red;
}
</style>
