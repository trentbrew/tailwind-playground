<script setup>
import { useCounterStore } from './stores/counter';
const store = useCounterStore();

store.count++;
store.increment(2);

console.log(store);


</script>

<template>
  <h1>Count is {{ store.count }}</h1>
  <h2>Double is {{ store.doubleCount }}</h2>
  <button @click="store.increment(1)">Increment</button>
  <button @click="store.waitAndAdd">Wait + Increment</button>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
