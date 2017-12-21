<template>
  <header class="header">
    <div class="header-menu">
      <div class="header-icon" v-on:click="shouye">
        <span class="image"></span>
        <span class="font">菜花网Saika</span>
      </div>
      <el-menu 
        :default-active="activeIndex" 
        class="el-menu-demo" 
        mode="horizontal" 
        @select="handleSelect" 
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b">
        <el-menu-item index="1">照片</el-menu-item>
        <el-submenu index="2" >
          <template slot="title" background-color="#fff">插画</template>
          <div>sddsdsds</div>
          <el-menu-item  index="2-1">选项1</el-menu-item>
        </el-submenu>
        <el-menu-item index="3">视频</el-menu-item>
        <el-menu-item index="4">摄影师</el-menu-item>
        <el-menu-item index="5">版权保证</el-menu-item>
        <el-menu-item index="6"><a href="https://www.ele.me" target="_blank">创意合成</a></el-menu-item>
        <el-menu-item index="7">矢量/模板</el-menu-item>
      </el-menu>
      <div class="login-enter">
        <button type="button">注册</button>
        <button type="button">登录</button>
      </div>
    </div>
  </header> 
</template>
<script>
  export default {
    data () {
      return {
        activeIndex: '1'
      }
    },
    methods: {
      handleSelect (key, keyPath) {
        console.log(key, keyPath)
      },
      shouye (event) {
        console.log(event)
      }
    }
  }
</script>
<style lang="scss" scoped>
  .header{
    background-color: #545c64;
  }
  .header-menu{
    max-width: 1200px;
    min-width: 1000px;
    height: 60px;
    margin:0px auto;

    .header-icon{
      display:inline-block;
      width: 200px;
      height: 60px;
      line-height: 60px;
      vertical-align: top;

      .image{
        display:inline-block;
        background-image: url(/static/image/header-icon.png);
        background-repeat: no-repeat;
        margin-top: 6px;
        height: 48px;
        width: 48px;
      }
      .font{
        display:inline-block;
        color:#fff;
        height: 60px;
        line-height: 60px;
        vertical-align: top;
        font-size: 20px;
        font-weight: bold;
      }
    }

    .el-menu-demo{
      display:inline-block;
    }

    .login-enter{
      display:inline-block;
      vertical-align: top;
      height: 60px;
      line-height: 60px;
      color:#fff;
      width:180px;
      float: right;

      button{
        width:70px;
        height: 30px;
        border-radius: 3px;
        line-height: 30px;
        margin-top: 15px;
        vertical-align: middle;
        border:1px solid #fff;
        color:#fff;
        background-color: #545c64;
        margin-left: 10px;
        float: right;
      }

      button:hover{
        background-color: #0095E5;
        border-color: #0095E5;
      }
    }
  }
</style>
