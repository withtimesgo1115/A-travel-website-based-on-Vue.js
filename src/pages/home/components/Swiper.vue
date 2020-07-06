<template>
<div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
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
        imgUrl: '//img1.qunarzz.com/sight/p0/1508/80/29eaf59b380bef97acacba8a8f6efd2a.water.jpg_600x330_76f8cfee.jpg'
      }, {
        id: '0002', imgUrl: '//img1.qunarzz.com/sight/p0/1507/d4/f8ac1f83c6911b40f31ee560e8ab5a1b.water.jpg_600x330_55810851.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 55.5%
    background: #eee
    .swiper-img
      width: 100%
</style>
