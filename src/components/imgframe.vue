<template>
  <div>
    <div id="head">
      <img src="../img/head.jpg" alt="">
      <span>Mynickname</span></div>
    <img :src="img" alt="">
    <div id="footer">
      <span># {{label}}留言</span></div>
    <div id="sign">
      <img src="../img/icon/good.svg" alt="">
      </div>
  </div>

</template>
<script>
  export default {
    props:['img','label'],
    methods:{
    }
  }
</script>
<style scoped>
  #head{
    display: flex;
    /*justify-content: center;*/  /*垂直水平居中*/
    align-items:center;
    height:55px;
  }
  #head img{
    height:40px;
    width:40px;
    border-radius: 50%;
    margin-left: 10px;
    margin-right: 10px;
    box-shadow: 2px 2px 3px #444444;
    border:3px solid rgba(159, 186, 226, 0.64);
    opacity: 0.9; /*透明度*/
  }
  #footer{
    height:50px;
    display: flex;
    /*justify-content: center;*/  /*垂直水平居中*/
    align-items:center;
    border-bottom:1px dashed rgba(83, 77, 77, 0.5);
  }
  #footer span{
    margin-left: 5px;
  }
  #sign{
    height:30px;
    border-bottom: solid 12px rgba(216, 210, 210, 0.5);
    display: flex;
    /*justify-content: center;*/  /*垂直水平居中*/
    align-items:center;
  }
  #sign img{
    width:20px;
    height: 20px;
    margin-left: 5px;
  }

  img{
    width: 100%;
    /*border-radius: 50%;*/ /*圆形头像框*/
  }
</style>
