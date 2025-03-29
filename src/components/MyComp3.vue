<script setup lang="ts">
import {inject} from 'vue'
const msg = inject('msg')
</script>
<template>
  <view style="border: 1px solid red;padding: 10px;">
    <view>
  <text>comp3</text>
  </view>
  <text>{{msg}}</text>
</view>
</template>