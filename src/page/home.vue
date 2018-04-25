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
    <!--<img :src="img">-->
    <!--<img :src="image">-->
    <div  v-for="item in image" >
      <div id="head">
        <img src="../img/head.jpg" alt="">
      <span>Mynickname</span></div>
      <img :src="item.img" :alt="item.label">
      <div id="footer">{{item.lable}}留言</div>
      <div id="sign">这是图标</div>
    </div>
    <children :background="background" :label="'咸鱼'" @setBackground="setBackground"></children>
    <router-view></router-view>
  </div>
</template>

<script>
  import axios from 'axios'
  import img from '@/img/IMG_5510.jpg';
  import children from './children.vue'
  export default {
    components:{
      children
    },
    name: 'home',
    data () {
      return {
        img: img,
        image:'',
        imgList:[
          {
            url:'a',
            label:'a'
          },
          {
            url:'b',
            label:'b'
          },
          {
            url:'c',
            label:'c'
          },
        ],
        background:'background:blue',
      }
    },
    created(){
      const root = this;
      axios.get('public/test/Test/index').then(function (res) {
        root.image = res.data;
        console.log(res.data);
      })
    },
    methods: {
      loadMore () {
      },
      setBackground(val){
        this.background = val;
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
  #head{
    height:50px;
    line-height: 50px;
  }
  #head img{
    height:40px;
    width:40px;
    border-radius: 50%;
    margin-left: 10px;
    margin-top: 5px;
  }
  #head span{

  }
  #footer{
    height:50px;
    border-bottom:1px dashed rgba(83, 77, 77, 0.5)
  }
  #sign{
    height:30px;
    border-bottom: solid 12px rgba(216, 210, 210, 0.5)
  }

  img{
    width: 100%;
    /*border-radius: 50%;*/ /*圆形头像框*/
  }
</style>
