## VUE3

### Create Project
```
(Answered No)
$npm init vue@latest
$cd vue-demo
$npm install
$npm run dev
```
Sample
```
App.vue
<script setup>
import {ref} from 'vue';
const count = ref(0)
</script>
<template>
  <main>
        <h1>{{ count }}</h1>
        <button @click='count--'>-</button>
        <button @click='count++'>+</button>
  </main>
</template>
<style scoped>
</style>
```
