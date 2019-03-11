<template>
  <div>
    <div
      class="banner"
      @click="handleBannerClick"
    >
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">故宫(AAAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;39</span>
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGrallyClose"
     >
     </common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: [
        'http://img1.qunarzz.com/wugc/p123/201211/19/a2045d091f02b25493835fbb.png_r_800x800_c59f0eba.png'
      ]
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGrallyClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      position absolute
      left 0
      right 0
      bottom 0
      color #fff
      line-height 0.6rem
      display flex
      background-image linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.08))
      .banner-title
        flex 1
        font-size 0.32rem
        padding 0 .2rem
      .banner-number
        margin-top  .14rem
        padding 0 .4rem
        line-height 0.32rem
        height 0.32rem
        border-radius .2rem
        font-size 0.24rem
        background rgba(0,0,0,.8)
        .banner-icon
          font-size 0.24rem
</style>
