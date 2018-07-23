<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe627;</span>
      输入城市/景点/游戏主题
    </div>
    <div class="header-right">
      <span class="iconfont arrow-icon">&#xe65e;</span>
      城市
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: 0.86rem
    background: $bgColor
    color: #fff
    .header-left
      .back-icon
        text-align: center
        font-size: 0.4rem
      width: 0.64rem
      float: left
    .header-input
      flex: 1
      height: 0.64rem
      line-height: 0.64rem
      margin-top: 0.12rem
      margin-left: 0.2rem
      background: #fff
      padding-left: 0.2rem
      border-radius: 0.1rem
      color: #ccc
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .arrow-icon
        margin-left: -0.04rem
        font-size: .24rem
</style>
