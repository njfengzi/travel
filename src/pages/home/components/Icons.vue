<template>
  <div class='icons'>
    <swiper >
      <swiper-slide v-for='(page,index) of pages' :key='index'>

    <div class="icon" v-for='item of page' :key='item.id'>
      <div class="icon-img">
        <img class='icon-img-content' :src='item.imgUrl'>
      </div>
      <p class='icon-dec'>{{item.desc}}</p>
    </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
    export default {
        name: "HomeIcons",
        data(){
          return {
            iconList:[{
              id:'0001',
              imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
              desc:'景点门票'
            },
              {
                id:'0002',
                imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
                desc:'滑雪季'
              },
              {
                id:'0003',
                imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
                desc:'文化古迹'
              },
              {
                id:'0004',
                imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/97/02f5043b51b2102.png',
                desc:'牛首山'
              },
              {
                id:'0005',
                imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/b71c1387a921ccf9c6edc7e8def3da90.png',
                desc:'红山森林动物园'
              },
              {
                id:'0006',
                imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
                desc:'滑雪季'
              },
              {
                id:'0007',
                imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
                desc:'文化古迹'
              },
              {
                id:'0008',
                imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/97/02f5043b51b2102.png',
                desc:'牛首山'
              },
              {
                id:'0009',
                imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/b71c1387a921ccf9c6edc7e8def3da90.png',
                desc:'红山森林动物园'
              }
            ]
          }
        },
        computed:{
          pages (){
            const pages =[]
            this.iconList.forEach((item,index)=>{
              const page =Math.floor(index/8);
              if (!pages[page]){
                pages[page]=[]
              }
              pages[page].push(item)
            })
            return pages
          }
        }
    }
</script>

<style lang='stylus' scoped>
  @import "../../../assets/styles/varibles.styl"
  @import "../../../assets/styles/mixins.styl"
 .icons>>>.swiper-container
   height:0
   padding-bottom:50%
  .icons
    margin-top:.1rem

  .icon
    width:25%
    float:left
    overflow:hidden
    padding-bottom:25%
    position:relative;
    height:0
  .icon-img
    position:absolute
    top:0
    left:0
    bottom:0.44rem
    width:100%;
    box-sizing:border-box
    padding:.1rem
  .icon-img-content
    display:block
    margin:0 auto
    height:100%
  .icon-dec
    position:absolute
    width:100%
    text-align:center
    left:0
    bottom:0
    height:.44rem
    line-height:.44rem
    color:$darkTextColor
    ellipsis()
</style>
