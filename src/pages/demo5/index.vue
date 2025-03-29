<script setup lang="ts">
const html = "<view style='color:red'>你好</view>"
const code = `
<script setup lang="ts">
const html = "<view style='color:red'>你好</view>"
<\/script>
<template>
  <view v-html="html"></view>
</template>`
</script>
<template>
  <view v-html="html"></view>
  <text>{{code}}</text>
</template>