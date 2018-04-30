<template>
  <div id="register">
    <mt-header fixed title="注册">
      <router-link to="/" slot="left">
        <mt-button icon="back">返回</mt-button>
      </router-link>
      <mt-button slot="right" @click="login">登陆</mt-button>
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
export default {
  name: 'register',
  methods: {
    login: function () {
      this.$router.push({path:'/login'})
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
