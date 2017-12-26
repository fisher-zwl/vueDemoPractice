<template>
  <div class="search">
      <div class="search-input">
        <input type="text" class="search-input-ipt"/>
      </div>
      <div class="search-select">
        <el-menu class="el-menu-demo" mode="horizontal" @select="handleSelect">
          <el-submenu index="1">
            <template slot="title">我的工作台</template>
            <el-menu-item index="1-1">选项1</el-menu-item>
            <el-menu-item index="1-2">选项2</el-menu-item>
            <el-menu-item index="1-3">选项3</el-menu-item>
          </el-submenu>
        </el-menu>
      </div>
      <input type="button" class="search-btn"/>
  </div>
</template>
<script>
  export default {
    data () {
      return {
      }
    },
    methods: {
      handleSelect (key, keyPath) {
        console.log(key, keyPath)
      }
    }
  }
</script>
<style lang="scss" scoped>
    .search{
      height: 50px;
      margin-top: 20px;
      position: relative;

      .search-input{
        border:1px solid #dcdcdc;
        display:inline-block;
        position: absolute;
        left: 0;
        right: 270px;
        height: 50px;

        .search-input-ipt{
          width: 96%;
          height: 100%;
          border:none;
          outline: none;
          margin-left: 20px;
        }
      }

      .search-select{
        display:inline-block;
        position: absolute;
        width: 120px;
        right: 150px;
        height: 50px;
        border:1px solid #dcdcdc;
        border-left: none;
        border-right: none;
      }
      .search-select /deep/ .el-submenu__title{
        height: 50px;
        line-height:50px;
      }
      .search-select /deep/ .el-menu--horizontal .el-submenu>.el-menu{
        top: 50px;
        width: 100px;
        border: 1px solid #dcdcdc;
      }

      .search-btn{
        display:inline-block;
        position: absolute;
        border:1px solid #dcdcdc;
        outline: none;
        right: 0px;
        width: 150px;
        height: 52px;
      }
    }
</style>