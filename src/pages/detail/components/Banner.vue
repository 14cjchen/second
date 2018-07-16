<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img"
           src="//img1.qunarzz.com/sight/p0/1511/be/be92297f68b40be390.water.jpg_600x330_cf40e757.jpg"/>
      <div class="banner-info">
        <div class="banner-title">莲花山温泉度假村</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe692; </span>39</div>
      </div>
    </div>
    <common-gallery :imgs="imgs" v-show="GalleryShow" @close="handleGalleryClose"></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'Detail',
  components: {
    CommonGallery
  },
  data () {
    return {
      GalleryShow: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1507/b1/bcc9a2ba77f88f6486fe923a05d734b8.water.jpg_r_800x800_644b2c89.jpg',
        'http://img1.qunarzz.com/sight/p0/1507/b4/905d547af265048effa3c99ce6cc1901.water.jpg_r_800x800_38ca712c.jpg']
    }
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
