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
//3.变量运算
//4.混入(函数) 声明混入:@mixin 混入名称  使用混入: @include 混入名称
$color: black;
$color2: skyblue;

$w1: 20px;
$w2: 30px;

@mixin cc($col: skyblue) {
  color: $col;
}

.btn {
  color: red;
  h1 {
    color: blue;
    span {
      color: yellow;
    }
    &:hover {
      // color: $color2;
      // @include cc(green);
      @include cc();

      font-size: $w1 + $w2;
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
