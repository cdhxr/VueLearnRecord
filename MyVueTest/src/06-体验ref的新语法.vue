<template>
  <div>
      <componentsTest01 ref="test"></componentsTest01>
      <button @click="getChildMethod">测试输出值</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import componentsTest01 from './components/componentsTest01.vue';
const test =ref('null')

const getChildMethod = () => {
    console.log(test.value.newMsg)
    test.value.logMsg()
}     
</script>

<style scoped>

</style>