<template>
    <div class="samestore">
        <div class="same_store_title">
            <img :src="samestore.storesametitle" alt="">
        </div>
        <ul class="storesame_link">
            <li class="storesame_li" v-model="lis" v-for="(title,val,index) in lis.storeSameList.storeSameContent" :style="{background:title.isShow?'black':'grey'}" v-on:mouseenter="changeActive(index,title)">{{title.title}}</li>
        </ul>
        <div class="storesame">
            <ul class="storesame_box" :style="{left:left+'px'}">
                <li class="store_li" v-for="(item,index) in samestore.storeSameList.storeSameContent">
                    <div class="storesameb_left">
                        <a href=""><img class="storesamePic" :src="item.leftPic" alt=""></a>
                    </div>
                    <div class="storesameb_right">
                        <div class="storesameb_top">
                            <div class="storesame_top1" >
                                <div class="storesametoptxt">
                                    <p class="enbrand">{{item.list.list1.name}}</p>
                                    <p>{{item.list.list1.price}}</p>
                                </div>
                                <div class="storesametoppic">
                                    <a href="">
                                        <img class="storePic" :src="item.list.list1.salePic" alt="">
                                    </a>
                                </div>
                            </div>
                            <div class="storesame_top2">
                                <div class="storesametoptxt">
                                    <p class="enbrand">{{item.list.list2.name}}</p>
                                    <p>{{item.list.list1.price}}</p>
                                </div>
                                <div class="storesametoppic">
                                    <a href="">
                                        <img class="storePic" :src="item.list.list2.salePic" alt="">
                                    </a>
                                </div>
                            </div>
                            <div class="storesame_top1">
                                <div class="storesametoptxt">
                                    <p class="enbrand">{{item.list.list3.name}}</p>
                                    <p>{{item.list.list3.price}}</p>
                                </div>
                                <div class="storesametoppic">
                                    <a href="">
                                        <img class="storePic" :src="item.list.list3.salePic" alt="">
                                    </a>
                                </div>
                            </div>
                        </div>
                        <div class="storesameb_bottom">
                            <div class="storesamebottom1" v-for="(bottom,bottomname,bottomindex) in item.list.bottom" :style="{marginRight:bottomindex==2?0:7}">
                                <div class="storesametoptxt" >
                                    <p class="enbrand">{{bottom.name}}</p>
                                    <p>{{bottom.price}}</p>
                                </div>
                                <div class="storesametoppic" >
                                    <a href=""><img class="storePic" :src="bottom.salePic" alt=""></a>
                                </div>
                            </div>
                            <!-- <div>{{item.list.bottom}}</div> -->
                        </div>
                    </div>
                </li>
            </ul>

        </div>
    </div>
</template>
<script>
export default {
    props: ['samestore'],
    data() {
        return { lis: this.samestore,
        activeIndex:0,
        left:0 }

    },
    methods: {
        changeActive: function(index, title) {
            console.log(title);
            // for(var i = 0;i<3;i++){
            //     this.lis.storeSameList.storeSameContent[i].isShow = false;
            // }
            for (var key in this.lis.storeSameList.storeSameContent) {
                if (this.lis.storeSameList.storeSameContent.hasOwnProperty(key)) {
                    this.lis.storeSameList.storeSameContent[key].isShow = false;

                }
            }
            //改变激活的页面
            this.activeIndex = index;
            title.isShow = true;
        }
    },
    watch:{
        //监听激活的页面变化
        activeIndex:function(){
            if (this.activeIndex==0) {
                this.left = 0;
            }else if (this.activeIndex==1) {
                this.left = -1210;
            }else{
                this.left = -2420;
            }
        }
    }
}

</script>
<style>
.storesame_link {
    overflow: hidden;
    margin-bottom: 15px;
    list-style: none;
}

.storesame_link .storesame_li {
    float: left;
    width: 395px;
    height: 30px;
    background: #999;
    color: #fff;
    line-height: 30px;
    text-align: center;
    font-size: 14px;
    margin-right: 8px;
}

.storesame {
    overflow: hidden;
    width: 100%;
    height: 517px;
    position: relative;
}

.storesame .storesame_box {
    position: absolute;
    left: 0;
    width: 9999px;
    transition: .5s;
}

.storesame_box .store_li {
    overflow: hidden;
    float: left;
    width: 1210px;
}

.storesame .storesameb_left {
    float: left;
}

.storesame .storesameb_right {
    float: left;
    margin-left: 9px;
}

.storesameb_left .storesamePic {
    width: 368px;
}

.storesameb_right .storesameb_top {
    overflow: hidden;
    margin-bottom: 8px;
}

.storesameb_right .storesameb_bottom {
    overflow: hidden;
}

.storesameb_right .storesameb_top .storesame_top1 {
    width: 222px;
    height: 248px;
    text-align: center;
    border: 1px solid #ccc;
    overflow: hidden;
    float: left;
}

.storesameb_right .storesameb_top .storesame_top2 {
    overflow: hidden;
    border: 1px solid #ccc;
    text-align: center;
    width: 367px;
    height: 248px;
    float: left;
    margin: 0 7px;
}

.storesameb_top .storesame_top1 .storesametoptxt {
    left: 0;
    font-size: 13px;
    color: #666;
    display: inline-block;
    position: relative;
    transition: .3s;
}

.storesametoppic {
    text-align: center;
    position: relative;
    right: 0;
    transition: .3s;
}

.storesameb_top .storesame_top2 .storesametoptxt {
    font-size: 13px;
    margin-top: 20px;
    margin-left: 70px;
    color: #666;
    display: inline-block;
    position: relative;
    float: left;
}

.enbrand {
    color: #000;
}

.storesametoppic .storePic {
    width: 150px;
}

.storesameb_bottom .storesamebottom1 {
    margin-right: 7px;
    border: 1px solid #ccc;
    float: left;
    width: 271px;
    height: 255px;
    overflow: hidden;
}

.storesametoptxt {
    text-align: center;
    position: relative;
    left: 0;
    transition: .3s;
}
.storesame_top1:hover .storesametoptxt{
    left: -20px;
}
.storesame_top1:hover .storesametoppic{
    right: -20px;
}
.storesame_top2:hover .storesametoptxt{
    left: -20px;
}
.storesame_top2:hover .storesametoppic{
    right: -20px;
}
.storesamebottom1:hover .storesametoptxt{
    left: -20px;
}
.storesamebottom1:hover .storesametoppic{
    right: -20px;
}
</style>
