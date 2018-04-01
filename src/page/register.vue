<template>
  <div id="register">
    <mt-header fixed title="注册">
      <router-link to="/" slot="left">
        <mt-button icon="back">返回</mt-button>
      </router-link>
      <mt-button icon="more" slot="right" @click="more"></mt-button>
    </mt-header>
    <div  id="home">
      <router-link to="/">首页</router-link>
    </div>
    <div id="login">
      <router-link to="/login">登陆</router-link>
    </div>
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  name: 'register',
  methods: {
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
