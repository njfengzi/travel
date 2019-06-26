<template>
  <div>
    <div class='title'>周末去哪儿</div>
    <ul>
      <li class="item border-bottom"
          v-for='item of recommendList'
          :key='item.id'
      >
        <div class="item-img-wrapper">
          <img class='item-img' :src='item.imgUrl'>
        </div>
        <div class='item-info'>
          <p class='item-title'>{{item.title}}</p>
          <p class='item-desc'>{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
  export default {
    name: "HomeWeekend",
    data:function () {
      return {
        recommendList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/e1/cdbf56d837da59.jpg_r_640x214_105fc3f2.jpg',
          title:'大连圣亚',
          desc:'浪漫大连首页'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/e1/cdbf56d837da59.jpg_r_640x214_105fc3f2.jpg',
          title:'大连圣亚',
          desc:'浪漫大连首页'
        },{
          id:'0003',
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/f3/d51669250308cc.jpg_r_640x214_7a127cd0.jpg',
          title:'大连圣亚',
          desc:'浪漫大连首页'
        },{
          id:'0004',
          imgUrl:'http://img1.qunarzz.com/sight/source/1811/58/a02ad3ab47e3e3.jpg_r_640x214_08977098.jpg',
          title:'大连圣亚',
          desc:'浪漫大连首页'
        }]
      }
    }
  }
</script>

<style lang='stylus' scoped>
  @import "../../../assets/styles/mixins.styl"
  .title
    margin-top:.2rem
    line-height:.8rem
    background:#eee
    text-indent:.2rem
  .item-img-wrapper
    height:0
    overflow:hidden
    padding-bottom:33.9%
  .item-img
    width:100%
  .item-info
    min-width:0
    padding:.1rem
  .item-title
    line-height:.54rem
    font-size:.32rem
    ellipsis()
  .item-desc
    line-height:.4rem
    color:#ccc
    ellipsis()



</style>
