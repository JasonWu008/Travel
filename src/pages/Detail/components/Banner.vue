<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1602/45/459bd3d00321a44790.water.jpg_600x330_81c878a2.jpg">
      <div class="banner-info">
        <div class="banner-title">景山公园（AAAA景区）</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe634;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
        :imgs="bannerImgs"
        v-if="showGallary"
        @close="handleGallaryClose"
      ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'Banner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      bannerImgs: ['http://img1.qunarzz.com/sight/p0/1602/45/459bd3d00321a44790.water.jpg_600x330_81c878a2.jpg', 'http://img1.qunarzz.com/sight/p0/1909/a7/a7f107630d794c8a3.img.jpg_350x240_a7898b34.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
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
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
