<template>
  <div id="login">
    <mt-header fixed title="登陆">
      <router-link to="/" slot="left">
        <mt-button icon="back" @click="handleClose">返回</mt-button>
      </router-link>
      <mt-button icon="more" slot="right" @click="more"></mt-button>
    </mt-header>
    <div id="home">
      <router-link to="/">首页</router-link>
    </div>
    <div id="register">
      <router-link to="/register">注册</router-link>
    </div>
    <router-view></router-view>
  </div>
</template>
<script>
import http from 'axios'
export default {
  name: 'login',
  created () {
    this.getData()
  },
  methods: {
    getData () {
      http.get('/selectexpress', {

      }).then(data => {

      })
    },
    handleClose: function () {
      console.log('返回')
    },
    more: function () {
      console.log('更多')
    }
  }
}
</script>
<style scoped>
  #home{
    margin-top: 100px;
  }
</style>
