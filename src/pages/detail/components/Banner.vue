<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_600x330_8572a930.jpg" />
      <div class="banner-info">
          <div class="banner-title">上海迪士尼乐园</div>
          <div class="banner-number"><span class='iconfont banner-icon'>&#xe628;</span>93</div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1905/ba/ba56de7b77bab2a5a3.img.jpg_r_800x800_daf85203.jpg', 'http://img1.qunarzz.com/sight/p0/1905/2a/2abf1aea5eecc2f6a3.img.jpg_r_800x800_52ca584c.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
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
        font-size: .36rem
        padding: 0 .2rem .2rem .2rem
      .banner-number
        margin-top: .1rem
        height: .4rem
        width: 1rem
        padding: 0 .2rem
        line-height: .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .5)
        font-size: .24rem
        color: #fff
        text-align: center
        .banner-icon
          padding-right: .15rem
          font-size: .24rem
</style>
