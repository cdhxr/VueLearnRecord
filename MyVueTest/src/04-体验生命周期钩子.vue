<script setup>
import { ref ,onMounted,onBeforeMount,onBeforeUpdate,onUpdated} from 'vue'
const count = ref(0)
onBeforeMount(() => {
    console.log('onBeforeMount')
})
onMounted(() => {
    console.log('onMounted')
})
onBeforeUpdate(() => {
    console.log('onBeforeUpdate')
}) 
onUpdated(() => {
    console.log('onUpdated')
})
</script>

<template>
    <div>

    </div>
</template>

<style scoped>

</style>