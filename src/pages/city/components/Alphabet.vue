<template>
  <ul class="list">
    <li class="item" v-for="(item, key) of cities" :key="key">{{key}}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/variable.styl"
  .list
    position: absolute
    display: flex
    flex-direction: column
    justify-content: center
    top: 1.78rem
    right: 0
    bottom: 0
    width: .4rem
    .item
      line-height: .42rem
      text-align: center
      color: $bgColor
</style>
