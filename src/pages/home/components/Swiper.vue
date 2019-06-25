<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for='item of swiperList' :key='item.id'>
      <img class='swiper-img' :src='item.imgUrl'>
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
    export default {
        name: "HomeSwiper",
        data(){
          return {
            swiperOption:{
              pagination:{
                el:'.swiper-pagination'
              },
              loop:true
            },
            swiperList:[{
              id:'0001',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/818f6cc784ae6669b74bbbb255414a53.jpg_750x200_66ca5873.jpg'
            },{
              id:'0002',
              imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/3f47010a2312c32fff92fec3bcc99563.jpg_750x200_7ae774e5.jpg'
            }]
          }
        }
    }
</script>

<style lang='stylus' scoped>
  .wrapper >>>.swiper-pagination-bullet-active
    background:#fff
  .wrapper
    width:100%
    overflow :hidden
   .swiper-img
      width:100%;
</style>
