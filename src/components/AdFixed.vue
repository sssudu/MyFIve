<template>
    <div class="fix_ad" v-if="isPopShow">
        <div class="pop_main">
            <img :src="imgSrc" alt="">
            <a href="javascript:;" @click="isPopShow=false"></a>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            imgSrc:'/src/imgs/foot_popup.png',
            isPopShow:true,
            ss:'a'
            }
    }
}
</script>
<style>
.fix_ad {
    position: fixed;
    bottom: 0;
    width: 100%;
    height: 120px;
    height: 120px;
    z-index: 99999;
    /* width: 100%; */
    background: url(http://img550.5lux.com.cn/2016/12/27/mn/148282825934_2x120.png) repeat-x center top;
}
.fix_ad img,.pop_main{
    width: 1210px;
    height: 120px;
    position: absolute;
    bottom: 0;
    left: 50%;
    margin-left: -605px;
}
.fix_ad a{
    position: absolute;
    top: 0px;
    right: 0;
    height: 47px;
    width: 70px;
}
</style>
