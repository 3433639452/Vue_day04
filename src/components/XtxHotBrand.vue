<template>
<!-- 结构 -->
  <!-- 热门品牌 -->
    <div class="hot">
      <div class="wrapper">
        <div class="title">
          <div class="left">
            <h3>热门品牌</h3>
            <p>国际经典 品质认证</p>
          </div>
          <div class="button">
            <a href="#"><i class="iconfont icon-arrow-left-bold"></i></a>
            <a href="#"><i class="iconfont icon-arrow-right-bold"></i></a>
          </div>
        </div>
        <div class="bd">
          <ul>
            <BaseBrandItem v-for="item in 5" :key="item"></BaseBrandItem>
          </ul>
        </div>
      </div>
    </div>
</template>

<script>
// 逻辑
import BaseBrandItem from './BaseBrandItem.vue';
export default {
  components:{
    BaseBrandItem
  }
}
</script>

<style scoped>
/* 样式 */

</style>