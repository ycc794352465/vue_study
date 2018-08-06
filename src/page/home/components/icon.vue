<template>
  <div class="icon">
    <swiper>
      <swiper-slide :options="swiperOption" v-for="(page, index) in pages" :key="index">
        <div  v-for="item in page" :key="item.id" class="icon_list">
          <img :src="item.src" alt="">
          <p>{{ item.content }}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcon',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: false
      },
      iconList: [{
        id: '001',
        content: '景点门票',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
      },
      {
        id: '002',
        content: '水上乐园',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png  '
      },
      {
        id: '003',
        content: '游乐场',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png'
      },
      {
        id: '004',
        content: '海洋馆',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png'
      },
      {
        id: '005',
        content: '动植物园',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png'
      },
      {
        id: '006',
        content: '玩转深圳',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png'
      },
      {
        id: '007',
        content: '城市观光',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png'
      },
      {
        id: '008',
        content: '海滨沙滩',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/27/dac2bcf9added702.png'
      },
      {
        id: '009',
        content: '玩转深圳',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png'
      },
      {
        id: '010',
        content: '城市观光',
        src: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icon_list
    float: left
    width: 25%
    img
      width: 60%
      margin: 30px auto 5px
      display: block
    p
      text-align: center
      color: $fontColor
      font-size: 0.16rem
      ellipsis()
</style>
