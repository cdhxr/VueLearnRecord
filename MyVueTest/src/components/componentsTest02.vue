<script setup>
import { inject } from 'vue';
const msg = inject('item');

const changeStr = inject('itemB');

const changeVal = ()=>{
  changeStr();
}
</script>
<template>
  <div class="son">
    <h2>孙子组件</h2>
    <h3>{{ msg }}</h3>
    <button @click="changeVal">改变祖先组件的值</button>
  </div>
</template>

<style scoped>
.son {
  padding: 51px;
  border: 1px solid pink;
}
</style>