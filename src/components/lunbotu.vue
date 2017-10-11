<template>
    <div class="swiper-container swipers" :class="detail.Name">
        <div class="swiper-wrapper">
            <div class="swiper-slide slide" v-for="ul in swiper">
                <a href="javascript:;" v-for="imgs in ul.listPic"><img :src="imgs" alt=""></a>
                </div>
        </div>
        
        
        <!-- 如果需要导航按钮 -->
        <div class="bx-controls-direction">
            <a  href="javascript:;" class="bx_next" :class="detail.nextButton">Next</a>
            <a  href="javascript:;" class="bx_prev" :class="detail.prevButton">Prev</a>
        </div>
        <div class="pager" :class="detail.pagination"></div>
    </div>
</template>
<script>
import swiper from '../../static/swiper/swiper-3.4.2.min.js'
export default {
    props:['swiper','detail'],
    data() {
        return {
        }
    },
    mounted() {
        var mySwiper = new Swiper('.'+this.detail.Name, {	//挂载创建swiper实例

            direction: this.detail.direction,	//滑动方向

            loop: this.detail.loop,	//是否可循环（能从最后一个滑块滑到第一个）

            pagination: this.detail.pagination,

            autoplay:this.detail.autoplay,

            nextButton: '.'+this.detail.nextButton,

            speed:this.detail.speed,

            prevButton: '.'+this.detail.prevButton

        })
    }
}
</script>
<style>
@import '/static/swiper/swiper-3.4.2.min.css';
.swiper-container {
    
    width: 100%;
}
.swipers{
    overflow: hidden;
    width: 100%;
    height: 150px;
    margin-top: 14px;
}
.slide img{
    max-width: 100%;
    display: block;
        float: left;
    margin-right: 2px;
}
.slide img{
    border: none !important;
    width: 90px !important;
    height: auto !important;
    margin-bottom: 12px !important;
    margin-left: 12px !important;
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
.pager{
        text-align: center;
    /* font-size: .85em; */
    font-family: Arial;
    font-weight: bold;
    color: #666;
    padding-top: 1em;
    padding-bottom: 1em;
    position: absolute;
    bottom: -4px!important;
    width: 100%;
    
}
.bx-controls-direction a{
    width: 8px!important;
    height: 14px!important;
    top: 122%!important;
    position: absolute;
    margin-top: -60px;
    outline: 0;
    text-indent: -9999px;
    z-index: 9999;
}
.bx-controls-direction .bx_prev{
        left: 70px!important;
    background: url(http://www.5lux.com/vendor/images/v30/share02.png) no-repeat -239px -384px!important;
}
.bx-controls-direction .bx_next{
    right: 70px!important;
    background: url(http://www.5lux.com/vendor/images/v30/share02.png) no-repeat -267px -384px!important;
}
</style>



