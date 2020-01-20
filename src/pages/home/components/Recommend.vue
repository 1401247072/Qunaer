<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img" :src="item.imgUrl" />
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <div class="item-price">
                        <span class="itemg-price">￥<em class="item-num">{{item.price}}</em>
                        </span>起</div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        desc: '🔥全球最大的迪士尼城堡',
        price: '399'
      }, {
        id: '002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/2001/f6/f66fb64d494a4d78a3.img.jpg_200x200_005ebaf5.jpg',
        title: '上海海昌海洋公园',
        desc: '精彩纷呈的海洋梦幻之旅',
        price: '179'
      }, {
        id: '003',
        imgUrl: 'https://imgs.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg',
        title: '东方明珠',
        desc: '259米透明悬空观光廊了解一下~',
        price: '75'
      }, {
        id: '004',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1912/e3/e34a3084c05532cca3.img.jpg_200x200_ecbe41c5.jpg',
        title: '上海野生动物园',
        desc: '会跳芭蕾舞的小海狮们~',
        price: '119.4'
      }, {
        id: '005',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1811/e4/e4b9b471d2afc473a3.img.jpg_200x200_9a7794fc.jpg',
        title: '上海欢乐谷',
        desc: '全敢上1200米长的木质过山车吗？',
        price: '199'
      }, {
        id: '006',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1904/20/20dd895e78548b50a3.img.jpg_200x200_348c3831.jpg',
        title: '上海长风海洋世界',
        desc: '和奥莉一起看魔鬼鱼啦',
        price: '139'
      }, {
        id: '007',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1502/ba/ba5f873a22327e0f.water.jpg_200x200_9bf5cc14.jpg',
        title: '上海影视乐园',
        desc: '真实艺术地展现上海的历史风貌和人文景观',
        price: '64.7'
      }, {
        id: '008',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1411/4f/146031f0bc5d7e0dd960d3f5bf0c9eca.water.jpg_200x200_f22705c9.jpg',
        title: '上海科技馆',
        desc: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)',
        price: '49'
      }, {
        id: '009',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1506/16/f05ab7bbcbdf7b7fdee652843ebba2db.water.jpg_200x200_abc1efd6.jpg',
        title: '东平国家森林公园',
        desc: '在这里，你只需要深呼吸',
        price: '39.4'
      }, {
        id: '010',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1802/d3/d345e53fdc97849ba3.img.jpg_200x200_c00f5662.jpg',
        title: '安徒生童话乐园',
        desc: '把握安徒生主题，深入结合童话特质',
        price: '162'
      }, {
        id: '011',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1603/30/30a1bb5ff6a1960c90.water.jpg_200x200_d5cb85c9.jpg',
        title: '朱家角古镇',
        desc: '素有"上海威尼斯"及"沪郊好莱坞"之誉',
        price: '25'
      }, {
        id: '012',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1507/b3/b33a7caa457c0a52.img.jpg_200x200_fe73bd81.jpg',
        title: '东方明珠空中旋转餐厅',
        desc: '🔥好评如潮，小伙伴热推景点~',
        price: '239'
      }]
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
