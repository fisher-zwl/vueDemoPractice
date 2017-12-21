<template>
  <div class="search">
      <div class="search-input">
        <input type="text" class="search-input-ipt"/>
      </div>
      <div class="search-select">
        <el-dropdown>
          <span class="el-dropdown-link">
            下拉菜单<i class="el-icon-arrow-down el-icon--right"></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>黄金糕</el-dropdown-item>
            <el-dropdown-item>狮子头</el-dropdown-item>
            <el-dropdown-item>螺蛳粉</el-dropdown-item>
            <el-dropdown-item disabled>双皮奶</el-dropdown-item>
            <el-dropdown-item divided>蚵仔煎</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
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
    }
  }
</script>
<style lang="scss" scoped>
    .search{
      height: 50px;
      margin-top: 20px;
      position: relative;

      .search-input{
        border:1px solid #f1f1f1;
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
        border:1px solid #f1f1f1;
        border-left: none;
        border-right: none;
      }

      .search-btn{
        display:inline-block;
        position: absolute;
        right: 0px;
        width: 150px;
        height: 50px;
      }
    }
</style>