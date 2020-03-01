<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.url" />
      </swiper-slide>

      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  // props: {
  //   list: Array
  // },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '1',
          url: 'https://pics.lvjs.com.cn/pics/super/2020/02/1581762603_85902.jpg'
        },
        {
          id: '2',
          url: 'https://pics.lvjs.com.cn/pics/super/2020/02/1581607657_41736.jpg'
        }
      ]
    }
  }
  // computed: {
  //   showSwiper () {
  //     return this.list.length
  //   }
  // }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
      width: 100%
</style>
