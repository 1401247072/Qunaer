<template>
  <div>
    <div class="item" v-for="(item, index) of list" :key="index">
      <div class="item-title border-bottom" @click="handleItemClick(index)">
        <span class="item-title-icon"></span>
        {{item.title}}
      </div>
      <div v-show="nowIndex===index" class="item-child">
        <detail-list :list="item.child"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  },
  data () {
    return {
      nowIndex: -1
    }
  },
  methods: {
    handleItemClick (index) {
      if (this.nowIndex < 0) {
        this.nowIndex = index
      } else {
        this.nowIndex = -1
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .item-title-icon
    position: relative
    left: .1rem
    top: .08rem
    display: inline-block
    width: .36rem
    height: .36rem
    background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
    margin-right: .1rem
    background-size: .4rem 3rem
  .item-title
    line-height: .8rem
    font-size: .32rem
    padding: 0 .1rem
  .item-child
    padding: 0 .15rem
</style>
