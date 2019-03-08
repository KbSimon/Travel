<template>
   <div>
      <div class="recommend-title">周末去哪</div>
      <ul>
          <li
            class="item border-bottom"
            v-for="item of recommendList"
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
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/52/b6776b49d27025.jpg_r_640x214_35ae205c.jpg',
        title: '美丽普陀山',
        desc: '人间仙境杭州，佛教圣地普陀山等你来玩！在这里静心接收佛家的洗礼，用心感受佛文化'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '杭州必打卡',
        desc: '杭州，前世今生与你有一场美丽约会'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
        title: '承载杭城的历史之地',
        desc: '饱经沧桑的地方诉述着这座城的段段衷肠'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1602/c1/48e295bdafbc88.jpg_r_640x214_3723c001.jpg',
        title: '花开正当时',
        desc: '阳春三月，恰是赏花好时节'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import  '~styles/mixins.styl';
  .recommend-title
    line-height 0.8rem
    background #ccc
    margin-top 0.2rem
    text-indent .2rem
  .item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 33.9%
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
