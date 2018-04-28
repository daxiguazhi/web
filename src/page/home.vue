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
    <div  v-for="item in imgList" >
      <imgframe :nickname="item.nickname" :img="item.img" :tag="item.tag"></imgframe>
    </div>
    <div id="footer">
      <mt-tabbar v-model="selected" fixed>
        <mt-tab-item id="">
          <img slot="icon" src="../img/icon/office.svg">
          首页
        </mt-tab-item>
        <mt-tab-item id="">
          <img slot="icon" src="../img/icon/attachment.svg">
          推荐
        </mt-tab-item>
        <mt-tab-item id="">
          <img slot="icon" src="../img/icon/earth.svg">
          广场
        </mt-tab-item>
        <mt-tab-item id="">
          <img slot="icon" src="../img/icon/personal-center.svg">
          个人中心
        </mt-tab-item>
      </mt-tabbar>
    </div>
    <!--<children :background="background" :label="'咸鱼'" @setBackground="setBackground"></children>-->
    <router-view></router-view>
  </div>
</template>

<script>
  import axios from 'axios'
  import img from '@/img/IMG_5510.jpg';
  import children from './children.vue'
  import imgframe from '../components/imgframe.vue'
  export default {
    components:{
      children,
      imgframe
    },
    name: 'home',
    data () {
      return {
        img: img,
        image:'',
        imgList:[
          {
            nickname:'麋鹿',
            img:'http://47.106.139.76/img/IMG_20140821_074346_HDR.jpg',
            tag:[
              {
                value:'摄影'
              },
              {
                value:'旅行'
              },
              {
                value:'风景'
              },
              {
                value:'摄影分享'
              }
            ]
          },
          {
            nickname:'环球旅行',
            img:'http://47.106.139.76/img/IMG_20141213_161942_HDR.jpg',
            tag:[
              {
                value:'摄影'
              },
              {
                value:'旅行'
              },
              {
                value:'风景'
              },
              {
                value:'摄影分享'
              }
            ]
          },
          {
            nickname:'也许',
            img:'http://47.106.139.76/img/IMG_20150115_135939.jpg',
            tag:[
              {
                value:'摄影'
              },
              {
                value:'旅行'
              },
              {
                value:'风景'
              },
              {
                value:'摄影分享'
              }
            ]
          },
          {
            nickname:'Jork',
            img:'http://47.106.139.76/img/IMG_20141205_100512_HDR.jpg',
            tag:[
              {
                value:'摄影'
              },
              {
                value:'旅行'
              },
              {
                value:'风景'
              },
              {
                value:'摄影分享'
              }
            ]
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
    border-bottom: solid 12px rgb(232, 232, 232)
  }

</style>
