<template>
    <div class="main_main">
        <div class="brandship">
            <img src="http://www.5lux.com/vendor/images/v30/mainx_brandship.png" alt="无法显示">
        </div>
        <ul class="brandship_list">
            <li v-for="(logo,index) in logoList" @mouseover="logo.logoShow=true" @mouseout="logo.logoShow=false">
                <a href="">
                    <img class="brand_main_img" :src="logo.imgSrc" alt="">
                    <div class="brandship_tbox">
                        <div class="brand_hide" :class="{showbrand:logo.logoShow}">
                            <img class="brandlogopic" :src="logo.logoPic" alt="">
                            <p class="splitline">
                                <span class="blackbar"></span>
                            </p>
                            <p class="enbrand">{{logo.logotitle}}</p>
                            <p class="chnbrand">{{logo.logoName}}</p>
                        </div>
                    </div>
                </a>
            </li>

        </ul>
        <v-hot-store :hotstore="hotStore"></v-hot-store>
        <v-same-store :samestore="storesame"></v-same-store>
        <v-shop-center></v-shop-center>
    </div>
</template>
<script>
import VHotStore from '../components/hot_store.vue'
import VSameStore from '../components/storesame.vue'
import VShopCenter from '../components/ShopCenter.vue'
export default {
    data() {
        return {
            logoList: [
                {
                    logoShow: false,
                    imgSrc: 'src/imgs/14593957951708.jpg',
                    logotitle: 'Rado',
                    logoName: '雷达',
                    logoPic: 'src/imgs/14477432448399.png'
                },
                {
                    logoShow: false,
                    imgSrc: 'src/imgs/14633665089670.jpg',
                    logotitle: 'Breguet',
                    logoName: '宝姬',
                    logoPic: 'src/imgs/14477282116284.png'
                },
                {
                    logoShow: false,
                    imgSrc: 'src/imgs/14656961493524.jpg',
                    logotitle: 'Prada',
                    logoName: '普拉达',
                    logoPic: 'src/imgs/14477432418542.png'
                },
                {
                    logoShow: false,
                    imgSrc: 'src/imgs/150632785246_236x329.jpg',
                    logotitle: 'AlexanderMcqueen',
                    logoName: '亚历山大.麦昆',
                    logoPic: 'src/imgs/14477248162526.png'
                },
                {
                    logoShow: false,
                    imgSrc: 'src/imgs/150209001061_236x329.jpg',
                    logotitle: 'Guerlian',
                    logoName: '娇兰',
                    logoPic: 'src/imgs/14477320365133.png'
                },

            ],
            hotStore:
            {
                hotStoreTitle: 'src/imgs/hotstore_t.jpg',
                //热门旗舰店三个轮波图页面
                hotStoreList:
                {
                    list1: {
                        estee: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee1: {
                            imgSrc: 'src/imgs/14477419323290.png',
                            name: '万宝龙',
                            isShow: false
                        },
                        estee2: {
                            imgSrc: 'src/imgs/14477414658831.png',
                            name: 'MCM',
                            isShow: false
                        },
                        estee3: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee4: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee5: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee6: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee7: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee8: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee9: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee10: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee11: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee12: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee13: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        }
                    },
                    list2: {
                        estee0: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee1: {
                            imgSrc: 'src/imgs/14477419323290.png',
                            name: '万宝龙',
                            isShow: false
                        },
                        estee2: {
                            imgSrc: 'src/imgs/14477414658831.png',
                            name: 'MCM',
                            isShow: false
                        },
                        estee3: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee4: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee5: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee6: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee7: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee8: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee9: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee10: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee11: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee12: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee13: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        }
                    },
                    list3: {
                        estee: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee1: {
                            imgSrc: 'src/imgs/14477419323290.png',
                            name: '万宝龙',
                            isShow: false
                        },
                        estee2: {
                            imgSrc: 'src/imgs/14477414658831.png',
                            name: 'MCM',
                            isShow: false
                        },
                        estee3: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee4: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee5: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee6: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee7: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee8: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee9: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee10: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee11: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee12: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        },
                        estee13: {
                            imgSrc: 'src/imgs/14477312236406.png',
                            name: '雅诗兰黛',
                            isShow: false
                        }
                    }
                }

            },
            storesame: {
                storesametitle: '../../src/imgs/storesametitle.jpg',
                //只用键值对,不用数组
                storeSameList: {
                    storeSameContent: {
                        hotSale: {
                            isShow:true,
                            title:'热卖品牌',
                            last:false,
                            leftPic: 'src/imgs/150753039957_366x515.jpg',
                            list: {
                                list1: {
                                    name: 'Sergio Rossi',
                                    price: '￥ 5399',
                                    salePic: '../../src/imgs/150741123459_1571x2000.JPG'
                                },
                                list2: {
                                    name: 'LACUES',
                                    price: '￥ 88',
                                    salePic: '../../src/imgs/150675183045_800x800.jpg'
                                },
                                list3: {
                                    name: 'Lovers + Friends',
                                    price: '￥ 1558',
                                    salePic: '../../src/imgs/150750398296_505x864_800x800.jpg'
                                },
                                bottom: {
                                    list1: {
                                        name: 'YFB CLOTHING',
                                        price: '￥ 1812',
                                        salePic: 'http://img550.5lux.com.cn/2017/10/10/vw/150759024168_505x864_800x800.jpg'
                                    },
                                    list2: {
                                        name: 'Tiffany & Co.蒂芙尼',
                                        price: '￥ 511680',
                                        salePic: 'http://img550.5lux.com.cn/2017/09/19/gh/150579225278_800x800.jpg'
                                    },
                                    list3: {
                                        name: 'Athletic Propulsion Labs: APL',
                                        price: '￥ 1225',
                                        salePic: 'http://img550.5lux.com.cn/2017/10/10/rs/150759027561_505x864_800x800.jpg'
                                    }
                                }



                            }
                        },
                        newPush: {
                            title:'新品推荐',
                            isShow:false,
                            last:false,
                            leftPic: 'src/imgs/150753039957_366x515.jpg',
                            list: {
                                list1: {
                                    name: 'Sergio Rossi',
                                    price: '￥ 5399',
                                    salePic: '../../src/imgs/150741123459_1571x2000.JPG'
                                },
                                list2: {
                                    name: 'LACUES',
                                    price: '￥ 88',
                                    salePic: '../../src/imgs/150675183045_800x800.jpg'
                                },
                                list3: {
                                    name: 'Lovers + Friends',
                                    price: '￥ 1558',
                                    salePic: '../../src/imgs/150750398296_505x864_800x800.jpg'
                                },
                                bottom: {
                                    list1: {
                                        name: 'YFB CLOTHING',
                                        price: '￥ 1812',
                                        salePic: 'http://img550.5lux.com.cn/2017/10/10/vw/150759024168_505x864_800x800.jpg'
                                    },
                                    list2: {
                                        name: 'Tiffany & Co.蒂芙尼',
                                        price: '￥ 511680',
                                        salePic: 'http://img550.5lux.com.cn/2017/09/19/gh/150579225278_800x800.jpg'
                                    },
                                    list3: {
                                        name: 'Athletic Propulsion Labs: APL',
                                        price: '￥ 1225',
                                        salePic: 'http://img550.5lux.com.cn/2017/10/10/rs/150759027561_505x864_800x800.jpg'
                                    }
                                }



                            }
                        },
                        star: {
                            title:'明星同款',
                            isShow:false,
                            last:true,
                            leftPic: 'src/imgs/150753039957_366x515.jpg',
                            list: {
                                list1: {
                                    name: 'Sergio Rossi',
                                    price: '￥ 5399',
                                    salePic: '../../src/imgs/150741123459_1571x2000.JPG'
                                },
                                list2: {
                                    name: 'LACUES',
                                    price: '￥ 88',
                                    salePic: '../../src/imgs/150675183045_800x800.jpg'
                                },
                                list3: {
                                    name: 'Lovers + Friends',
                                    price: '￥ 1558',
                                    salePic: '../../src/imgs/150750398296_505x864_800x800.jpg'
                                },
                                bottom: {
                                    list1: {
                                        name: 'YFB CLOTHING',
                                        price: '￥ 1812',
                                        salePic: 'http://img550.5lux.com.cn/2017/10/10/vw/150759024168_505x864_800x800.jpg'
                                    },
                                    list2: {
                                        name: 'Tiffany & Co.蒂芙尼',
                                        price: '￥ 511680',
                                        salePic: 'http://img550.5lux.com.cn/2017/09/19/gh/150579225278_800x800.jpg'
                                    },
                                    list3: {
                                        name: 'Athletic Propulsion Labs: APL',
                                        price: '￥ 1225',
                                        salePic: 'http://img550.5lux.com.cn/2017/10/10/rs/150759027561_505x864_800x800.jpg'
                                    }
                                }



                            }
                        },
                    }

                }
            }






        }



    },
    components: {
        VHotStore, VSameStore,VShopCenter
    },
    methods: {
        listenter: function(index) {
            console.log(index)
        }
    }
}
</script>
<style>
img {
    vertical-align: middle;
}

.main_main {
    width: 1210px;
    margin: 0 auto;
    margin-bottom: 50px;
}

.brandship {
    margin-top: 40px;
    margin-bottom: 28px;
}

.brandship_list {
    overflow: hidden;
}

.brandship_list li {
    float: left;
    position: relative;
    margin-right: 8px;
}

.brand_hide img {
    display: block;
}

.brandship_list li .brand_main_img {
    width: 234px;
    height: 329px;
}

.brandship_tbox {

    position: absolute;
    bottom: 1px;
    left: 30px;
    width: 174px;
    height: 154px;
    overflow: hidden;
    z-index: 1;
}

.brandship_tbox .brand_hide {
    transition: top .5s;
    background: #fff;
    width: 106px;
    height: 154px;
    position: absolute;
    top: 100px;
    padding: 0 34px 0 34px;
}

.brand_hide .brandlogopic {
    width: 60px;
    margin: 0 auto;
    margin-top: 10px;
    margin-bottom: 3px;
}

.brand_hide .splitline {
    height: 30px;
    line-height: 0;
    text-align: center;
}

.blackbar {
    display: inline-block;
    width: 20px;
    height: 2px;
    background: #000;
}

.brand_hide .enbrand {
    font-size: 14px;
    text-align: center;
    color: #000;
}

.brand_hide .chnbrand {
    font-size: 14px;
    text-align: center;
    color: #000;
}

.brandship_tbox .showbrand {
    top: 0;
}
</style>
