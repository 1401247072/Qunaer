<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" />
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      weekendList: [{
        id: '001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1511/ea/7f43191b747bb9.jpg_r_640x214_f58e829d.jpg',
        title: '上海泡汤圣地',
        desc: '上海的朋友总会问，哪里可以泡温泉，哪里的温泉...'
      }, {
        id: '002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海必打卡',
        desc: '中西合璧，现代和传统各有各的精彩'
      }, {
        id: '003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/7b/2a6b0ce087f0e5.jpg_r_640x214_5c76b115.jpg',
        title: '情迷博物馆',
        desc: '走进艺术殿堂，电影博物馆生动演绎着电影人和电...'
      }, {
        id: '004',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1603/ad/69b0fc5f48ad5f.jpg_r_640x214_b0fd5c7b.jpg',
        title: '周末亲子乐园',
        desc: '走进自然或玩转乐园，感知大千世界，游乐项目惊...'
      }, {
        id: '005',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1511/1d/fe098e8cfec117.jpg_r_640x214_a9be292a.jpg',
        title: '上海城市观光',
        desc: '来这里寻找你所不认识的魔都，感受云端漫步，品...'
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 38%
    .item-img
      width: 100%
  .item-info
    padding: .14rem .2rem .2rem .2rem
  .item-title
    line-height: .48rem
    font-size: .28rem
    color: #212121
    ellipsis()
  .item-desc
    font-size: .24rem
    line-height: .42rem
    color: #616161
    ellipsis()
</style>
