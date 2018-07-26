<template>
  <div class="icon">
    <div class="icon_list" v-for="item in iconList" :key="item.id">
      <img :src="item.src" alt="">
      <p>{{ item.content }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeIcon',
  data () {
    return {
      iconList: [{
        id: '001',
        content: '签证·WiFi',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      },
      {
        id: '002',
        content: '欢乐谷·游玩',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      },
      {
        id: '003',
        content: '吃喝玩乐',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      },
      {
        id: '004',
        content: '来看看',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      },
      {
        id: '005',
        content: '机票·火车票',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      },
      {
        id: '006',
        content: '机票·火车票',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      },
      {
        id: '007',
        content: '签证·WiFi',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      },
      {
        id: '008',
        content: '机票·火车票',
        src: 'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=886685743,4109459620&fm=58'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .icon_list
    width: 25%
    float: left
    img
      width: 80%
      margin: 0 auto
      display: block
    p
      text-align: center
      color: $fontColor
      font-size: 0.16rem
</style>
