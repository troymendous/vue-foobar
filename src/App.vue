<template>
  <div>
    <h1>FooBar Vue App</h1>
    <ul>
      <li v-for="num in numbers" :key="num">{{ displayText(num) }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numbers: Array.from({ length: 100 }, (_, i) => i + 1),
    };
  },
  methods: {
    displayText(num) {
      if (num % 3 === 0 && num % 5 === 0) return "FooBar";
      if (num % 3 === 0) return "Foo";
      if (num % 5 === 0) return "Bar";
      return num;
    },
  },
};
</script>

<style>
h1 {
  text-align: center;
}
ul {
  list-style-type: none;
  padding: 0;
  text-align: center;
}
</style>
