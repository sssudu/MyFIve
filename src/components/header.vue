<template>
    <header>
        <div class="head">
            <div class="go_homepage">
                <b></b>
                <a href="">第五大道首页</a>
                <i></i>
            </div>
            <div class="go_phone">
                <b></b>
                贵宾专线：4008-6767-38
            </div>
            <div class="head_right">
                <div class="mobile" @mouseover="mobilShow=true" @mouseout="mobilShow=false">
                    <div>
                        <span>手机版下载</span>
                    </div>
                    <ul v-show="mobilShow">
                        <li><img :src="imgSrc[0]" alt=""></li>
                        <li>扫描下载APP</li>
                        <li>
                            <span>赠送50元</span>立即</li>
                    </ul>
                </div>
                <div class="help">
                    <a href="">帮助中心</a>
                    <i></i>
                </div>
                <div class="my5lux" @mouseover="lux5Show=true" @mouseout="lux5Show=false">
                    <div>
                        <span>我的第五大道</span>
                        <i></i>
                    </div>
                    <ul v-show="lux5Show">
                        <li>
                            <a href="">我的订单</a>
                        </li>
                        <li>
                            <a href="">我的收藏</a>
                        </li>
                        <li>
                            <a href="">已购商品</a>
                        </li>
                        <li>
                            <a href="">我的礼券</a>
                        </li>
                        <li>
                            <a href="">我的积分</a>
                        </li>
                    </ul>

                </div>
                <div class="logbox">
                    <div class="login">
                        <a href="">登陆</a>
                        <i></i>
                    </div>
                    <div class="regist">
                        <span></span>
                        <a href="">注册</a>
                        <i></i>
                    </div>

                </div>

            </div>

        </div>
        <div class="head_mid">
            <div class="mid_content">
                <div class="mid_logo">
                    <a href="">
                        <img :src="imgSrc[1]" alt="" title="第五大道奢侈品网">
                    </a>
                </div>
                <div class="mid_ad">
                    <a href="javascript:;">
                        <img :src="imgSrc[2]" alt="">
                    </a>
                </div>
                <div class="mid_search">
                    <form action="">
                        <div class="in_con">
                            <input type="text" name="keyword" class="search_input" placeholder="唇部彩妆">
                            <input type="button" value="搜 索" class="search_b">
                            <ul class="inc_adlist">
                                <li>
                                    <a href="">太阳镜</a>
                                </li>
                                <li>
                                    <a href="">美妆</a>
                                </li>
                                <li>
                                    <a href="">运动户外</a>
                                </li>
                                <li>
                                    <a href="">箱包</a>
                                </li>
                                <li>
                                    <a href="">配饰</a>
                                </li>
                                <li>
                                    <a href="">腕表</a>
                                </li>
                            </ul>
                        </div>
                    </form>
                </div>
                <div class="mid_cart">
                    <div class="cart_content">
                        <div class="cart_unit" @mouseenter="shopingShow=true" @mouseleave="shopingShow=false">
                            <img :src="imgSrc[3]" alt="" width="22"> 购物袋(
                            <span id="cart_number">0</span> )
                            <transition name="slide-fade">
                                <div v-show="shopingShow">
                                    <div class="shopping_bag">
                                        <ul>
                                            <li>
                                                <p>购物袋暂时没有商品，</p>
                                                <br> 赶紧选择心爱的商品吧！
                                            </li>
                                        </ul>
                                    </div>
                                    <b></b>
                                </div>
                            </transition>
                        </div>

                    </div>
                </div>
            </div>

        </div>
    </header>
</template>
<script>

export default {

    data() {
        return {
            imgSrc: ['/src/imgs/qr.jpg', '/src/imgs/logo.jpg', '/src/imgs/yijian.jpg', '/src/imgs/v30cart.png'],
            lux5Show: false,
            mobilShow: false,
            shopingShow: false
        }
    }
}
</script>
<style>
.slide-fade-enter-active {
    transition: all .3s ease;
}

.slide-fade-leave-active {
    transition: all .3s ease;
}

.slide-fade-enter,
.slide-fade-leave-to
/* .slide-fade-leave-active for below version 2.1.8 */

{
    transform: translateY(-10px);
    opacity: 0;
}

a {
    color: inherit;
    text-decoration: none;
}

ul {
    list-style: none;
}

a:hover {
    color: rgb(178, 130, 71);
}

.head {
    font: 12px/200% "microsoft yahei", 微软雅黑, Helvetica, Arial, Tahoma, 黑体, 宋体, sans-serif;
    height: 30px;
    background: rgb(242, 242, 242);
    position: relative;
    width: 1210px;
    margin: 0px auto;
}

.head div {
    height: 30px;
    position: relative;
    color: rgb(102, 102, 102);
    text-align: center;
}

.head .go_homepage {
    display: inline-block;
    float: left;
    text-align: center;
    width: 110px;
    line-height: 30px;
}

.head .go_phone {
    padding-left: 6px;
    text-align: left;
    display: inline-block;
    float: left;
    width: 166px;
    line-height: 30px;
}

.head .go_homepage b {
    display: inline-block;
    width: 16px;
    height: 14px;
    position: absolute;
    left: 2px;
    top: 7px;
    background: url(/src/imgs/home.png) center center no-repeat;
}

.head .go_phone b {
    width: 25px;
    height: 30px;
    display: inline-block;
    float: left;
    background: url(/src/imgs/brandstore_share.png) -348px -338px no-repeat;
}

.head a {
    display: inline-block;
    margin-left: 7px;
}

.head .go_homepage i {
    position: absolute;
    height: 12px;
    right: 0px;
    top: 9px;
    border-left: 1px solid rgb(223, 223, 223);
}

.head_right {
    width: 604px;
    float: right;
    line-height: 30px;
    position: relative;
    vertical-align: middle;
}

.head_right div {
    display: inline-block;
    float: left;
    text-align: center;
    line-height: 30px;
    height: 30px;
    width: 100%;
    position: relative;
}

.head_right i {
    position: absolute;
    height: 12px;
    right: 0px;
    top: 9px;
    border-left: 1px solid rgb(223, 223, 223);
}

.head_right span {
    float: left;
}

.head .mobile {
    width: 106px;
    position: absolute;
    right: 0px;
    top: 0px;
    z-index: 33;
    cursor: pointer;
    padding: 0px 11px;
}

.mobile ul {
    display: inline-block;
    float: left;
    text-align: center;
    width: 106px;
}

.mobile img {
    width: 106px;
}

.mobile ul li {
    line-height: 20px;
    font-size: 13px;
}

.mobile ul li span {
    color: rgb(208, 0, 0);
    font-size: 16px;
}

.mobile div {
    padding-left: 5px;
    background: url(/src/imgs/brandstore_share.png) -218px -369px no-repeat;
}

.mobile:hover {
    background: rgb(255, 255, 255);
}

.mobile div:hover {
    color: rgb(208, 0, 0);
    background: url(/src/imgs/brandstore_share.png) -218px -404px no-repeat;
}

.head .help {
    position: absolute;
    width: 85px;
    right: 130px;
    top: 0px;
}

.head .my5lux {
    width: 130px;
    position: absolute;
    right: 215px;
    top: 0px;
    z-index: 150;
}

.my5lux:hover {
    background: rgb(255, 255, 255);
}

.head .my5lux ul {
    float: left;
    width: 100%;
    background: rgb(255, 255, 255);
}

.my5lux span {
    float: left;
    padding-left: 15px;
}

.my5lux div {
    background: url(/src/imgs/brandstore_share.png) -253px -436px no-repeat;
}

.logbox {
    position: absolute;
    right: 350px;
    top: 0;
}

.head_right .regist {
    width: 88px;
}

.head_right .regist span {
    width: 22px;
    height: 24px;
    float: left;
    background: url('/src/imgs/youli.gif') no-repeat;
    margin: 0 5px 0 17px;
}

.head_right .login {
    width: 100px;
    text-align: right;
    padding-right: 20px;
}

.head .logbox {
    position: absolute;
    right: 350px;
    top: 0px;
    line-height: 30px;
    color: rgb(0, 0, 0);
    width: auto;
}

.head_mid {
    background: #fff;
}

.mid_content {
    position: relative;
    height: 110px;
    width: 1210px;
    margin: 0 auto;
}

.mid_logo {
    position: absolute;
    top: 0;
    left: 0;
    width: 244px;
    height: 110px;
}

.mid_ad {
    position: absolute;
    /* top: 10px; */
    /* left: 240px; */
    top: 14px;
    left: 290px;
    /* width: 135px; */
    width: 142px;
    height: 80px;
    overflow: hidden;
}

.mid_search {
    overflow: hidden;
    position: absolute;
    /* left: 380px; */
    left: 485px;
    top: 36px;
}

.mid_search .in_con {
    width: 383px;
    padding: 2px 2px;
    background: #c69c6d;
    height: 34px;
}

.in_con .search_input {
    outline: none;
    /* width: 410px; */
    width: 300px;
    height: 34px;
    line-height: 34px;
    vertical-align: middle;
    border: none;
    background: #fff;
    padding-left: 3px;
    float: left;
}

.in_con .search_b {
    width: 86px;
    width: 80px;
    height: 34px;
    border: none;
    float: left;
    color: #fff;
    font-size: 15px;
    background: none;
}

.inc_adlist {
    clear: both;
}

.in_con .inc_adlist li {
    display: inline-block;
    float: left;
    color: #999;
    font-size: 11px;
    padding-right: 25px;
    line-height: 32px;
}

.inc_adlist li a:hover {

    color: #d00000;
}

.mid_cart {
    position: absolute;
    right: 10px;
    top: 35px;
    z-index: 30;
}

.cart_content {
    width: 290px;
    background: #fff;
    position: relative;
}

.mid_cart .cart_unit {
    cursor: pointer;
    width: 138px;
    height: 32px;
    line-height: 32px;
    text-indent: 45px;
    border: 1px solid #ccc;
    box-shadow: 0 0 2px rgba(0, 0, 0, .2);
    -moz-box-shadow: 0 0 2px rgba(0, 0, 0, .2);
    -webkit-box-shadow: 0 0 2px rgba(0, 0, 0, .2);
    position: relative;
    float: right;
    color: #666;
    background: url(/src/imgs/brandstore_share.png) no-repeat -337px -405px;
}

.cart_unit img {
    position: absolute;
    left: 10px;
    top: 2px;
}

.cart_unit span {
    color: #d00000;
}

.shopping_bag {
    position: absolute;
    right: -1px;
    clear: both;
    width: 268px;
    padding: 10px 10px 20px 10px;
    border: 1px solid #ccc;
    text-align: center;
    box-shadow: 0 0 2px rgba(0, 0, 0, .2);
    -webkit-box-shadow: 0 0 2px rgba(0, 0, 0, .2);
    -moz-box-shadow: 0 0 2px rgba(0, 0, 0, .2);
    background-color: #fff;
}

.cart_content b {
    width: 138px;
    height: 4px;
    display: block;
    position: absolute;
    background: #fff;
    right: 0px;
    top: 29px;
    z-index: 1;
}
</style>
