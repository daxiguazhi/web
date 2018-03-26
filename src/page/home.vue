<template>
  <div>
    <mt-swipe :auto="4000">
      <mt-swipe-item>1</mt-swipe-item>
      <mt-swipe-item>2</mt-swipe-item>
      <mt-swipe-item>3</mt-swipe-item>
    </mt-swipe>
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
</style>
