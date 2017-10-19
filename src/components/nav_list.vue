<template>
  <div class="container">

      <ul class="menu">
        <li>
          <v-link href="/">商品分类</v-link>
        </li>
        <li>
          <v-link href="/about">品牌</v-link>
        </li>
        <li>
          <v-link href="">最新</v-link>
        </li>
        <li>
          <v-link href="">女士</v-link>
        </li>
        <li>
          <v-link href="">男士</v-link>
        </li>
        <li>
          <v-link href="">生活馆</v-link>
        </li>
        <li>
          <v-link href="">海外馆</v-link>
        </li>
        <li>
          <v-link href="">时尚</v-link>
        </li>
        <li>
          <v-link href="">特惠</v-link>
        </li>
        <li>
          <v-link href="">礼品区</v-link>
        </li>
        <li class="find_store">
          <i></i>
          <v-link href="">到店</v-link>
        </li>

      </ul>
      <ul class="icon_wrap" @mouseleave="hide()">
        <li @mouseenter="show('first')"  :class="{active:isActive.first}">
          <div class="div_list div_list1">
            <a href="">
              <span></span>
              <b>品牌授权,官方验证</b>
            </a>
          </div>
        </li>
        <li @mouseenter="show('second'),axos()"  v-bind:class="{active:isActive.second}">
          <div class="div_list div_list2">
            <a href="">
              <span></span>
              <b>尊享品牌会员服务</b>
            </a>
          </div>
        </li>
        <li @mouseenter="show('third')"  v-bind:class="{active:isActive.third}">
          <div class="div_list div_list3">
            <a href="">
              <span></span>
              <b>商务部诚信示范企业</b>
            </a>
          </div>
        </li>
      </ul>
      <slot></slot>
    </div>
</template>
<script>
import VLink from '../components/VLink.vue'
export default {
  data() {
    return { isActive: {
        first:false,
        second:false,
        third:false
    } }
  },
  components: {
    VLink
  },
  watch: {
    isActive: function() {
      console.log(this)
    }
  },
  methods: {
    show: function(val) {
      for (var key in this.isActive) {
          this.isActive[key] = false;
      }
      this.isActive[val] =true;
    },
    hide: function() {
      for (var key in this.isActive) {
          this.isActive[key] = false;
      }
    },
    //axios AJAXrequest
    axos:function(){
        this.axios.get('/static/json/test.json').then((response) => {
            console.log(response.data)
            })
    }
  }
}
</script>
<style>
.container {
  position: relative;
  width: 100%;
  /* height: 38px; */
  background: url(http://www.5lux.com/vendor/images/v30/navi_1pxbg.png) repeat-x;
  vertical-align: middle;
  /* border-bottom: 1px solid #c9c9c9; */
}

.menu {
  overflow: hidden;
  width: 1210px;
  margin: 0 auto;
  position: relative;
}

.menu>li {
  display: inline-block;
  float: left;
  z-index: 20;
  font-size: 14px;
  text-align: center;
  font-family: "微软雅黑";
  height: 40px;
  line-height: 40px;
}

.menu .find_store:hover>i {
  background-position: -366px -252px;
}

.menu .find_store i {
  display: inline-block;
  float: left;
  width: 19px;
  height: 40px;
  line-height: 40px;
  background: url(http://www.5lux.com/vendor/images/v30/share02.png) no-repeat -58px -169px;
  margin-left: 23px;
}

.icon_wrap {
  margin: 0;
  position: absolute;
  right: 15px;
  top: 0;
  height: 40px;
  line-height: 40px;
  overflow: hidden;
  z-index: 10;
}

.icon_wrap li {
  float: left;
  margin-right: 12px;
  width: 30px;
  overflow: hidden;
  transition: .5s;
}

.icon_wrap .active {
  width: 140px;
}

.icon_wrap li .div_list {
  width: 200px;
  overflow: hidden;
}

.div_list a {
  height: 40px;
  display: inline-block;
}

.div_list a span {
  display: inline-block;
  width: 30px;
  height: 40px;
  line-height: 40px;
  float: left;
  margin-right: 3px;
}

.div_list1 a span {
  background: url(http://www.5lux.com/vendor/images/v30/share02.png) no-repeat -237px -66px;
}

.div_list2 a span {
  background: url(http://www.5lux.com/vendor/images/v30/share02.png) no-repeat -296px -66px;
  ;
}

.div_list3 a span {
  background: url(http://www.5lux.com/vendor/images/v30/share02.png) no-repeat -354px -66px;
}

.div_list a b {
  font-weight: 400;
  float: left;
  color: #fff;
}
</style>


