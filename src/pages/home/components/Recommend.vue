<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <router-link
        tag="li"
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
        :to="'/detail/' + item.id"
      >
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      list: [
        {
          id: '1',
          imgUrl: 'http://imgs.qunarzz.com/p/tts7/1703/5c/7a23eb2a744cce02.jpg_r_480x320x90_36341f62.jpg',
          title: '武汉-迪拜 6天跟团游',
          desc: '林肯加长豪车游迪拜7日|冲沙|棕榈岛列车观光|五星酒店|水上的士|帆船酒店'
        },
        {
          id: '2',
          imgUrl: 'http://imgs.qunarzz.com/p/tts2/1811/2e/d7c7b4b78f58b002.jpg_r_480x320x90_cfd83461.jpg',
          title: '武汉-芭堤雅 6天跟团游',
          desc: '泰国曼谷+芭堤雅6天5晚跟团游·真0自费·宿3晚钻五·泰按摩·赠888大礼包'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
