<template>
  <h1>笨蛋火火</h1>
  <button @click="foo">btn</button>
  <p>{{ msg }}</p>
</template>

<script setup>
import { ref } from 'vue';

let msg = ref("hhh");
async function foo() {
  const res = await fetch("https://jsonplaceholder.typicode.com/todos/1");
  const data = await res.json()
  msg.value = data
}
</script>
