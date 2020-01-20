<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
    <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>
        <!-- Optional controls -->
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
        id: '001',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/7b45da191f638f13455777030853a1ea.jpg_750x200_883fe3a8.jpg'
      }, {
        id: '002',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/071210d83e8ab09d363446166db5d34e.jpg_750x200_41285396.jpg'
      }, {
        id: '003',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/9c4bd16baa22bcd6810b714b225b5c33.jpg_750x200_95d6ad38.jpg'
      }, {
        id: '004',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/1586638277619f1041ebd03877cfccee.jpg_750x200_8db6a58a.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
    .wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 26.75%
        background: #eee
        //height: 26.8vm(兼容不好)
      .swiper-img
          width: 100%
</style>
