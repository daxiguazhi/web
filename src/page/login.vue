<template>
  <div id="login">
    <mt-header fixed title="登陆">
      <router-link to="/" slot="left">
        <mt-button icon="back" @click="">返回</mt-button>
      </router-link>
      <mt-button slot="right" @click="register">注册</mt-button>
    </mt-header>
    <div id="main">
      <div>
        <input type="text" class="text" placeholder="用户名">
      </div>
      <div>
        <input type="password" class="text" placeholder="密码">
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>
<script>
import http from 'axios'
export default {
  name: 'login',
  created () {
  },
  methods: {
    register(){
      this.$router.push({path:'/register'})
    }
  }
}
</script>
<style scoped>
  #main{
    margin-top: 180px;
  }
  #main div{
    display: flex;
    justify-content: center;  /*垂直水平居中*/
    align-items:center;
  }
  #main .text{
    border-bottom: 1px solid #dbdbdb;
    border-top:0px;
    border-left:0px;
    border-right:0px;
    margin-left: 10px;
    height: 45px;
    width: 80%;
  }
</style>
