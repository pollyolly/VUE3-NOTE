## VUE3

### Create Project
```
(Answered No)
$npm init vue@latest
$cd vue-demo
$npm install
$npm run dev
```
Composition Api (New)
```
//Composition Api
<script setup>
import {ref} from 'vue';
const count = ref(0)
const substractButton = () =>{
        count.value = count.value - 1;
}
const addButton = () => {
        count.value = count.value + 1;
}
</script>

```
Options Api
```
<script setup>
//Options Api
export default ({
     data(){
         return {
            count: 0
         }
     },
     methods: {
        substractButton(){
            this.count = this.count - 1;
        },
        addButton(){
            this.count = this.count + 1;
        }
     }
})
</script>
```
```
<template>
  <main>
        <h1>{{ count }}</h1>
        <button @click='count--'>-</button>
        <button @click='count++'>+</button>
        <br>
        <br>
        <button @click='substractButton'>Substract</button>
        <button @click='addButton'>Add</button>
  </main>
</template>
<style scoped>
</style>
```
