<script setup>
import { ref,reactive } from 'vue'

const props = defineProps({
  msg : String
})

const count = ref(0)
const local = reactive({
  per1: 6,
  per2: 2
})

function SomeFunction() {
  count.value--
  local.per2 += local.per1
}
</script>

<template>
  <h1>{{ local.per2 }}</h1>
  <h1>{{ props.msg }}</h1>

  <div class="card">
    <button type="button" @click="SomeFunction">count is {{ count }}</button>
  </div>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
