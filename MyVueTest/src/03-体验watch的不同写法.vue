<script setup>
import { ref } from "vue";
  const count = ref (0)
  const age = ref (20)
  const addCount = () => {
    count.value++
  }
  
  const addAge = () => {
    age.value++
  }

  watch([count,age],(newVal,oldVal) => {
    console.log('newVal:',newVal)
    console.log('oldVal:',oldVal)
  }
  {immdiately:true}
  )
</script>
  
<template>
  <div class="box">
    <button class="my-button" @click="addCount">result {{ count }}</button>
    <button class="my-button" @click="addAge">resultB {{ age }}</button>
  </div>
</template>

<style scoped>
.box {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  padding: 20px;
}

.my-button {
  display: inline-block;
  text-align: center;
  vertical-align: middle;
  padding: 15px 32px;
  text-decoration: none;
  font-size: 16px;
  font-weight: 500;
  border-radius: 4px;
  border: none;
  cursor: pointer;

  background-color: #4caf50;
  color: white;

  transition: background-color 0.3s ease;
  &:hover {
    background-color: #45a049;
  }

  &:active {
    background-color: #388e3c;
  }
}
</style>
