<script setup>
import componentsTest03 from './components/componentsTest03.vue';
import { provide, ref } from 'vue';

const test = ref('sehr gut');
provide('item', test)

const changeMsg = () => {
  test.value = 'xopowo';
}

provide('itemB', changeMsg)
</script>

<template>
  <div class="box">
    <h2>祖先组件</h2>
    <componentsTest03></componentsTest03>
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
</style>