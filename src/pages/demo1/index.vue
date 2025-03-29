<script setup lang="ts">
import Taro from '@tarojs/taro';
import MyButton from '@/components/MyButton.vue';
const code = `
<MyButton type="primary" @click="Taro.showToast({ title: '你好' })">你好</MyButton>
<view v-html="html"></view>
MyButton.vue
<script setup lang="ts">
import { useSlots } from 'vue';
const slots = useSlots();
<\/script>
<template>
  <nut-button v-bind="$attrs">
    <template v-for="(_, name) in slots" #[name]="slotProps">
      <slot :name="name" v-bind="slotProps || {}" />
    </template>
</nut-button>
</template>
`

</script>
<template>
  <MyButton type="primary" @click="Taro.showToast({ title: '你好' })">你好</MyButton>
  <view>
    <text>{{ code }}</text>
  </view>
</template>