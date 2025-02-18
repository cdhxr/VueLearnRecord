<script setup>
import ComponentsTest01 from "./components/componentsTest01.vue";
import { ref } from "vue";
const msg = ref("父组件的数据");

const getMsg = (val) => {
  console.log(val);
};
</script>

<template>
  <div class="box">
    <h2>父组件</h2>
    <ComponentsTest01 :msg="msg" @send-msg="getMsg"></ComponentsTest01>
  </div>
</template>