<template>
  <div class="hot_store">
      <div class="hotstore_title">
          <img :src="hotstore.hotStoreTitle" alt="">
          <div class="hotarrowbtn">
                <a class="hot_pre" href="javascript:;"></a>
                <a class="hot_next" href="javascript:;"></a>
            </div>
      </div>

      <div class="hotflag">
          <div class="swiper-container " id="hot_swiper">
            <div class="swiper-wrapper">
                <div class="swiper-slide" v-for="items in hotstore.hotStoreList">
                    <div class="hotflagson" v-for="son in items" @mouseover="son.isShow=true" @mouseleave="son.isShow=false">
                        <img class="sonPic" :src="son.imgSrc" alt="">
                        <div class="hotmiddle" :style="{opacity:son.isShow?1:0}">
                            <a href="">
                                <p class="brandchname">{{son.name}}</p>
                                <p class="blackline"><span></span></p>
                            </a>
                        </div>
                        <div class="topline" :style="{width:son.isShow?166+'px':0}"></div>
                        <div class="rightline" :style="{height:son.isShow?85+'px':0}"></div>
                        <div class="bottomline" :style="{width:son.isShow?166+'px':0}"></div>
                        <div class="leftline" :style="{height:son.isShow?85+'px':0}"></div>
                    </div>
                </div>
            </div>

            <!-- 如果需要导航按钮 -->
            

        </div>
      </div>
  </div>
</template>
<script>
export default {
  props:['hotstore'],
  data(){
      return {thisItem:false}
      
  },
  mounted() {

        var mySwiper = new Swiper('#hot_swiper', {	//挂载创建swiper实例

            direction: 'horizontal',	//滑动方向

            loop: false,	//是否可循环（能从最后一个滑块滑到第一个）

            nextButton: '.hotarrowbtn .hot_next',

            speed:500,

            prevButton: '.hotarrowbtn .hot_pre'

        })
    }
}
</script>
<style>
@import '/static/swiper/swiper-3.4.2.min.css';
.swiper-container {
    /* background: #000; */
    /* height: 520px; */
    /* overflow: hidden; */
    width: 100%;
}
.hotflag{
    height: 180px;
    width: 100%;
    position: relative;
    overflow: hidden;
}
.hotflagson{
    position: relative;
    float: left;
    width: 106px;
    height: 55px;
    padding: 14px 29px;
    border: 1px solid #dfdfdf;
    margin-right: 6px;
    margin-bottom: 7px;
}
.hotflagson .topline{
    height: 1px;
    position: absolute;
    top: -1px;
    left: 0;
    background: #000;
    transition: .3s;
}
.hotflagson .bottomline{
    height: 1px;
    position: absolute;
    bottom: -1px;
    left: 0;
    background: #000;
    transition: .3s;
}
.hotflagson .rightline{
    width: 1px;
    position: absolute;
    bottom: -1px;
    right: -1px;
    background: #000;
    transition: .3s;
}
.hotflagson .leftline{
   width: 1px;
    position: absolute;
    top: -1px;
    left: -1px;
    background: #000; 
    transition: .3s;
}
.hotflagson .sonPic{
        width: 107px;
    height: 54px;
}
.hotmiddle{
    position: absolute;
    left: 29px;
    top: 14px;
    opacity: .8;
    width: 107px;
    height: 42px;
    padding-top: 12px;
    background: #fff;
    transition: .3s;
    /* transition: .8s; */
}
.hotstore_title{
    overflow: hidden;
}
.hotstore_title .hotarrowbtn{
    float: right;
    padding-top: 23px;
    padding-right: 15px;
}
.hotarrowbtn a{
    width: 8px;
    height: 15px;
    cursor: pointer;
    display: inline-block;
}
.hotarrowbtn .hot_pre{
    background: url(/src/imgs/share02.png) no-repeat -160px -384px;
}
.hotarrowbtn .hot_next{
    background: url(/src/imgs/share02.png) no-repeat -180px -384px;
    margin-left: 20px;
}
.hotmiddle .brandchname{
    font-size: 18px;
    text-align: center;
}
.blackline{
    text-align: center;
    margin-top: 5px;
    line-height: 0;
}
.blackline span{
        display: inline-block;
    width: 20px;
    height: 2px;
    background: #000;
}
</style>
