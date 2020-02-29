<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
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
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1802/40/40b2075640718d7a3.img.png_600x330_11cd3f65.png'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/86/86d65748c963998fa3.water.jpg_600x330_546ce88a.jpg'
      }]
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
