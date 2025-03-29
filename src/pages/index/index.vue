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
    <text># 支持jsx组件</text>
    <nut-button @click="Taro.navigateTo({
      url: '/pages/demo3/index'
    })">支持jsx组件</nut-button>
    <text># 支持provide和inject</text>
    <nut-button @click="Taro.navigateTo({
      url: '/pages/demo4/index'
    })">支持provide和inject</nut-button>
    <text># 支持v-html</text>
    <nut-button @click="Taro.navigateTo({
      url: '/pages/demo5/index'
    })">支持v-html</nut-button>
    <text># 支持全局状态管理（vue3的ref和reactive天生就很适合做全局状态管理，并不需要额外引入vuex或pinia）</text>
    <text># 支持路由，但由于page隔离，返回按钮交互问题，一般不建议引入路由，容易和小程序路由搞混，且只能在当前页使用，意义不大</text>
    <text style="color:red">不足：</text>
    <text># 页面存在循环较多的双向绑定组件时，会导致卡顿。解决方案：1.将组件拆分到不同页面；2.使用虚拟列表技术，只渲染可见区域；3.减少非必要的双向绑定和响应式计算</text>
    <text># 不支持 keep-alive(小程序page隔离，应用场景不多)</text>
    <text># 不支持&lt;style scoped>（小程序不支持属性选择，所以导致[data-v-*]失效。但可以重写vue源码将data-v-*加入class就可以支持了）</text>
    <text># 运行库过大，运行库大概1M，加上第三方组件库，分包吃力</text>
    <text># 不支持异步组件（小程序限制）</text>
    <text>#
      不支持app(建议通过tauri2或Capacitor搭建一个web套壳app，taro打包产物可以打入app中，页面则无需网络请求。缺点：不同手机的webview版本会有兼容性问题，当随着手机的升级换代，兼容性的包袱会越来越小)</text>

  </view>
</template>
<style>
text,
button {
  margin-top: 20px;
}
</style>