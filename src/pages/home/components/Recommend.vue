<template>
   <div>
      <div class="recommend-title">热销推荐</div>
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
                  <button class="item-button">查看详情</button>
              </div>
          </li>
      </ul>
   </div>
</template>

<script>

export default {
  name: 'HomeRecomend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import  '~styles/mixins.styl';
  .icons
  .recommend-title
    line-height 0.8rem
    background #ccc
    margin-top 0.2rem
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      min-width 0
      padding .1rem
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height 0.4rem
        color #ccc
        ellipsis()
      .item-button
        background #ff9300
        padding 0 .2rem
        line-height 0.44rem
        border-radius .06rem
        color #fff
        margin-top .16rem
</style>
