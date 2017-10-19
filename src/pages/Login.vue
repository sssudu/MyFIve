<template>
    <div class="login">
        <div class="loginHeader">
            <div class="loginHeaderCenter">
                <v-link href="/" class="FiveLuxLogo"></v-link>
                <span class="headerLine"></span>
                <span class="headerText">欢迎登陆</span>
                <div class="headerRight">
                    <div class="headerRightText">
                        <i class="loginIcon"></i>
                        <p class="loginText">客服热线：4008-6767-38</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="loginWraper">
            <div class="loginwp">
                <div class="loginCRight">
                    <ul class="logTitle">
                        <li class="logTitleList fl" :class="{loginActive:showTip[0]}" style="float:left" @click="whitchShow(0)">扫码登录</li>|
                        <li class="logTitleList fr" :class="{loginActive:showTip[1]}" @click="whitchShow(1)">账户登录</li>

                    </ul>
                    <div class="logBody">
                        <div class="saoma" v-if="showTip[0]" >
                            <div class="ma">
                                <div class="qcodeHook" @mouseenter="isShowImg=true" @mouseleave="isShowImg=false">
                                    <img src="http://m.5lux.com/api/gen2qrcode?t=1507774812205" alt="">
                                    <img src="http://www.5lux.com/vendor/images/5lux/login/new/exqcode.png" alt="" class="quImg" v-bind:style="isShowImg?logoImg:''">
                                </div>
                            </div>
                        </div>
                        <div class="user" v-if="showTip[1]">
                            <form action="" class="submit">
                                <input type="text" v-model="test" class="user_hk" placeholder="邮箱/手机号/账号" @blur="errorTip">
                                <input type="text" class="user_hk" placeholder="密码">
                                <div class="erro_tip">
                                    <div class="erro_tip_tip" v-show="!isErrorTipShow">
                                        <i class="tip_logo"></i>
                                        <p class="tip_text">用户名不正确</p>
                                    </div>
                                </div>
                                <input type="submit" class="sub_btn">
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <v-foot></v-foot>
    </div>
</template>
<script>
import Vue from 'vue'
import VLink from '../components/VLink.vue'
import VFoot from '../components/Footer.vue'
export default {
    data() {
        return {
            showTip: [true, false],
            logoImg: {
                display:'inline-block',verticalAlign: 'top', marginLeft: '20px', height: '165px', width: '165px'
            },
            isShowImg: false,
            isErroTip:false,
            test:''
        }
    },
    components: {
        VFoot,VLink
    },
    computed:{
        isErrorTipShow:function(){
            let reg =/^[a-zA-Z0-9_-]{8,16}$/;
            let reg1 = /^((13[0-9])|(14[5|7])|(15([0-3]|[5-9]))|(18[0,5-9]))\d{8}$/;
            let email = /^([A-Za-z0-9_\-\.])+\@([A-Za-z0-9_\-\.])+\.([A-Za-z]{2,4})$/;
            return reg.test(this.test)||reg1.test(this.test)||email.test(this.test);
        }
    },
    methods: {
        whitchShow: function(index) {
            console.log(this.showTip)
            //   this.showTip[1] = false;
            //   this.showTip[0] = false;
            //   this.showTip[index] = true;
            //vue无法直接改变像上面改变数组的值，
            Vue.set(this.showTip, 0, false);
            Vue.set(this.showTip, 1, false);
            Vue.set(this.showTip, index, true);
        },
        errorTip:function(){
            
        }
    }
}
</script>
<style>
@import '/static/common/common.css';
*{
  margin: 0;
  padding: 0;
  }
.loginHeader {
    height: 98px;
}

.loginHeaderCenter {
    width: 1210px;
    height: 100%;
    margin: 0 auto;
    font-size: 0;
}

.login .FiveLuxLogo {
    vertical-align: middle;
    display: inline-block;
    height: 98px;
    width: 244px;
    background-size: 244px 98px;
    background-repeat: no-repeat;
    background-image: url(http://www.5lux.com/vendor/images/5lux/login/new/5luxlogo.jpg)
}

.headerLine {
    display: inline-block;
    width: 2px;
    height: 44px;
    vertical-align: middle;
    background-color: #ccc;
    margin: 0 18px;
}

.headerText {
    display: inline-block;
    font-size: 22px;
    color: #999;
    vertical-align: middle;
}

.loginHeader .headerRight {
    display: table;
    font-size: 0;
    height: 100%;
    float: right;
}

.loginHeader .headerRightText {
    display: table-cell;
    vertical-align: middle;
}

.login .loginIcon {
    display: inline-block;
    width: 19px;
    height: 19px;
    padding-right: 10px;
    background-image: url(http://www.5lux.com/vendor/images/5lux/login/new/phone-logo.png);
    background-size: 19px 19px;
    background-repeat: no-repeat;
    vertical-align: middle;
}

.login .loginText {
    display: inline-block;
    color: #666;
    font-size: 13px;
    vertical-align: middle;
}

.login .loginWraper {
    background-color: #262626;
    text-align: center;
}

.loginWraper .loginwp {
    position: relative;
    width: 1210px;
    height: 524px;
    background-repeat: no-repeat;
    background-size: 100% 100%;
    margin: 0 auto;
    background-image: url(http://www.5lux.com/vendor/images/5lux/login/new/login_background1.jpg);
    padding: 30px 0;
    background-size: 100% 584px;
}

.loginCRight {
    width: 400px;
    float: right;
    margin-right: 40px;
    padding: 0;
    background: #ffffff;
}

.loginCRight .logTitle {
    margin: 0 20px;
    margin-top: 34px;
    font-size: 20px;
    line-height: 20px;
    height: 20px;
    color: #999;
}

.logTitleList {
    font-size: 20px;
    line-height: 20px;
    font-weight: 400;
    width: 49%;
    text-align: center;
    cursor: pointer;
    float: right;
}

.loginActive {
    color: #000;
}

.logBody {
    width: 100%;
    height: 380px;
}

.saoma {
    text-align: center;
    height: 100%;
    display: table;
}

.saoma .ma {
    display: table-cell;
    width: 400px;
    margin: 0 auto;
    vertical-align: middle;
    text-align: center;
}

.qcodeHook {
    height: 165px;
    display: inline-block;
}

.quImg {
    vertical-align: top;
    margin-left: 20px;
    height: 165px;
    width: 0px;
    transition: .3s;
}

.user {
    text-align: center;
    height: 100%;
    display: block;
}

.user .submit {
    padding-top: 20px;
}

.user .user_hk {
    display: block;
    margin: 0 31px;
    margin-top: 16px;
    width: 296px;
    height: 48px;
    border: 1px solid #CCC;
    padding: 0 20px;
    font-size: 14px;
}

.erro_tip {
    width: 338px;
    margin: 0 31px;
    height: 54px;
}

.tip_logo {
    display: inline-block;
    width: 14px;
    height: 14px;
    background-image: url(http://www.5lux.com/vendor/images/5lux/login/new/close.png);
    background-size: 14px 14px;
    background-repeat: no-repeat;
    vertical-align: middle;
}

.erro_tip_tip {
    font-size: 0;
    color: #f62b0f;
    height: 14px;
    line-height: 14px;
    margin: 20px 0;
    /* cursor: pointer; */
}

.tip_text {
    height: 14px;
    line-height: 14px;
    font-size: 14px;
    display: inline-block;
    vertical-align: middle;
    margin-left: 5px;
}

.sub_btn {
    transition: all linear 0.5s;
    -moz-transition: all linear 0.5s;
    -webkit-transition: all linear 0.5s;
    -o-transition: all linear 0.5s;
    /* display: inline-block; */
    width: 338px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    color: #fff;
    background: #333;
    margin: 0 31px;
    /* text-decoration: none; */
    font-size: 18px;
    border: none;
    cursor: pointer;
}

.sub_btn:hover {
    background: #a60000;
}
</style>
