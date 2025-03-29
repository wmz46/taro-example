<script setup lang="ts">
import MyComp1 from '@/components/MyComp1.vue'
import { ref,provide } from 'vue'
const msg = ref('Hello World')
provide('msg',msg)
</script>
<template>
  <nut-input v-model="msg"/>
  <MyComp1/>
</template>