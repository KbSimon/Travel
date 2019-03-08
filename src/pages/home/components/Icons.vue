<template>
   <div class="icons">
       <div
         class="icon"
         v-for="item of list"
          :key="item.id"
       >
           <div class="icon-img">
             <img class="icon-img-content" :src="item.imgUrl">
             <p class="icon-desc">{{item.desc}}</p>
           </div>
       </div>
   </div>
</template>

<script>

export default {
  name: 'HomeIcons',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import  '~styles/varibles.styl'
  @import  '~styles/mixins.styl';
  .icons
    height: 0
    margin-top .1rem
    padding-bottom 50%
    overflow hidden
    .icon
      width 25%
      height 0
      float left
      position: relative
      padding-bottom 25%
      background #fff
      overflow hidden
      .icon-img
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        position: absolute
        .icon-img-content
          height 100%
          display block
          margin 0 auto
      .icon-desc
        text-align center
        bottom 0
        left 0
        right 0
        height .44rem
        line-height .44rem
        color $darkTextColor
        ellipsis()
</style>
