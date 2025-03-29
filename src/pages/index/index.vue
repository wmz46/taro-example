<script setup lang="ts">
import Taro from '@tarojs/taro';
</script>
<template>
  <view style="padding: 20px; display: flex; flex-direction: column; justify-content: center;">
    <text>TARO开发小程序的优势：</text>
    <text># 可以使用完整的Vue3开发体验</text>
    <text># 支持属性、事件及插槽透传</text>
    <nut-button @click="Taro.navigateTo({
      url: '/pages/demo1/index'
    })">支持属性、事件及插槽透传</nut-button>
    <text># 支持动态组件</text>
    <nut-button @click="Taro.navigateTo({ url: '/pages/demo2/index' })">支持动态组件</nut-button>
    <text># 支持jsx</text>
    <nut-button @click="Taro.navigateTo({
      url: '/pages/demo3/index'
    })">支持jsx</nut-button>
    <text># 支持provice和inject</text>
    <nut-button @click="Taro.navigateTo({
      url: '/pages/demo4/index'
    })">支持provice和inject</nut-button>
    <text style="color:red">不足：</text>
    <text># 不支持 keep-alive(小程序page隔离，应用场景不多)</text>
    <text># 不支持&lt;style scoped>（小程序不支持属性选择，所以导致[data-v-*]失效。但可以重写vue源码将data-v-*加入class就可以支持了）</text>
    <text># 运行库过大，运行库大概1M，加上第三方组件库，分包吃力</text>

  </view>
</template>
<style>
text,
button {
  margin-top: 20px;
}
</style>