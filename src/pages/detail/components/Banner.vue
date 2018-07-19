<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img"
           :src="bannerImg"/>
      <div class="banner-info">
        <div class="banner-title">{{sightName}}</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe692; </span>{{this.gallaryImgs.length}}</div>
      </div>
    </div>
    <common-gallery :imgs="gallaryImgs" v-show="GalleryShow" @close="handleGalleryClose"></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallery
  },
  props: {
    bannerImg: String,
    gallaryImgs: Array,
    sightName: String
  },
  data () {
    return {
      GalleryShow: false}
  },
  methods: {
    handleBannerClick () {
      this.GalleryShow = true
    },
    handleGalleryClose () {
      this.GalleryShow = false
    }
  }
}
</script>

<style lang="stylus" scoped>
 .banner
   overflow: hidden
   height: 0
   padding-bottom: 55%
   position: relative
   .banner-img
     width: 100%
   .banner-info
     display: flex
     position: absolute
     left: 0
     right: 0
     bottom: 0
     line-height: .8rem
     color: #fff
     background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
     .banner-title
       flex: 1
       font-size: .4rem
       padding: .2rem .2rem
     .banner-number
       height: .38rem
       line-height: .38rem
       margin-top: .4rem
       margin-right: .2rem
       padding: 0 .4rem
       border-radius: .2rem
       background: rgba(0, 0, 0, .8)
       font-size: .24rem
       .banner-icon
         font-size: .24rem
</style>
