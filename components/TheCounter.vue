<template>
  <div>
    <h1>Counter</h1>
    <p>{{ counter.count }}</p>
    <button @click="counter.increment">+</button>
    <button @click="counter.decrement">-</button>
  </div>
</template>

<script setup lang="ts">
import { useCounter } from '~~/stores/counter';
const counter = useCounter();
</script>
