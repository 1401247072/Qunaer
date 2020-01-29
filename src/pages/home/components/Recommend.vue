<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <router-link tag="li" :to="'/detail/' + item.id" class="item border-bottom" v-for="item of list" :key="item.id">
                <img class="item-img" :src="item.imgUrl" />
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <div class="item-price">
                        <span class="itemg-price">￥<em class="item-num">{{item.price}}</em>
                        </span>起</div>
                </div>
            </router-link>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
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
    height: 2.0rem
    padding-top: .2rem
    padding-bottom: .2rem
    .item-img
      width: 2rem
      height: 100%
    .item-info
      flex: 1
      padding-left: .22rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        color: #212121
        ellipsis()
      .item-desc
        font-size: .24rem
        line-height: .4rem
        color: #616161
        ellipsis()
      .item-price
        //padding: 0 .2rem
        margin-top: .4rem
        .itemg-price
          font-size: .24rem
          line-height: .4rem
          color: #ff8300
          .item-num
            font-size: .4rem
</style>
