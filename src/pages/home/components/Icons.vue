<template>
   <div class="icons">
       <div
         class="icon"
         v-for="item of iconList"
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
  data () {
    return {
      iconList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        desc: '名胜古迹'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/f5/a963333e1fa802.png',
        desc: '本地玩乐'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        desc: '亲子游'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
        desc: '全部玩乐'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import  '~styles/varibles.styl'
  @import  '~styles/mixins.styl';
  .icons
    height: 0
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
