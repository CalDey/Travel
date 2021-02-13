<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
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
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://imgs.qunarzz.com/vs_ceph_vcimg/6ff121fd416169b8d56c60384e3baf79.jpeg'
      },
      {
        id: '0002',
        imgUrl: 'http://imgs.qunarzz.com/vs_ceph_vcimg/f7813c9431796cc32ae7b7a78447342e.jpeg'
      },
      {
        id: '0003',
        imgUrl: 'http://imgs.qunarzz.com/vs_ceph_vcimg/f03f5ac90ae59d0d9c6332a2bfd9782e.jpeg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  // >>> 样式穿透
  .wrapper >>> .swiper-pagination-bullet-active
      background: #fff !important
  .wrapper
    width: 100%
    // height: 31.25vm
    height: 0
    overflow: hidden
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
      width: 100%
</style>
