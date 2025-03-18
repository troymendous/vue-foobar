<script setup>
import { ref } from 'vue';

const numbers = ref([]);
//const numbers = [];
// initialization; condition; afterthought
for (let i = 1; i <= 100; i=i+1) {
  if (i % 15 === 0) {
    numbers.value.push("FooBar");
  } else if (i % 3 === 0) {
    numbers.value.push("Foo");
  } else if (i % 5 === 0) {
    numbers.value.push("Bar");
  } else {
    numbers.value.push(i);
  }

  
}
setTimeout(() => numbers.value.push('penises'), 1)
</script>

<template>
  <div class="container">
    <h1>FooBar App</h1>
    <ul>
      <li v-for="(item, index) in numbers" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<style>
.container {
  font-family: Arial, sans-serif;
  text-align: center;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  font-size: 20px;
  margin: 5px 0;
}
</style>