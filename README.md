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
<script setup> //setup Composition Api
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
```
//Composition Api
<script>
import {ref} from 'vue';
setup(){  //setup Composition Api
     const operationDisplay = ref('');
     const operation = ref('');
     const count = ref(0)
     const substractButton = () =>{
          count.value = count.value - 1;
          operation.value = 'subtract';
     }
     const addButton = () => {
          count.value = count.value + 1;
          operation.value = 'add';
     }
     
     watch(operation, (opt) =>{
          operationDisplay.value = (opt=='add')? 'Addition': 'Subtract';
     })
     
     return {
          count,
          substractButton,
          addButton
     }
 },
 methods: {
      add(){
           this.addButton();  
      }
 }
</script>

```
Options Api
```
<script>
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
### Use Cases
[Computed](https://vuejs.org/guide/essentials/computed.html#basic-example)

[Writable Computed](https://vuejs.org/guide/essentials/computed.html#writable-computed)
``` 
- Use for existing Data
- Do not use for fetching Data
```
[Watch](https://vuejs.org/api/reactivity-core.html#watch)
```
- Can be used for fetching Data
- Can monitor state,ref, variable etc. changes

```
### References

[VUE3 DEMO](https://github.com/pollyolly/VUE3-DEMO/blob/main/App.vue)

[VUE PATTENRS](https://learn-vuejs.github.io/vue-patterns/patterns/#handling-errors)

[PINIA](https://www.youtube.com/watch?v=JGC7aAC-3y8)
