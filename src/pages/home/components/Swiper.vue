<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSiper">
       <swiper-slide v-for="item of list" :key="item.id">
        <img
          class="swiper-img"
          :src="item.imgUrl"
        >
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        loop: true,
        autoplay: 3000,
        pagination: '.swiper-pagination'
      }
    }
  },
  computed: {
    showSiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
   background: #fff !important
  .wrapper
    width: 100%
    height: 0
    padding-bottom: 31.25%
    overflow: hidden
    .swiper-img
      width: 100%;
</style>
