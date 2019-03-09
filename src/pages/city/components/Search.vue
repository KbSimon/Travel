 <template>
    <div class="search">
      <input type="text" class="search-input" placeholder="输入城市名或拼音">
    </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .search
    height 0.72rem
    background $bgColor
    padding 0 .1rem
    .search-input
      height .62rem
      width 100%
      color #666
      box-sizing border-box
      padding 0 .1rem
      line-height 0.62rem
      text-align center
      border-radius .06rem
</style>
