<script setup>
import { useStoreCounter } from '../stores/counter';
const counter = useStoreCounter();

const patch = () => {
  counter.$patch({
    count: 100,
    user: {
      name: 'Jane Doe',
    },
  });
};
</script>

<template>
  <h2>Hello Pinia</h2>
  <p>カウント:{{ counter.count }}</p>
  <button @click="patch">Patch</button>
</template>
