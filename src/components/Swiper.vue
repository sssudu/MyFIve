<template>
    <div class="swiper-container " id="top_swiper">
        <div class="swiper-wrapper">
            <div class="swiper-slide"><a href=""><img :src="swiper.imgSrc[0]" alt=""></a></div>
            <div class="swiper-slide"><a href=""><img :src="swiper.imgSrc[1]" alt=""></a></div>
            <div class="swiper-slide"><a href=""><img :src="swiper.imgSrc[2]" alt=""></a></div>
            <div class="swiper-slide"><a href=""><img :src="swiper.imgSrc[3]" alt=""></a></div>
        </div>
        <!-- 如果需要分页器 -->
        <div class="swiper-pagination swiper-pointers"></div>

        <!-- 如果需要导航按钮 -->
        <div class="btns">
            <div class="swiper-button-prev" id="left-swiper"></div>
            <div class="swiper-button-next" id="right-swiper"></div>
        </div>

        <!-- 如果需要滚动条 -->
        <div class="swiper-scrollbar"></div>
    </div>
</template>
<script>
import swiper from '../../static/swiper/swiper-3.4.2.min.js'
export default {
    props:[],
    data() {
        return {
            swiper:{
                imgSrc:['/src/imgs/150570390639_1440x520.jpg', '/src/imgs/150579029436_1440x520.jpg','/src/imgs/150587969280_1440x520.jpg','/src/imgs/150596336935_1440x520.jpg'],
               
            }
            
        }
    },
    mounted() {

        var mySwiper = new Swiper('#top_swiper', {	//挂载创建swiper实例

            direction: 'horizontal',	//滑动方向

            loop: true,	//是否可循环（能从最后一个滑块滑到第一个）

            pagination: '.swiper-pagination',

            autoplay:1500,

            nextButton: '.btns .swiper-button-next',

            speed:500,

            prevButton: '.btns .swiper-button-prev'

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

.swiper-container .btns {
    width: 1000px;
    margin: 0 auto;
    position: absolute;
    top: 0px;
    left: 50%;
    transform: translate(-50%);
    height: 100px;
    z-index: 999;

}
.swiper-pointers{
    z-index: 100;
}
#left-swiper {
    top: 200px;
    left: 0;
    cursor: pointer;
    position: absolute;
    background: url(/src/imgs/templateleft.png);
    
}

#right-swiper {

    top: 200px;
    right: 0;
    cursor: pointer;
    position: absolute;
    background: url(/src/imgs/templateright.png);
}

.swiper-container #right-swiper img {
    border: none;
    vertical-align: middle;
}

.swiper-container #left-swiper img {
    border: none;
    vertical-align: middle;
}
</style>


