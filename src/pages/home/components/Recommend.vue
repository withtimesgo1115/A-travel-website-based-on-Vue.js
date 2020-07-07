<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <img class="item-img" :src='item.imgUrl' />
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
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
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/23/8492f586c3c1551cab635ccb25a4921f.jpg_200x200_4a7a209d.jpg',
        title: '罗浮山宝田养生温泉',
        desc: '浪漫惠州首战，浪漫的养生之旅'
      },
      {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/23/8492f586c3c1551cab635ccb25a4921f.jpg_200x200_4a7a209d.jpg',
        title: '罗浮山宝田养生温泉',
        desc: '浪漫惠州首战，浪漫的养生之旅'
      },
      {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/23/8492f586c3c1551cab635ccb25a4921f.jpg_200x200_4a7a209d.jpg',
        title: '罗浮山宝田养生温泉',
        desc: '浪漫惠州首战，浪漫的养生之旅'
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
    height: 1.9 rem
    .item-img
      width: 1.7 rem
      height: 1.7 rem
      padding: .1 rem
    .item-info
      flex: 1
      padding: .1 rem
      min-width: 0
      .item-title
        line-height: .54 rem
        font-size: .32 rem
        ellipsis()
      .item-desc
        line-height: .4 rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44 rem
        margin-top: .16 rem
        background: #ff9300
        padding: 0 .2 rem
        border-radius: .06 rem
        color: #fff
</style>
