<template>
  <div id="home">
    <mt-header fixed title="首页"></mt-header>
    <div id="swipe">
      <mt-swipe :auto="4000">
        <mt-swipe-item>1</mt-swipe-item>
        <mt-swipe-item>2</mt-swipe-item>
        <mt-swipe-item>3</mt-swipe-item>
      </mt-swipe>
    </div>
    <div id="login">
      <router-link :to="{name: 'Login'}">登陆</router-link>
    </div>
    <div id="register">
      <router-link :to="{name: 'register'}">注册</router-link>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'home'
}
</script>
<style scoped>
  #login{
    margin-top: 200px;
}
  #swipe{
    height: 200px;
    width: 100%;
  }
  mt-swipe-item{
    background: red;
  }
</style>
