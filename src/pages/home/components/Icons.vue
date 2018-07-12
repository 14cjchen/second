<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src='item.imgUrl'/>
          </div>
          <p class="icons-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '热门景点'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/27/dac2bcf9added702.png',
        desc: '美食'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
        desc: '游乐场'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png',
        desc: '玩转长隆'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
        desc: '全部玩乐'
      }, {
        id: '006',
        imgUrl: 'https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png',
        desc: '天猫'
      }, {
        id: '007',
        imgUrl: 'https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png',
        desc: '聚划算'
      }, {
        id: '008',
        imgUrl: 'https://gw.alicdn.com/tfs/TB163FbPVXXXXcKXXXXXXXXXXXX-183-144.png',
        desc: '天猫国际'
      }, {
        id: '009',
        imgUrl: 'https://gw.alicdn.com/tps/TB1eXc7PFXXXXb4XpXXXXXXXXXX-183-144.png',
        desc: '外卖'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  @import '~styles/mixins.styl'
.icons >>> .swiper-container
  height: 0
  padding-bottom: 50%
.icon
  position: relative
  overflow: hidden
  float: left
  width: 25%
  height: 0
  padding-bottom: 25%
  .icon-img
   position: absolute
   top: 0
   left: 0
   right: 0
   bottom: .44rem
   box-sizing:border-box
   padding:.1rem
   .icon-img-content
    display:block
    margin: 0 auto
    height: 100%
  .icons-desc
   position: absolute
   left: 0
   right: 0
   bottom: 0
   height: .44rem
   line-height: .44rem
   text-align: center
   color:darkText
   ellipsis()
</style>
