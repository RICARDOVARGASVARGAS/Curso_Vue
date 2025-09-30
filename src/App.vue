<script setup>

import { ref, reactive, computed } from 'vue'

const count = ref(0)

const user = reactive({
  name: 'John Doe',
  age: 18
})

const estado = computed(() => {
  return user.age >= 18 ? 'Eres mayor de edad' : 'Eres menor de edad'
})

function increment() {
  count.value++
  user.age++
}

function decrement() {
  count.value--
  user.age--
}



</script>

<template>

  <div>
    <h1>Count: {{ count }}</h1>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>


    <h1>Name: {{ user.name }}</h1>
    <h1>Age: {{ user.age }}</h1>


    <p>
      {{ estado }}
    </p>
  </div>

</template>

<style scoped></style>
