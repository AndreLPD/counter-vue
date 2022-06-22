<script setup>
import { ref } from 'vue'

const count = ref(0);

  defineProps({
  msg: String,
  initialValue:Number
})

function increment(){
  count.value++
}

function decrement(){
  count.value--
}

function initialValue(){
  count.value = 0;
}




</script>

<template>
  <h1>{{ msg }}</h1>

  <p>
    {{count}}
  </p>

  <p>
    <a>
      <button type="button" @click="increment">increment</button>
    </a>
    <a>
      <button type="button" @click="decrement">decrement</button>
    </a>
    <a>
      <button type="button" @click="initialValue">initial value</button>
    </a>
  </p>

  
  
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
