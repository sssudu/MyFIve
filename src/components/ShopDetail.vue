<template>
  <div class="shopdetail">
        <div class="shopdetailtitle">
            <img :src="shop.shopPic" alt="">
            <div class="rightbtn">
                <a href="">
                    <span class="icon"></span>
                    <span class="moretxt">SHOW MORE</span>
                </a>
            </div>
        </div>
        <div class="goods">
            <div class="goods1">
                <ul class="goodslinks">
                    <li class="goodsitem" v-for="goodlink in shop.shopList"><a href="">{{goodlink}}</a></li>
                </ul>
                <v-swiper v-bind="shop" :detail="swiperDetail"></v-swiper>
            </div>
            <div class="goods2">
                <a href="">
                    <img :src="shop.shopDetailPic" alt="">
                </a>
            </div>
            <div class="goods3">
                <div class="Pic" v-for="(detailPic,detailPicIndex) in shop.shopDetail" :class="detailPicIndex%2==0?goodsPic:goodsPic2">
                    <img :src="detailPic" alt="">{{detailPicIndex}}
                </div>
            </div>
        </div>
  </div>
</template>
<script>
import VSwiper from '../components/lunbotu.vue'
export default {
    //获取的是传入对象的键值对(属性)
  props:['shop'],
  data(){
      return {
          swiperDetail:{	//挂载创建swiper实例
            Name:'classic',
            direction: 'horizontal',	//滑动方向

            loop: true,	//是否可循环（能从最后一个滑块滑到第一个）

            pagination: 'pager',

            autoplay:0,

            nextButton: 'goods_next',

            speed:500,

            prevButton: 'goods_prev'

        },
        goodsPic:'goods3Pic1',
        goodsPic2:'goods3Pic2'
      }
  },
  components:{
      VSwiper
  }
}
</script>
<style>
.shopdetail .rightbtn{
    float: right;
    overflow: hidden;
    height: 60px;
    line-height: 60px;
}
.shopdetail .rightbtn .moretxt{
    float: right;
    font-size: 16px;
}
.shopdetail .rightbtn .icon{
        float: right;
    background: url(http://www.5lux.com/vendor/images/v30/share02.png) no-repeat -470px -360px;
    width: 18px;
    height: 60px;
    margin-left: 6px;
}
.goods{
    overflow: hidden;
}
.goods .goods1{
    float: left;
    width: 220px;
    height: 366px;
    border: 1px solid #ccc;
    padding: 0 9px;
    padding-top: 4px;
    margin-right: 8px;
}
.goods1 .goodslinks{
    overflow: hidden;
    border-bottom: 1px dashed #d4d4d4;
    padding-bottom: 16px;
}
.goods1 .goodslinks .goodsitem{
    float: left;
    line-height: 36px;
    width: 110px;
    font-size: 14px;
    color: #666;
    text-align: left;
}
.goods .goods2{
    float: left;
    width: 390px;
    height: 370px;
    border: 1px solid #ccc;
    overflow: hidden;
    margin-right: 8px;
}
.goods .goods3{
    overflow: hidden;
    height: 372px;
}
.goods3 .goods3Pic1{
        width: 276px;
    height: 189px;
    margin-right: 7px;
}
.goods3 .goods3Pic2{
    width: 276px;
    height: 189px;
}
.goods3 .Pic{
    float: left;
}
</style>
