<script setup>
import HelloWorld from './components/HelloWorld.vue'
import { reactive } from 'vue';

const local = reactive({
  stroka : "Переменная из строки"
})

</script>

<template>
  <HelloWorld :msg="local.stroka" />
  <HelloWorld msg="local.stroka" />
</template>

<style scoped>

</style>
