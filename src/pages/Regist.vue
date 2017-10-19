<template>
  <div class="regist">
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
                    <div class="registTitle" style="
    padding-bottom: 10px;
">注册第五大道</div>
                    <div class="logBody">
                        <div class="user">
                            <form action="" class="submit" style="padding:0">
                                <input type="text" class="user_hk" placeholder="手机号">
                                <div class="phoneTest">
                                    <input type="text" class="user_hk cross" placeholder="请输入验证码"><span class="phoneOpen">获取验证码</span>
                                </div>
                                <input type="text" class="user_hk" placeholder="请输入密码">
                                <input type="text" class="user_hk" placeholder="确认密码">
                                
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
  components:{
      VFoot,VLink
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

.regist .FiveLuxLogo {
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

.regist .loginIcon {
    display: inline-block;
    width: 19px;
    height: 19px;
    padding-right: 10px;
    background-image: url(http://www.5lux.com/vendor/images/5lux/login/new/phone-logo.png);
    background-size: 19px 19px;
    background-repeat: no-repeat;
    vertical-align: middle;
}

.regist .loginText {
    display: inline-block;
    color: #666;
    font-size: 13px;
    vertical-align: middle;
}

.regist .loginWraper {
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

.regist .sub_btn {
    transition: all linear 0.5s;
    -moz-transition: all linear 0.5s;
    -webkit-transition: all linear 0.5s;
    -o-transition: all linear 0.5s;
    /* display: inline-block; */
        margin-top: 16px;
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
.registTitle{
        padding: 35px 0;
    font-size: 20px;
    height: 20px;
    line-height: 20px;
    text-align: center;
    color: #000;
}
.regist .cross{
    display: inline-block;
    padding: 0 19px;
    width: 142px;
    margin-left: 0;
    margin-right: 31px;
    margin-top: 16px;
}
.regist .phoneOpen{
        display: inline-block;
    vertical-align: middle;
    width: 130px;
    height: 50px;
    line-height: 50px;
    text-align: center;
    background-color: #f2f2f2;
    font-size: 14px;
    cursor: pointer;
}
.phoneTest{
        margin-top: 8px;
        padding-bottom: 16px;
}
</style>
