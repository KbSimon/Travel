<template>
   <div>
      <div class="recommend-title">周末去哪</div>
      <ul>
          <li
            class="item border-bottom"
            v-for="item of list"
            :key="item.id"
          >
              <div class="item-img-wrapper">
                  <img :src="item.imgUrl" class="item-img">
              </div>
              <div class="item-info">
                  <p class="item-title">{{item.title}}</p>
                  <p class="item-desc">{{item.desc}}</p>
              </div>
          </li>
      </ul>
   </div>
</template>

<script>

export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import  '~styles/mixins.styl';
  .recommend-title
    line-height 0.8rem
    background #ccc
    text-indent .2rem
  .item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 37.09%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
       line-height 0.4rem
       color #ccc
       ellipsis()
</style>
