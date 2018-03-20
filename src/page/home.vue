<template>
  <div>
    这是首页
    <router-link :to="{name: 'Login'}">登陆</router-link>
    <router-link :to="{name: 'Register'}">注册</router-link>
    <router-view></router-view>
  </div>
</template>
