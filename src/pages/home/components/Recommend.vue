<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img"
               :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomerRecommend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1511/be/be92297f68b40be390.water.jpg_200x200_6e04dcf5.jpg',
        title: '莲花山温泉度假村',
        desc: '“泉”来了！花草泉、灵芝泉、艾草泉、超音波喷射泉'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1512/62/628c1e85c1d00e3590.water.jpg_200x200_cf118541.jpg',
        title: '汕头丹樱生态园',
        desc: '丹樱生态旅游区拥有得天独厚的自然景观，清澈的湖水、层层叠叠的岩石。生态旅游区的地理位置优越，离汕头只有十分钟的车程。通过引进各种先进的高科技技术，大力发展高科技农业、环保农业、园林农业、观赏农业，致力于打造成为粤东地区乃至全国知名的“可复制式”的原生态旅游观光区。随着生态旅游区销售网络的不断发展，把各式各样具有本土特色的蔬果品种直销全国各个地区，使其农业不断走向网络化、专业化、多元化，成为中国农业发展新模式，让人耳目一新。旅游区内环境质量高，自然风光优美，所有景观设施项目采用开放式建筑设计，具有浓厚的异国风情。旅游区内规划了观赏性农作物区、花海区、温棚科普教育区、桃花谷、湿地公园区、茶园、潮汕文化长廊、潮汕特色农家菜式区、垂钓区、荔枝园、潮汕文化中心、情人桥、码头、环湖自行车道、拓展及娱乐休闲区。'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/3b/3b0a34d3984b4ac590.water.jpg_200x200_4fa25893.jpg',
        title: '南澳岛',
        desc: '这里有细软的海滩、温柔的海浪、丰富的资源、悠久的历史…'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 2.1rem
    .item-img
       margin-top: .1rem
       width: 2rem
       height: 2rem
       padding: .1rem
    .item-info
       flex: 1
       padding:.1rem
       min-width: 0
       .item-title
         line-height: .54rem
         font-size: .32rem
         ellipsis()
       .item-desc
         line-height: .4rem
         color: #333
         ellipsis()
       .item-button
          line-height: .44rem
          margin-top: .16rem
          background: #ff9300
          padding: 0 .2rem
          border-radius: .06rem
          color: #fff
</style>
