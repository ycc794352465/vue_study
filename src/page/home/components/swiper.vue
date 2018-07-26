<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/vc/b8/dc/e9/464bc1e47e99d8a308a6e24817.jpg'
      },
      {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/vc/cc/65/94/c5830be6e372c05248a2a5a139.jpg'
      },
      {
        id: '0003',
        imgUrl: 'https://img1.qunarzz.com/vc/cc/65/94/c5830be6e372c05248a2a5a139.jpg'
      },
      {
        id: '0004',
        imgUrl: 'https://img1.qunarzz.com/vc/b8/dc/e9/464bc1e47e99d8a308a6e24817.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff !important;
}

.wrapper {
  width: 100%;
  height: 0;
  background: #eee;
  overflow: hidden;
  padding-bottom: 31.25%;

  .swiper-img {
    width: 100%;
  }
}
</style>
