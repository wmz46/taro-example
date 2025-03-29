<script setup lang="ts">
import { Button, Input } from '@nutui/nutui-taro';
const code = `
<script setup lang="ts">
import { Button, Input } from '@nutui/nutui-taro';
<\/script>
<template>
  <component :is="Button">我是按钮</component>
  <component :is="Input" v-bind="{ modelValue: '我是输入框' }"></component>
</template>
`
</script>
<template>
  <component :is="Button">我是按钮</component>
  <component :is="Input" v-bind="{ modelValue: '我是输入框' }"></component>
  <view>
    <text>{{ code }}</text>
  </view>
</template>