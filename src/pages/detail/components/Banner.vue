<template>
  <div>
    <div class="banner" @click="handleBannerClick">
    <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1410/23/8492f586c3c1551cab635ccb25a4921f.jpg_600x330_32ef0c0e.jpg" />
    <div class="banner-info">
      <div class="banner-title">
        大连圣亚海洋世界(AAAA景区)
      </div>
      <div class="banner-number">
        <span class="iconfont banner-icon">&#xe64b;</span>
        39
      </div>
    </div>
    </div>
    <common-gallery
      :imgs="imgs"
      v-show="showGallery"
      @close="handleGalleryClose"
    ></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201401/08/445d158d7b1c60356638bc1dd9c58387.jpg_r_800x800_c7995321.jpg',
        'http://img1.qunarzz.com/sight/p0/201401/08/a19ab4e7b5c88fc4acd67a6aa39a78d6.jpg_r_800x800_d146da0f.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  },
  components: {
    CommonGallery
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        line-height: .32rem
        border-radius: .2rem
        background: rgba(0,0,0,.8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
