<template>
  <div>
    <div id="head">
      <img src="../img/head.jpg" alt="">
      <span class="nickname">{{nickname}}</span></div>
    <img :src="img" alt="">
    <div id="footer">
      <span class="tagheader">＃</span>
      <div  v-for="item in tag" >
        <span class="tag">{{item.value}}</span>
      </div>
    </div>
    <div id="sign">
      <img src="../img/icon/good.svg" alt="">
      </div>
  </div>

</template>
<script>
  export default {
    props:['nickname','img','tag'],
    methods:{
    }
  }
</script>
<style scoped>
  #head{
    display: flex;
    /*justify-content: center;*/  /*垂直水平居中*/
    align-items:center;
    height:60px;
  }
  #head img{
    height:35px;
    width:35px;
    border-radius: 50%;
    margin-left: 10px;
    margin-right: 15px;
    /*box-shadow: 2px 2px 3px #444444;*/ /*阴影*/
    /*border:3px solid rgba(159, 186, 226, 0.64);*/  /*边框*/
    opacity: 0.9; /*透明度*/
  }
  #head .nickname{
    font-size: 14px;
  }
  #footer{
    margin-left: 10px;
    margin-right: 10px;
    height:50px;
    display: flex;
    /*justify-content: center;*/  /*垂直水平居中*/
    align-items:center;
    border-bottom:1px dotted rgba(162, 156, 156, 0.5);
  }
  #footer .tagheader{
    color: #D3D3D3;
    font-size: 15px;
  }
  #footer .tag{
    margin-left: 10px;
    color: #D3D3D3;
    font-size: 12px;
  }
  #sign{
    height:30px;
    border-bottom: solid 12px rgb(232, 232, 232);
    display: flex;
    /*justify-content: center;*/  /*垂直水平居中*/
    align-items:center;
  }
  #sign img{
    width:20px;
    height: 20px;
    margin-left: 10px;
  }

  img{
    width: 100%;
    /*border-radius: 50%;*/ /*圆形头像框*/
  }
</style>
