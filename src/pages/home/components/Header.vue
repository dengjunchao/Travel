<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont arrow-icon" >&#xe6aa;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped >
  @import "~styles/varbles.styl"
  .header
    display: flex
    line-height: .86rem
    background :$bgColor
    color:#fff
    .header-left
      width: .64rem
      float: left
      text-align: center
    .header-input
      flex: 1
      line-height :.64rem
      height: .64rem
      margin-top :.12rem
      margin-left :.2rem
      background : #fff
      border-radius :.1rem
      padding-left :.2rem
      color:#ccc
    .header-right
      width :1.24rem
      float :right
      text-align :center
      .arrow-icon
        font-size :.24rem
</style>
