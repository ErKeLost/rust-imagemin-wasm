<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from './components/HelloWorld.vue'
import * as init from '../../rust-imagemin/pkg'
import img from './pink.jpg'
// console.log(rust.get_image_view('../public/vite.svg'))
console.log(img)
const res = init.digest('aaa')
console.log(res)
var reader = new FileReader() // 这是核心, 读取操作就是由它完成.
const imgRes = new Image()
imgRes.src = img
console.log(imgRes)
</script>

<template>
  <div>
    <img :src="img" width="400" alt="" />
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
