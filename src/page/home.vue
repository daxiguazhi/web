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
    <ul
      v-infinite-scroll="loadMore"
      infinite-scroll-disabled="loading"
      infinite-scroll-distance="10"
    >
      <li v-for = " item in list ">{{ item }}</li>
    </ul>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      list: [{
        a: 1
      }]
    }
  },
  methods: {
    loadMore () {
      this.loading = true
      setTimeout(() => {
        let last = this.list[this.list.length - 1]
        for (let i = 1; i <= 10; i++) {
          this.list.push(last + i)
        }
        this.loading = false
      }, 2500)
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
</style>
