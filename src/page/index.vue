<template>
  <div>
    <myHeader></myHeader>
    <div class="content">
      <div class="contenter">
        <my-search></my-search>
      </div>
    </div>
    <myFooter></myFooter>
  </div>
</template>
<script>
import myHeader from '../components/header/header.vue'
import myFooter from '../components/footer/footer.vue'
import mySearch from '../components/search/search.vue'
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
  }
</style>

