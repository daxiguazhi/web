<template>
  <div>
    <yd-navbar title="NavBar"></yd-navbar>
    这是首页
    <router-link :to="{name: 'Login'}">登陆</router-link>
    <router-link :to="{name: 'register'}">注册</router-link>
    <router-view></router-view>
  </div>
</template>

<script>
export default {

}
</script>
<style type="text/css">
  .navbar-bottom-line-color:after {
    border-color: blue !important;
  }
  .yd-navbar navbar-bottom-line-color{
    height: 8rem !important;
  }
</style>
