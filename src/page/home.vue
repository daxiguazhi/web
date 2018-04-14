<template>
  <div id="home">
    <mt-header fixed title="首页"></mt-header>
    <!--<div id="swipe">
      <mt-swipe :auto="400000">
        <mt-swipe-item class="swip-item-1 item">

        </mt-swipe-item>
        <mt-swipe-item class="swip-item-2 item">2</mt-swipe-item>
        <mt-swipe-item class="swip-item-3 item">3</mt-swipe-item>
      </mt-swipe>
    </div>-->
    <!--<div id="login">
      <router-link :to="{name: 'Login'}">登陆</router-link>
    </div>
    <div id="register">
      <router-link :to="{name: 'register'}">注册</router-link>
    </div>-->
    <div id="main"></div>
    <img :src="img">
    <router-view></router-view>
  </div>
</template>

<script>
  import img from '@/img/IMG_5510.jpg';
  export default {
    name: 'home',
    data () {
      return {
        img: img
      }
    },
    methods: {
      loadMore () {
      }
    }
  }
</script>
<style scoped>
  #login{
    margin-top: 200px;
  }
  #swipe{
    margin-top: 40px;
    height: 200px;
    width: 100%;
  }
  .swip-item-1{
    background: url('../img/IMG_5510.jpg') no-repeat;
    background-size: 100% 100%;
  }
  #main{
    margin-top: 40px;
  }
  img{
    width: 100%;
    border-radius: 50%;
  }
</style>
