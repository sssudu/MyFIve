<template>
    <div class="shopcenter">
        <div class="shopcentertitle">
            <img :src="titlePic" alt="">
        </div>
        <ul class="shopcenterul">
            <li class="shopItem" v-for="shop in list">
                <div class="centerbox">
                    <a href="">
                        <div class="topbox">
                            {{shop.name}}
                        </div>
                    </a>
                    <a href="">
                        <div class="bottombox">
                            <div class="border">
                                <p class="en">{{shop.detail}}</p>
                            </div>
                        </div>
                    </a>
                </div>
            </li>
        </ul>
        <v-shop-detail :shop="shop" v-for="shop in list"></v-shop-detail>
    </div>
</template>
<script>
import VShopDetail from '../components/ShopDetail.vue'
export default {
    data() {
        return {
            titlePic: '../../src/imgs/shopcenter.jpg',
            list: {
                shop: {
                    name: '经典箱包',
                    detail:'Classic bags',
                    shopPic:'http://www.5lux.com/vendor/images/v30/goodtitle1.jpg',
                    shopDetailPic:'http://img550.5lux.com.cn/2017/10/09/gh/150753035361_390x370.jpg',
                    swiper:{
                        list1:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list2:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list3:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                    },
                    shopList:['单检包','手提包','手提斜挎包','双肩背包','手拿包','钱包','小披肩','旅行箱/包','斜挎包','化妆箱/包'],
                    shopDetail:['http://img550.5lux.com.cn/2017/10/09/hi/150753898977_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/wx/150753898924_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/ef/150753899028_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/ab/150753899090_275x180.jpg']

                },
                shop1: {
                    name: '典藏腕表',
                    detail:'Collection watches',
                    shopPic:'http://www.5lux.com/vendor/images/v30/goodtitle2.jpg',
                    shopDetailPic:'http://img550.5lux.com.cn/2017/10/09/mn/150753035213_390x370.jpg',
                    swiper:{
                        list1:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list2:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list3:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                    },
                    shopList:['单检包','手提包','手提斜挎包','双肩背包','手拿包','钱包','小披肩','旅行箱/包','斜挎包','化妆箱/包'],
                    shopDetail:['http://img550.5lux.com.cn/2017/10/09/cd/150753899560_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/wx/150753899575_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/mn/150753899680_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/qr/150753899611_275x180.jpg']

                },
                shop2: {
                    name: '精致配饰',
                    detail:'Exquisite accessories',
                    shopPic:'http://www.5lux.com/vendor/images/v30/goodtitle6.jpg',
                    shopDetailPic:'http://img550.5lux.com.cn/2017/10/09/kl/150753035173_390x370.jpg',
                    swiper:{
                        list1:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list2:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list3:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                    },
                    shopList:['单检包','手提包','手提斜挎包','双肩背包','手拿包','钱包','小披肩','旅行箱/包','斜挎包','化妆箱/包'],
                    shopDetail:['http://img550.5lux.com.cn/2017/10/09/np/150753899738_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/fg/150753899747_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/mn/150753899877_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/lm/150753899825_275x180.jpg']

                },
                shop3: {
                    name: '个护化妆',
                    detail:'ENurse makeup',
                    shopPic:'http://www.5lux.com/vendor/images/v30/goodtitle4.jpg',
                    shopDetailPic:'http://img550.5lux.com.cn/2017/10/09/kl/150753035037_390x370.jpg',
                    swiper:{
                        list1:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list2:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list3:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                    },
                    shopList:['单检包','手提包','手提斜挎包','双肩背包','手拿包','钱包','小披肩','旅行箱/包','斜挎包','化妆箱/包'],
                    shopDetail:['http://img550.5lux.com.cn/2017/10/09/rs/150753899024_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/mn/150753899175_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/qr/150753899199_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/ij/150753899233_275x180.jpg']
                    

                },
                shop4: {
                    name: '时尚鞋服',
                    detail:'Shoes and apparel',
                    shopPic:'http://www.5lux.com/vendor/images/v30/goodtitle3.jpg',
                    shopDetailPic:'http://img550.5lux.com.cn/2017/10/09/pq/150753035084_390x370.jpg',
                    swiper:{
                        list1:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list2:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                        list3:{
                            listPic:['http://img.5lux.com.cn/511/avatar/2015/11/17/14477406185992.png','http://img550.5lux.com.cn/2017/05/15/pq/149482910148_214x108.jpg','http://img.5lux.com.cn/511/avatar/2015/11/17/14477378665957.png','http://img.5lux.com.cn/511/avatar/2015/11/17/14477318724845.png']
                        },
                    },
                    shopList:['单检包','手提包','手提斜挎包','双肩背包','手拿包','钱包','小披肩','旅行箱/包','斜挎包','化妆箱/包'],
                    shopDetail:['http://img550.5lux.com.cn/2017/10/09/gh/150753899245_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/vw/150753899386_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/cd/150753899392_275x180.jpg','http://img550.5lux.com.cn/2017/10/09/gh/150753899415_275x180.jpg']

                },
            }

        }
    },
    components:{
        VShopDetail
    }
}
</script>
<style>
.shopcenter .shopcenterul{
    width: 100%;
    overflow: hidden;
}
.shopcenterul li{
    float: left;
    width: 234px;
    height: 50px;
    overflow: hidden;
    position: relative;
    margin-right: 8px;
}
.centerbox{
    top: 0px;
    position: relative;
    transition: .3s;
}
.centerbox .topbox{
    width: 234px;
    height: 50px;
    line-height: 50px;
    background: #999;
    text-align: center;
    font-size: 14px;
    color: #fff;
}
.centerbox .bottombox{
        width: 234px;
    height: 40px;
    padding: 5px;
    background: #333;
    color: #fff;
    text-align: center;
    font-size: 14px;
}

.bottombox .border{
        border: 1px solid #fff;
    width: 223px;
    height: 40px;
}
.border .en{
        margin-top: 10px;
}
.centerbox:hover{
    top: -50px;
}
</style>
