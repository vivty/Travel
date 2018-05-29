<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
        <swiper-slide v-for="item of SwiperList" :key="item.id">
           <img :src="item.imgURL" class="swiper-img">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>
</template>
<script>
export default {
    name: 'HomeSwiper',
    data (){
        return{
        swiperOption:{
            pagination:'.swiper-pagination',
            loop: true
        },
        SwiperList:[{
           id: '0001',
           imgURL: 'http://img1.qunarzz.com/piao/fusion/1805/77/f63bd04dd5319602.jpg_750x200_6ba8e0ca.jpg'
        },{
            id: '0002',
            imgURL: 'http://img1.qunarzz.com/piao/fusion/1706/b8/a8e8ff02b094c802.jpg_750x200_ddaec8e5.jpg'
        }]
    }
    }
}
</script>
<style lang='stylus' scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width：100%
    heigth:0
    padding-bottom:31.25%
    background:#eee
     .swiper-img
       width:100%
</style>



