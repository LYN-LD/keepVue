<template>
  <div id="app" style="margin: 0 auto;">
    <!--<img src="./assets/logo.png">-->
    <router-view/>
  </div>

</template>

<script>
  export default {
    name: 'App'
  }
</script>

<style lang="less">
  #app {
    /*设置背景图片*/
    position: absolute;
    right: 0;
    left: 0;
    top: 0;
    margin-left: 0!important;
    margin-right: 0!important;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0) url('./assets/bj.png') no-repeat scroll 50% 50%;
    /*background-size: auto;*/
    background-size: cover;
  }
</style>
