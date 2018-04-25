<template>
  <div>
    <div :style="background" class="div" @click="propData">
      {{label}}
    </div>
  </div>
</template>


<script>
  export default {
    props:['background','label'],
    methods:{
      propData(){
        this.$emit('setBackground', 'background:yellow')
      }
    }
  }
</script>
<style scoped>
  .div{
    width: 90px;
    height:90px;
    background: red;
  }
</style>
