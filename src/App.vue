<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div class="btn">
      盒子
      <div>sass使用</div>
      <h1>我是大标题<span>财务管理</span></h1>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
//1.标签的嵌套
//2.声明变量 sass -> $

$color: black;
$color2: skyblue;

.btn {
  color: red;
  h1 {
    color: blue;
    span {
      color: yellow;
    }
    &:hover {
    color: $color2;
  }
  }
  
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
