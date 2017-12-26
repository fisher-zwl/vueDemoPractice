<template>
  <div>
    <myHeader></myHeader>
    <div class="content">
      <div class="contenter">
        <my-search></my-search>
        <div class="pic-carousel">
          <template>
            <el-carousel :interval="2000" type="card" height="200px">
              <el-carousel-item v-for="item in 6" :key="item">
                <h3>{{ item }}</h3>
              </el-carousel-item>
            </el-carousel>
          </template>
        </div>
        <div class="selected-topics">
          <div  class="selected-topics-title oneTitle"><span>精选专题</span></div>
          <div class="selected-topics-twoTitle twoTitle"><span>给你创意和灵感，满足所有设计师的创作需求</span></div>
          <div>
            <ul class="selected-topics-pic">
              <li class="head">
                <a title="元旦快乐" href="#" target="_blank" class="head-img"><img src="/static/image/yuandan.png"/></a>
                <a href="javascript:void(0);" class="head-title">元旦快乐</a>
              </li>
              <li>
                <a title="元旦快乐" href="#" target="_blank" class="head-img"><img src="/static/image/yuandan.png"/></a>
                <a href="javascript:void(0);" class="head-title">元旦快乐</a>
              </li>
              <li>
                <a title="元旦快乐" href="#" target="_blank" class="head-img"><img src="/static/image/yuandan.png"/></a>
                <a href="javascript:void(0);" class="head-title">元旦快乐</a>
              </li>
              <li>
                <a title="元旦快乐" href="#" target="_blank" class="head-img"><img src="/static/image/yuandan.png"/></a>
                <a href="javascript:void(0);" class="head-title">元旦快乐</a>
              </li>
            </ul>
            <div class="classify-more"><p><span><a href="#" target="_blank">查看更多</a></span></p></div>
          </div>
        </div>
        <div class="pic-topics">
          <div class="oneTitle"><span>照片精选</span></div>
          <div class="twoTitle"><span>从我们的优质照片中找到你的灵感</span></div>
          <div>
            <ul>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
            </ul>
            <ul>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
            </ul>
            <ul>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
            </ul>
          </div>
        </div>
        <div class="illustration-topics">
          <div class="oneTitle"><span>插画精选</span></div>
          <div class="twoTitle"><span>有些画，我们只动了手，而你却动了心</span></div>
          <div></div>
        </div>
        <div class="vedio-topics">
          <div class="oneTitle"><span>视频精选</span></div>
          <div class="twoTitle"><span>优质视频音效 极致通用</span></div>
          <div></div>
        </div>
      </div>
    </div>
    <myFooter></myFooter>
  </div>
</template>
<script>
import myHeader from '../components/header/header.vue'
import myFooter from '../components/footer/footer.vue'
import mySearch from '../components/search/searchSS.vue'
export default {
  components: { myHeader, myFooter, mySearch },
  data () {
    return {
    }
  },
  created () {
  },
  methods: {
    getData () {
    }
  }
}
</script>
<style lang="scss" scoped>
  .content{
    width: 100%;
  }
  .contenter{
      max-width: 1200px;
      min-width: 1000px;
      height: 60px;
      margin: 0px auto;

    .pic-carousel{
      margin-top: 20px;
    }

    .oneTitle{
      margin-bottom: 10px;
      text-align: center;

      span{
        font-size: 28px;
        color: #666666;
      }
    } 

    .twoTitle{
      text-align: center;
      margin-bottom: 21px;

      span{
        font-size: 14px;
        color: #999999;
      }
    } 

    .selected-topics{
      margin-top: 40px;

      .selected-topics-pic{
        margin-right: -20px;
        height: 168px;
        margin-bottom: 20px;
        li{
          float: left;
          width: 285px;
          height: 168px;
          margin-right: 20px;
          position: relative;
          overflow: hidden;

          .head-img{
            width: 285px;
            height: 168px;

            img{
              width: 100%;
              height: 100%;
            }
          }

          .head-title{
            width: 100%;
            position: absolute;
            left: 0;
            bottom: 0;
            height: 40px;
            line-height: 40px;
            font-size: 18px;
            color: #FFFFFF;
            text-align: center;
            letter-spacing: 1.14px;
            background: rgba(0,0,0,0.3);
          }
        }
      }
    }

    .pic-topics{
      margin-top: 40px;
    }

    .illustration-topics{
      margin-top: 40px;
    }

    .vedio-topics{
      margin-top: 40px;
    }

    .classify-more{
      height: 70px;
      box-sizing: border-box;
      text-align: center;
      padding-top: 20px;
      p{
        display: inline-block;
        width: 1000px;
        border-top: 1px solid #EEEFF2;
        height: 0;
        span{
          display: inline-block;
          padding: 0 31px;
          background: #fff;
          position: relative;
          top: -11px;
          a{
            font-size: 14px;
            color: #666666;
            padding: 20px;
          }
        }
      }
    }
  }
  // *********************图片轮播样式**********************
  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
  }
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
  // *********************图片轮播样式结束**********************
</style>

