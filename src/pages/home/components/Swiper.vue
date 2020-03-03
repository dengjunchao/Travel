<template>
  <div class="wrapper">
    <swiper :options="swiperOption"  v-if="showSwiper">
      <!-- slides -->
      <swiper-slide v-for="item of list" :key="item.id">
        <img class='swpier-img' :src="item.imgUrl">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  //数据穿透 设置样式白色
  .wrapper >>> .swiper-pagination-bullet-active
    background : #fff
  .wrapper
    width: 100%
    height: 150px
    .swpier-img
      width: 100%
      height: 150px
</style>
