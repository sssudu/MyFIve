<template>
    <div class="DetailTitle">
        <div id="gdetail_con">
            <div class="gimg_box">
                <table>
                    <tbody>
                        <tr>
                            <td>
                                <div class="queryRoom">
                                    <img :src="picList[mainPic]" alt="" class="cloudZoom" :style="{opacity:1}">
                                    <img :src="picList[mainPic]" alt="" class="cloudZoom" :style="{opacity:0}">
                                </div>
                            </td>
                        </tr>
                        <tr>
                            <td>
                                <div class="tango">
                                    <div class="gdg_silder">
                                        <div class="queryNext" @click="queryleftMove(-1)"></div>
                                        <div class="queryPrev" @click="queryleftMove(1)"></div>
                                        <div class="queryClip">
                                            <div class="queryBox">
                                                <ul class="queryList" :style="{left:queryleft+'px'}">
                                                    <li class="queryItem" v-for="(pic,index) in picList" @click="mainPic=index">
                                                        <div class="gimg_wrap">
                                                            <img :src="pic" alt="">
                                                        </div>
                                                    </li>
                                                </ul>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </td>
                        </tr>

                    </tbody>
                </table>
                <ul class="clearfix new-left-content">
                    <li class="new-left-content-list gd30_share">
                        <i class="share"></i>
                        <p class="new-left-content-text">分享</p>
                    </li>
                    <li class="new-left-content-list add_collect_bt" title="7186">
                        <i class="collect"></i>
                        <p class="new-left-content-text">收藏（已有5048人收藏）</p>
                    </li>
                </ul>
            </div>
            <div class="gd_textinfo">
                <ul class="gd_text_con">
                    <li class="bo_xuxian">
                        <dl>
                            <dd class="fsize18 co999">Mont blanc万宝龙</dd>
                            <dd class="fsize18">Montblanc万宝龙 精钢鳄鱼皮自动导航计时码表系列中性表36973</dd>
                            <dd class="co999">货号: 5Lux011089</dd>
                        </dl>
                    </li>
                    <li class="bo_xuxian gd_priceCon b_bo_xuxian fsk_goods_li">
                        <span class="fsk_goods_price">
                            ￥ 27340
                        </span>
                        <span class="fsk_goods_special_price">
                            ￥ 32170
                        </span>
                        <div class="red-card">
                            <span class="red-card-tit">红卡会员价</span>
                        </div>
                        <div class="qr-code">
                            <img class="imgs" src="http://www.5lux.com/vendor/images/v30/qr.jpg" alt="">
                            <i></i>
                            <b></b>
                            <div class="content">
                                <p class="titleP">扫码下载手机客户端</p>
                                <p class="contentP">移动端立减￥100</p>
                            </div>
                        </div>
                    </li>
                    <li class="bo_xuxian">
                        <div class="shopServe">
                            <img src="http://img550.5lux.com.cn/2016/11/01/vw/147798675690_560x40.png" alt="">
                            <a href="" class="a1"></a>
                            <a href="" class="a2"></a>
                        </div>
                    </li>
                    <li class="bo_xuxian" id="gd30_promotebox">
                        <table>
                            <thead>
                                <tr>
                                    <th style="width: 80px">
                                        <span>活动</span>
                                    </th>
                                    <th style="width: 400px"></th>
                                    <th>
                                        <b title="1" class="gd30p_show" style="display:none;"></b>
                                    </th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td style="width: 80px"></td>
                                    <td style="width: 400px" class="gd30pitems">
                                        <dl style="margin-top:-37px">
                                            <a href="http://www.5lux.com/good/detail/134733" target="_blank">
                                                <dd>订单满9999元送价值1199元时尚管家服务</dd>
                                            </a>
                                        </dl>
                                    </td>
                                    <td></td>
                                </tr>
                            </tbody>
                        </table>
                    </li>
                    <li class="bo_xuxian mtop15">
                        <div class="gd_dt">
                            <span>颜色</span>
                        </div>
                        <div class="gd_dd" style="float: none;">
                            <div class="dd_item color_size_cur _ed ">
                                <a href="" class="color_attr  disabled ">
                                    香槟色 </a>
                            </div>
                        </div>
                    </li>
                    <li class="bo_xuxian mtop15">
                        <div class="gd_dt">
                            <span>款型</span>
                        </div>
                        <div class="gd_dd" style="float: none;">
                            <div class="dd_item color_size_cur _ed ">
                                <a href="" class="color_attr  disabled ">
                                    女款 </a>
                            </div>
                        </div>
                    </li>
                    <li class="clearfixgd mtop15 b_bo_xuxian">
                        <div class="gd_dt">
                            <span>数量:</span>
                        </div>
                        <div class="gd_dd" style="width:135px;">
                            <div class="buy_num">
                                <a href="javascript:void(0);" id="reducenum" class="btn_reduce" @click="numbers!=0?numbers--:numbers=0">
                                </a>
                                <a href="javascript:void(0);" id="addnum" class="btn_add" @click="numbers++">
                                </a>
                                <input type="text" v-model="numbers" class="buy_ntext" name="number" id="number">
                            </div>
                        </div>
                    </li>
                    <li class="gd_priceCon mtop15" id="gd30_hintbox">
                        <dl>
                            <dt>发货门店</dt>
                            <dd>此货品将由
                                <span class="gd30hstore">第五大道奢侈品网</span> 为您发货。</dd>
                        </dl>
                        <dl>
                            <dt>发货时效</dt>
                            <dd>预计3-5个工作日发货，延迟发货慢必赔！
                                <span class="look_btn" style="cursor:pointer;">查看详情 》</span>
                            </dd>
                        </dl>
                        <dl>
                            <dt>包邮政策</dt>
                            <dd>白金钻石顺丰包邮，注册用户满99元免邮
                                <!--（稀奇艺术品牌及货到付款除外）-->
                            </dd>
                        </dl>
                    </li>
                    <li class="clearfixgd mtop15" style="position:relative;">
                        <div class="buy_btn" style="margin-left:10px;" id="v30_nowbuy_btn">
                            <a href="javascript:;" id="go-buy">
                                <span class="v30_btmid">立即购买</span>
                            </a>
                        </div>
                        <div class="add_car_btn">
                            <a class="goods_add_fav" href="javascript:void(0)">
                                <span>加入购物袋</span>
                                <b></b>
                            </a>
                        </div>
                    </li>
                </ul>
                <ul class="clearfix new-right-content" style="padding-bottom:20px;">
                    <!--            <li class="new-right-content-list">
                                                    <i class="gf"></i>
                                                    <p class="new-right-content-text">品牌官方授权</p>
                                            </li>-->
                    <li class="new-right-content-list">
                        <i class="zhp"></i>
                        <p class="new-right-content-text">100%正品保证</p>
                    </li>
                    <li class="new-right-content-list">
                        <i class="bs"></i>
                        <p class="new-right-content-text">商务部诚信企业</p>
                    </li>
                    <li class="new-right-content-list" style="margin-right: 0;">
                        <i class="wyshb"></i>
                        <p class="new-right-content-text">无忧售后保障</p>
                    </li>
                </ul>
            </div>
        </div>

        <div id="gd30_taball" class="" style="top: 0px; left: 0px; z-index: 3; position: relative;">
            <div class="gd30tb_main">
                <div class="gd30tbm_b">
                    <div class="gd30tmb_head">
                        第五大道奢侈品网
                        <b></b>
                    </div>
                </div>
                <div class="gd30tbm_i">
                    <ul class="gd30btmi_swith">
                        <li class="_ed">商品详情
                            <b></b>
                        </li>
                        <li>尺寸参照
                            <b></b>
                        </li>
                        <li id="comment">商品评价
                            <b></b>
                        </li>
                    </ul>
                    <div class="gd30tbmi_qrcode">
                        <span>手机购买</span>
                        <i></i>
                        <b></b>
                        <div class="gd30tbmiq" style="display: none;">
                            <div class="mobile-weima">
                                <canvas width="128" height="128"></canvas>
                            </div>
                            <span>扫一扫，手机购买</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div id="gd30_main">
            <div class="goodsContent_left">
                <div class="v30_sideitem" style="padding-top:10px;">
                    <dl>
                        <dt>热销排行</dt>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204192">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2016/10/11/tu/147616923971_800x800_200x200.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_深棕色表带白色表盘中性针扣石英腕表 DW1123" title="Daniel Wellington/DW 丹尼尔·惠灵顿_深棕色表带白色表盘中性针扣石英腕表 DW1123">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">1</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204192" title="深棕色表带白色表盘中性针扣石英腕表 DW1123">深棕色表带白色表盘中性针扣石英腕表 DW1123</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1628</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204249">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2016/10/13/jk/147632425855_800x800_200x200.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_蓝白紫拼色尼龙表带白色表盘女士针扣石英腕表 DW0609" title="Daniel Wellington/DW 丹尼尔·惠灵顿_蓝白紫拼色尼龙表带白色表盘女士针扣石英腕表 DW0609">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">2</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204249" title="蓝白紫拼色尼龙表带白色表盘女士针扣石英腕表 DW0609">蓝白紫拼色尼龙表带白色表盘女士针扣石英腕表 DW0609</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1100</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204237">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2016/10/12/ab/147625227129_800x800_200x200.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_黑色牛皮表带白色表盘男士针扣石英腕表 DW1101" title="Daniel Wellington/DW 丹尼尔·惠灵顿_黑色牛皮表带白色表盘男士针扣石英腕表 DW1101">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">3</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204237" title="黑色牛皮表带白色表盘男士针扣石英腕表 DW1101">黑色牛皮表带白色表盘男士针扣石英腕表 DW1101</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1759</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204239">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2016/10/12/ab/147626145756_800x800.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_蓝红白条纹尼龙表带白色表盘男士针扣石英腕表 DW0213" title="Daniel Wellington/DW 丹尼尔·惠灵顿_蓝红白条纹尼龙表带白色表盘男士针扣石英腕表 DW0213">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">4</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204239" title="蓝红白条纹尼龙表带白色表盘男士针扣石英腕表 DW0213">蓝红白条纹尼龙表带白色表盘男士针扣石英腕表 DW0213</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1188</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204246">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2016/10/13/bc/147632084425_800x800_200x200.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_棕色皮带白色表盘男士针扣石英腕表 DW0211" title="Daniel Wellington/DW 丹尼尔·惠灵顿_棕色皮带白色表盘男士针扣石英腕表 DW0211">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">5</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204246" title="棕色皮带白色表盘男士针扣石英腕表 DW0211">棕色皮带白色表盘男士针扣石英腕表 DW0211</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1452</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/1898936">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2017/05/15/cd/149483840573_800x800_200x200.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_Classic系列 白色圆盘编织金属石英腕表 DW00100163" title="Daniel Wellington/DW 丹尼尔·惠灵顿_Classic系列 白色圆盘编织金属石英腕表 DW00100163">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">6</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/1898936" title="Classic系列 白色圆盘编织金属石英腕表 DW00100163">Classic系列 白色圆盘编织金属石英腕表 DW00100163</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1136</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204240">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2016/10/12/cd/147626442336_800x800.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_棕色牛皮表带白色表盘中性针扣石英腕表 DW1122" title="Daniel Wellington/DW 丹尼尔·惠灵顿_棕色牛皮表带白色表盘中性针扣石英腕表 DW1122">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">7</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204240" title="棕色牛皮表带白色表盘中性针扣石英腕表 DW1122">棕色牛皮表带白色表盘中性针扣石英腕表 DW1122</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1628</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/181989">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/04/05/14598288442431_200x200.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_蓝白红拼色尼龙表带白色表盘男士针扣石英腕表 DW0103" title="Daniel Wellington/DW 丹尼尔·惠灵顿_蓝白红拼色尼龙表带白色表盘男士针扣石英腕表 DW0103">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">8</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/181989" title="蓝白红拼色尼龙表带白色表盘男士针扣石英腕表 DW0103">蓝白红拼色尼龙表带白色表盘男士针扣石英腕表 DW0103</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1188</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/7186">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/07/21/14690895117407.jpg" alt="Armani阿玛尼_香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表  AR0155" title="Armani阿玛尼_香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表  AR0155">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">9</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/7186" title="香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表  AR0155">香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表 AR0155</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 899</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204175">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2016/10/11/np/147616388478_800x800_200x200.jpg" alt="Daniel Wellington/DW 丹尼尔·惠灵顿_棕色表带白色表盘男士针扣石英腕表 DW1120" title="Daniel Wellington/DW 丹尼尔·惠灵顿_棕色表带白色表盘男士针扣石英腕表 DW1120">
                                            <div><img src="http://img550.5lux.com.cn/2016/11/21/rs/147971379779_30x30.png" style="position: absolute;left:0px;top: 5px;width: 30px;height: 30px;margin: 0;">
                                                <p style="position: absolute;top: 5px;left:0px;display: block;width: 18px;height: 30px;text-align: center;line-height: 20px;font-size: 12px;color: #fff;">10</p>
                                            </div>
                                        </div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/204175" title="棕色表带白色表盘男士针扣石英腕表 DW1120">棕色表带白色表盘男士针扣石英腕表 DW1120</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1759</li>
                            </ul>
                        </dd>
                    </dl>
                </div>
                <div class="v30_sideitem" style="padding-top:30px;">
                    <dl>
                        <dt>同品牌推荐</dt>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/34530">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2014/07/30/14066984207845.jpg" alt="Armani阿玛尼_金色表盘绿色表带男士手表 AR1722" title="Armani阿玛尼_金色表盘绿色表带男士手表 AR1722"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/34530" title="金色表盘绿色表带男士手表 AR1722">金色表盘绿色表带男士手表 AR1722</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 899</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/13404">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/02/24/14563080092079.jpg" alt="Armani阿玛尼_宝石蓝圆形表盘银色精钢表带男士石英腕表 AR2448" title="Armani阿玛尼_宝石蓝圆形表盘银色精钢表带男士石英腕表 AR2448"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/13404" title="宝石蓝圆形表盘银色精钢表带男士石英腕表 AR2448">宝石蓝圆形表盘银色精钢表带男士石英腕表 AR2448</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1290</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/27491">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/08/05/14703796045563.jpg" alt="Armani阿玛尼_蓝色圆盘表带单眼计时石英男士腕表 AR1647" title="Armani阿玛尼_蓝色圆盘表带单眼计时石英男士腕表 AR1647"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/27491" title="蓝色圆盘表带单眼计时石英男士腕表 AR1647">蓝色圆盘表带单眼计时石英男士腕表 AR1647</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1290</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/20643">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/2016/08/18/gh/147150342510_500x500.jpg" alt="Armani阿玛尼_银色圆盘表带石英女士腕表 AR5961" title="Armani阿玛尼_银色圆盘表带石英女士腕表 AR5961"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/20643" title="银色圆盘表带石英女士腕表 AR5961">银色圆盘表带石英女士腕表 AR5961</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 999</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/22530">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/07/28/14696855857001.jpg" alt="Armani阿玛尼_香槟色圆盘表带石英女士腕表 AR2039" title="Armani阿玛尼_香槟色圆盘表带石英女士腕表 AR2039"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/22530" title="香槟色圆盘表带石英女士腕表 AR2039">香槟色圆盘表带石英女士腕表 AR2039</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1390</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/20808">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/08/09/14707298589467.jpg" alt="Armani阿玛尼_褐色圆形三眼表盘不锈钢表带男士石英腕表 AR2454" title="Armani阿玛尼_褐色圆形三眼表盘不锈钢表带男士石英腕表 AR2454"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/20808" title="褐色圆形三眼表盘不锈钢表带男士石英腕表 AR2454">褐色圆形三眼表盘不锈钢表带男士石英腕表 AR2454</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1490</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/24433">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/08/08/14706459962212.jpg" alt="Armani阿玛尼_黑色圆形不锈钢表盘表带男士石英腕表 AR0382" title="Armani阿玛尼_黑色圆形不锈钢表盘表带男士石英腕表 AR0382"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/24433" title="黑色圆形不锈钢表盘表带男士石英腕表 AR0382">黑色圆形不锈钢表盘表带男士石英腕表 AR0382</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1190</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/14215">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/2016/08/16/np/147131000951_800x800.jpg" alt="Armani阿玛尼_棕色橡胶表带圆形多功能三眼男表 AR5890" title="Armani阿玛尼_棕色橡胶表带圆形多功能三眼男表 AR5890"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/14215" title="棕色橡胶表带圆形多功能三眼男表 AR5890">棕色橡胶表带圆形多功能三眼男表 AR5890</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1290</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/33603">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/07/29/14697847534472.jpg" alt="Armani阿玛尼_宝蓝色优雅珍珠彩贝女士石英腕表 AR7330" title="Armani阿玛尼_宝蓝色优雅珍珠彩贝女士石英腕表 AR7330"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/33603" title="宝蓝色优雅珍珠彩贝女士石英腕表 AR7330">宝蓝色优雅珍珠彩贝女士石英腕表 AR7330</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1490</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/29473">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/08/04/14702747344728.jpg" alt="Armani阿玛尼_玫瑰金色方形表盘表带石英女士腕表 AR1655" title="Armani阿玛尼_玫瑰金色方形表盘表带石英女士腕表 AR1655"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/29473" title="玫瑰金色方形表盘表带石英女士腕表 AR1655">玫瑰金色方形表盘表带石英女士腕表 AR1655</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1090</li>
                            </ul>
                        </dd>
                    </dl>
                </div>
                <div class="v30_sideitem" style="padding-top:30px;">
                    <dl>
                        <dt>浏览记录</dt>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/7186">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2016/07/21/14690895117407.jpg" alt="Armani阿玛尼_香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表  AR0155" title="Armani阿玛尼_香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表  AR0155"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/7186" title="香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表  AR0155">香槟色表盘咖啡色鳄鱼压纹表带方形石英奢华女士手表 AR0155</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 899</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2767662">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2017/10/12/ab/150780720162_897x1296_200x200.jpg" alt="See by Chloe_焦糖色mini双肩背包" title="See by Chloe_焦糖色mini双肩背包"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2767662" title="焦糖色mini双肩背包">焦糖色mini双肩背包</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 3698</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/11089">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2015/08/24/14403843423406.jpg" alt="Mont blanc万宝龙_Montblanc万宝龙 精钢鳄鱼皮自动导航计时码表系列中性表36973" title="Mont blanc万宝龙_Montblanc万宝龙 精钢鳄鱼皮自动导航计时码表系列中性表36973"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/11089" title="Montblanc万宝龙 精钢鳄鱼皮自动导航计时码表系列中性表36973">Montblanc万宝龙 精钢鳄鱼皮自动导航计时码表系列中性表36973</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 27340</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2767415">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2017/10/12/np/150776647648_990x1320_200x200.jpg" alt="TAGLIATORE_Tagliatore Clothing Fall/Winter 2017/2018" title="TAGLIATORE_Tagliatore Clothing Fall/Winter 2017/2018"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2767415" title="Tagliatore Clothing Fall/Winter 2017/2018">Tagliatore Clothing Fall/Winter 2017/2018</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 4136</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2767402">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2017/10/12/gh/150776633124_990x1320_200x200.jpg" alt="Fendi芬迪_Fendi Clothing Fall/Winter 2017/2018" title="Fendi芬迪_Fendi Clothing Fall/Winter 2017/2018"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2767402" title="Fendi Clothing Fall/Winter 2017/2018">Fendi Clothing Fall/Winter 2017/2018</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 5640</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2764631">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2017/10/10/st/150760920314_897x1296_200x200.jpg" alt="Acne Studios 艾克妮_Pansy蓝色笑脸帽" title="Acne Studios 艾克妮_Pansy蓝色笑脸帽"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2764631" title="Pansy蓝色笑脸帽">Pansy蓝色笑脸帽</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1224</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/64713">
                                        <div style="position:relative;text-align: center;"><img src="http://img.5lux.com.cn/511/avatar/2015/03/19/14267292328979_200x200.jpg" alt="Dior迪奥_蓝色小羊皮“Diorama”覆盖式中号手提包" title="Dior迪奥_蓝色小羊皮“Diorama”覆盖式中号手提包"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/64713" title="蓝色小羊皮“Diorama”覆盖式中号手提包">蓝色小羊皮“Diorama”覆盖式中号手提包</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 32500</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2762457">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2017/10/09/mn/150750364199_505x864_200x200.jpg" alt="Heartloom_BELLE 毛衣" title="Heartloom_BELLE 毛衣"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2762457" title="BELLE 毛衣">BELLE 毛衣</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 695</li>
                            </ul>
                        </dd>
                        <dd>
                            <ul style="border-bottom: solid #e5e5e5 1px;margin: 0 20px; text-align:left;">
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2764368">
                                        <div style="position:relative;text-align: center;"><img src="http://img550.5lux.com.cn/2017/10/10/vw/150759024168_505x864_200x200.jpg" alt="YFB CLOTHING_LANE 连身裤" title="YFB CLOTHING_LANE 连身裤"></div>
                                    </a>
                                </li>
                                <li>
                                    <a href="http://www.5lux.com/good/detail/2764368" title="LANE 连身裤">LANE 连身裤</a>
                                </li>
                                <li style="font-family:'微软雅黑'; color:#c8a985; padding-bottom:20px;">¥ 1812</li>
                            </ul>
                        </dd>
                    </dl>
                </div>
            </div>
            <div class="goodsContent_right">
                <ul>
                    <li>
                        <div class="product-recommend">
                            <div class="product-rec-banner img-warp">
                                <a href=""><img src="http://img550.5lux.com.cn/2017/10/12/de/150777952298_1440x520.jpg" alt=""></a>
                            </div>
                            <div class="product-rec-warp clearfix">
                                <div class="product-rec-list img-warp fl">
                                    <a href="">
                                        <img src="http://img550.5lux.com.cn/2017/10/11/tu/150769005749_750x560.jpg" alt="">
                                    </a>
                                </div>
                                <div class="product-rec-list img-warp fr">
                                    <a href=""><img src="http://img550.5lux.com.cn/2017/10/10/wx/150760374664_750x560.jpg" alt=""></a>
                                </div>
                            </div>
                        </div>

                        <ul class="common-detail-warp">
                            <li class="common-detail-list">
                                <div class="common-title">
                                    <img src="http://www.5lux.com/vendor/images/good/detail_desc/brand_story.jpg" alt="">
                                </div>
                                <div id="goodstory-box">
                                    <div class="goodstory-left">
                                        <img src="http://img550.5lux.com.cn/2017/09/19/ef/150578863532_400x244.jpg" alt="">
                                    </div>
                                    <div class="goodstory-right">
                                        <div class="goodstory-title">

                                            Mont blanc万宝龙
                                        </div>
                                        <div class="goodstory-content">

                                            万宝龙意指欧洲高峰——勃朗峰(MONT BLANC)，成立于1906年。1908年发表款高品质安全钢笔——“红与黑”。1910年以“MONT BLANC”注册成为正式商标。1924年万宝龙经典之件MEISTERSTUCK大班笔隆重面世。1935年开始生产小皮件。1992年推出限量发行的大文豪系列及艺术赞助人系列(又名帝皇系列)。2000年，万宝龙以波希米亚系列开创了书写艺术的新篇章，设计简洁流畅，小巧典雅，成为现代流行文化的新符号。
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <div class="goods_detail tab_list">
                                <table>
                                    <tbody>
                                        <tr>
                                            <td><img src="http://img.5lux.com.cn/511/avatar/2014/06/12/14025681786341.jpg" alt=""></td>
                                        </tr>
                                        <tr>
                                            <td><img src="http://img.5lux.com.cn/511/2016/08/31/jk/147260732714_800x1107.jpg" alt=""></td>
                                        </tr>
                                        <tr>
                                            <td><img src="http://img.5lux.com.cn/511/avatar/2014/06/12/14025681797042.jpg" alt=""></td>
                                        </tr>
                                        <tr>
                                            <td>
                                                <span>古典与经典往往集于一身。当科技在我们的生活中日新月异地发展时，古老文化的魔力演化成了心中的艺术品。“放缓脚步，尽享生命”正是Montblanc万宝龙的哲学。在万宝龙的产品中，可以看到人类用时间磨砺出的精神光芒，看到一段沉淀了近百年的文化。简洁的线条以及硬朗的外观，无时无刻不体现“大男人”的风范。</span>
                                            </td>
                                        </tr>
                                        <tr>
                                            <td><img src="http://img.5lux.com.cn/511/avatar/2014/06/12/14025681781664.jpg" alt=""></td>
                                        </tr>
                                        <tr>
                                            <td>
                                                <table border="0" class="ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border">
                                                    <tbody>
                                                        <tr>
                                                            <td>
                                                                <table border="0" class="goods_msg ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border ke_show_border">
                                                                    <tbody>
                                                                        <tr>
                                                                            <td class="gtitle"> 商品品牌&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> Montblanc万宝龙 </td>
                                                                            <td class="gtitle"> 产品款式&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 男款 </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> 产品型号&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 36967 </td>
                                                                            <td class="gtitle"> 产品颜色&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 银色表盘/黑色表带<br> </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> 机芯类型&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 自动机械机芯 </td>
                                                                            <td class="gtitle"> 产品产地&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 瑞士&nbsp; </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> 产品尺寸&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 表壳尺寸42mm[所有测量尺寸均取近似值]&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtitle"> 手表厚度&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 约
                                                                                <span style="color: rgb(0, 0, 0); font-family: Arial, Verdana, 宋体, sans-serif; font-size: small; line-height: 22px">14.5</span>mm </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> 表底形式&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 透底 </td>
                                                                            <td class="gtitle"> 表镜形式&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 蓝宝石水晶玻璃 </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> 表盘形状&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 圆形 </td>
                                                                            <td class="gtitle"> 产品材质&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext">
                                                                                <p> 精钢表壳/
                                                                                    <span style="line-height: 19.0909080505371px">鳄鱼皮表带</span>
                                                                                </p>
                                                                            </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> 表扣形式&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 折叠扣 </td>
                                                                            <td class="gtitle"> 表冠形式&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 普通 </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> 产品功能&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 两地时、计时码表、日历 </td>
                                                                            <td class="gtitle"> 防水性能&nbsp;&nbsp;&nbsp;&nbsp; </td>
                                                                            <td class="gtext"> 防水 30米 </td>
                                                                        </tr>
                                                                        <tr>
                                                                            <td class="gtitle"> <br> </td>
                                                                            <td class="gtext"> <br> </td>
                                                                            <td class="gtitle"> <br> </td>
                                                                            <td class="gtext"> <br> </td>
                                                                        </tr>
                                                                    </tbody>
                                                                </table>
                                                            </td>
                                                        </tr>
                                                    </tbody>
                                                </table>
                                            </td>
                                        </tr>
                                        <tr>
                                            <td><img src="http://img.5lux.com.cn/511/avatar/2014/06/12/14025681792236.jpg" alt=""></td>
                                        </tr>
                                        <tr>
                                            <td>
                                                <p><img src="http://img.5lux.com.cn/511/avatar/2015/08/24/14403824204410.jpg" alt=""></p>
                                                <p><img src="http://img.5lux.com.cn/511/avatar/2015/08/24/14403824209075.jpg" alt=""></p>
                                                <p><img src="http://img.5lux.com.cn/511/avatar/2015/08/24/14403824195596.jpg" alt=""></p>
                                                <p><img src="http://img.5lux.com.cn/511/avatar/2015/08/24/14403824196890.jpg" alt=""></p>
                                                <p><img src="http://img.5lux.com.cn/511/avatar/2015/08/24/14403824187920.jpg" alt=""></p>
                                                <p><img src="http://img.5lux.com.cn/511/avatar/2015/08/24/14403824188616.jpg" alt=""></p>
                                            </td>
                                        </tr>
                                        <tr>
                                            <td><img src="" alt=""></td>
                                        </tr>
                                        <tr>
                                            <td><img src="" alt=""></td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                            <li class="common-detail-list">
                                <div class="common-title">
                                    <img src="http://www.5lux.com/vendor/images/good/detail_desc/authenticity_guarantee.jpg" alt="">
                                </div>
                                <div id="realproduct-box">
                                    <div class="realproduct-content img-warp">
                                        <a href=""><img src="http://img550.5lux.com.cn/2017/09/01/mn/150425812560_1440x520.jpg" alt=""></a>
                                    </div>
                                </div>
                            </li>
                            <li class="common-detail-list">
                                <div class="common-title">
                                    <img src="http://www.5lux.com/vendor/images/good/detail_desc/about_5lux.jpg" alt="">
                                </div>
                                <div class="realproduct-content img-warp">
                                    <a href=""><img src="http://img550.5lux.com.cn/2017/09/01/mn/150425812560_1440x520.jpg" alt=""></a>
                                </div>
                                <div class="realproduct-content img-warp" style="margin-top:20px">
                                    <a href=""><img src="http://img550.5lux.com.cn/2017/09/04/np/150452213531_870x314.jpg" alt=""></a>
                                </div>
                            </li>
                            <li class="common-detail-list">
                                <div>
                                    <img src="http://www.5lux.com/vendor/images/good/detail_desc/you_may_also_like.jpg" alt="">
                                </div>
                                <div>
                                    <img src="" alt="">
                                </div>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>

    </div>
</template>
<script>
import TWEEN from '../../static/tween/tween.js'
export default {
    data() {
        return {
            queryleft: 0,
            mainPic: 3,
            picList: ['http://img.5lux.com.cn/511/avatar/2015/08/24/14403843423406.jpg', 'http://img.5lux.com.cn/511/avatar/2015/08/24/14403843423406.jpg', 'http://img.5lux.com.cn/510/images/201011/source_img/11089_P_1289783877946.jpg', 'http://img.5lux.com.cn/510/images/201011/source_img/11089_P_1289783974975.jpg',],
            numbers: 1
        }
    },
    methods: {
        queryleftMove: function(direction) {

            this.queryleft += direction * 86.5
            if (this.queryleft > 0) {
                this.queryleft = 0
            }
        }
    }
}
</script>
<style>
body {
    font-family: "microsoft yahei", 微软雅黑, Helvetica, Arial, Tahoma, 黑体, 宋体, sans-serif;
    font-size: 12px;
}

* {
    margin: 0;
    padding: 0;
}

.fl {
    float: left;
}

.fr {
    float: right;
}

.tab_list table {
    font: 12px/200% 'microsoft yahei', 微软雅黑, Helvetica, Arial, Tahoma, 黑体, 宋体, sans-serif;
}

#goodstory-box .goodstory-title {
    width: 432px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    font-size: 16px;
    font-weight: bold;
    overflow: hidden;
}

#goodstory-box .goodstory-content {
    width: 425px;
    height: auto;
    text-indent: 2em;
    padding: 5px;
    overflow: hidden;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 8;
}

#goodstory-box .goodstory-left {
    width: 410px;
    height: 244px;
    float: left;
}

#goodstory-box .goodstory-right {
    width: 435px;
    height: 244px;
    float: right;
    overflow: hidden;
}

.common-detail-warp .common-title {
    width: 870px;
    height: 98px;
}

#goodstory-box {
    border: 1px solid #CCDDFF;
    width: 850px;
    height: 244px;
    margin: 0 auto;
    background: #F5F5F5;
}

.goodsContent_right .product-rec-warp {
    margin-top: 10px;
    display: block;
}

.product-recommend {
    margin-top: 15px;
}

.product-rec-list {
    width: 430px;
    height: 321px;
    overflow: hidden;
}

.product-rec-banner {
    width: 100%;
    height: 314px;
    overflow: hidden;
}

.img-warp a {
    display: inline-block;
    width: 100%;
    height: 100%;
    margin-left: 0px;
    margin-top: 0px;
}

.img-warp img {
    width: 100%;
    height: 100%;
}

.v30_sideitem dl {
    display: block;
    width: 198px;
    border: 1px solid #c9c9c9;
}

.v30_sideitem dl dt {
    width: 198px;
    text-align: center;
    line-height: 33px;
    color: #fff;
    background: #bfa69a;
}

.v30_sideitem dl dd {
    width: 198px;
    text-align: center;
    line-height: 30px;
    color: #666;
    clear: both;
    margin-top: 20px;
}

.v30_sideitem dl dd a {
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    word-break: break-all;
    line-height: 20px;
}

.v30_sideitem dl dd img {
    width: 136px;
    margin: 5px auto;
    clear: both;
}

.v30_btmid {
    display: inline-block;
    font-size: 14px;
    color: #c8a985;
    line-height: 33px;
    height: 33px;
    width: 118px;
    border: 1px solid #c8a985;
    text-align: center;
}

.mtop15 {
    margin-top: 15px;
}

.shopServe {
    position: relative;
}

.shopServe .a1 {
    position: absolute;
    width: 220px;
    height: 40px;
    left: 71px;
    top: 0px;
}

.shopServe .a2 {
    position: absolute;
    width: 50px;
    height: 40px;
    left: 298px;
    top: 0px;
}

.qr-code {
    float: right;
    width: 200px;
    height: 30px;
    position: relative;
    margin-top: 6px;
    cursor: pointer;
}

p {
    margin: 0;
}

.qr-code .titleP {
    line-height: 14px;
    color: rgb(102, 102, 102);
}

.qr-code .contentP {
    line-height: 14px;
    color: #ff3333;
}

.qr-code .content {
    position: absolute;
    width: 120px;
    top: 0;
    left: 43px;
    height: 26px;
}

.qr-code i {
    display: inline-block;
    width: 27px;
    height: 26px;
    background: url(http://img550.5lux.com.cn/2017/06/09/qr/149697742783_27x26.jpg) no-repeat;
}

.qr-code b {
    display: inline-block;
    width: 12px;
    height: 26px;
    margin: 0px 2px;
    background: url(http://img550.5lux.com.cn/2017/06/16/wx/149761259453_12x26.png) no-repeat;
}

.qr-code .imgs {
    display: none;
    position: absolute;
    left: 0px;
    top: 30px;
    z-index: 90;
}

.red-card {
    position: relative;
    display: inline-block;
    cursor: pointer;
}

.red-card .red-card-tit {
    display: inline-block;
    text-align: center;
    width: 80px;
    height: 20px;
    line-height: 20px;
    font-size: 12px;
    color: #fff;
    background: #c8a985;
    border-radius: 10px;
}

.li2 {
    position: relative;
    padding: 10px 0 10px;
}

.DetailTitle {
    overflow: hidden;
}

.gimg_box {
    width: 480px;
    float: left;
}

.queryRoom {
    border: solid 1px #EAEAEA;
    width: 478px;
    height: 478px;
    overflow: hidden;
    text-align: center;
    position: relative;
}

.cloudZoom {
    position: absolute;
    left: 0px;
    top: 0px;
    right: 0px;
    bottom: 0px;
    margin: auto;
    width: auto;
    height: 100%;
    transition: .5s;
}

.tango {
    overflow: hidden;
}

.gdg_silder {
    width: 480px;
    padding: 25px 0;
    position: relative;
}

.gdg_silder .queryNext {
    position: absolute;
    top: 25px;
    right: 0;
    width: 15px;
    height: 87px;
    cursor: pointer;
    background: transparent url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -73px -362px;
    background-color: #f2f2f2;
    z-index: 100;
}

.gdg_silder .queryPrev {
    position: absolute;
    top: 25px;
    left: 0;
    width: 15px;
    height: 87px;
    cursor: pointer;
    background: transparent url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -32px -362px;
    background-color: #f2f2f2;
    z-index: 100;
}

.queryClip {
    z-index: 1;
    padding: 0;
    margin: 0;
    overflow: hidden;
    position: relative;
    width: 1000px;
    height: 87px;
    padding-left: 13px;
}

.queryClip .queryBox {
    position: absolute;
    overflow: hidden;
    width: 100%;
    height: 100%;
}

.queryClip .queryList {
    z-index: 1;
    overflow: hidden;
    position: relative;
    top: 0;
    left: 0;
    margin: 0;
    padding: 0;
    width: 99999px;
    transition: .5s;
}

.queryList .queryItem {
    width: 85px;
    height: 87px;
    padding: 0 3px;
    text-align: center;
    float: left;
}

.queryList .queryItem .gimg_wrap {
    height: 85px;
    width: 83px;
    overflow: hidden;
    position: relative;
    border: 1px solid #ccc;
}

.queryList .queryItem .gimg_wrap img {
    height: 85px;
    margin: 0 auto;
}

.gd_textinfo {
    width: 560px;
    min-height: 615px;
    overflow: hidden;
    float: left;
    padding-left: 60px;
    overflow-x: hidden;
}

.gd_text_con {
    width: 100%;
}

.gd_text_con .bo_xuxian {
    border-bottom: 1px dotted #bfbfbf;
}

.fsize18 {
    font-size: 18px;
}

.co999 {
    color: #999;
}











/*
To change this license header, choose License Headers in Project Properties.
To change this template file, choose Tools | Templates
and open the template in the editor.
*/


/* 
    Created on : 2015-8-16, 21:32:42
    Author     : cyndi
*/

#gdetail_con {
    width: 1100px;
    margin: 0 auto;
    overflow: hidden;
    zoom: 1;
    margin-top: 15px;
}

.gimg_box {
    width: 480px;
    float: left;
}

.jqueryzoom {
    position: relative;
    padding: 0;
}

.jqueryzoom img {
    width: 480px;
}

.gd_textinfo {
    width: 560px;
    min-height: 615px;
    overflow: hidden;
    float: left;
    padding-left: 60px;
    overflow-x: hidden;
}

.gd_text_con {
    width: 100%;
}

.gd_text_con li {
    display: block;
}

.clearfixgd {
    width: 100%;
    overflow: hidden;
    zoom: 1;
}

.b_bo_xuxian {
    border-bottom: 1px dotted #bfbfbf;
}

.gd_text {
    display: inline-block;
    float: left;
}

.gd_title {
    overflow: hidden;
    zoom: 1;
}

.gd_title a {
    font-size: 18px;
    cursor: pointer;
    font-weight: bold;
    text-decoration: none;
}

.gd_title {
    overflow: hidden;
    zoom: 1;
}

.gd_desc {
    padding: 3px 0px;
}

.gd_priceCon {
    /*    height: 45px;
    line-height: 45px;*/
    vertical-align: middle;
    position: relative;
}

.gd_price {
    font-size: 14px;
    color: #d00000;
    font-family: "å¾®è½¯é›…é»‘";
}

.gd_price span {
    font-size: 20px;
    margin-left: 8px;
}

.gd_priceCon img {
    cursor: pointer;
    position: absolute;
    top: 12px;
    left: 229px;
}

.gd_priceCon .mbprice_wrap {
    width: 175px;
    height: 90px;
    position: absolute;
    left: 307px;
    top: 12px;
    display: none;
    z-index: 19;
}

.mbprice_wrap .mbprice_title {
    height: 30px;
    line-height: 30px;
    font-size: 12px;
    text-align: center;
    background-color: #222325;
}

.mbprice_wrap .mbprice_title a,
.mbprice_wrap .mbprice_title a:hover {
    color: #fff;
}

.mbprice_list_wrap {
    border: 1px solid #c7c7c7;
    background: #fff;
}

.mbprice_wrap .mbprice_list_wrap ul {
    margin: 6px 15px;
}

.mbprice_wrap .mbprice_list_wrap ul li {
    line-height: 17px;
}

.f_8c8a8a {
    color: #8c8a8a;
}

.gd_dt {
    width: 80px;
    float: left;
    padding-left: 13px;
    text-align: left;
    overflow: hidden;
}

.gd_dd {
    width: 460px;
    min-width: 110px;
    float: left;
    overflow: hidden;
    position: relative;
}

.dd_item {
    float: left;
    margin: 0 13px 13px 0;
    position: relative;
    min-width: 32px;
    border: 1px solid #c9c9c9;
}

.color_size_cur a {
    padding: 1px;
    border: none;
    /*border: 1px solid #d00000;*/
}

.dd_item a {
    display: block;
    /*border: 1px solid #ccc;*/
    padding: 3px 4px;
    background-color: #fff;
    text-align: center;
    min-width: 22px;
}

.color_size_cur b {
    display: block;
    width: 21px;
    height: 19px;
    position: absolute;
    right: 0px;
    bottom: 0px;
    /*background: url(http://www.5lux.com/vendor/images/5lux/new_5luxbg.png) no-repeat;*/
    background-position: -249px -51px;
}

.gd_dd ._ed {
    border: 1px solid #dc0000;
}

#addCar_con {
    width: 427px;
}

#addCar_main {
    border: 1px solid #898989;
}

#addCar_main .addCar_top {
    width: 425px;
    height: 30px;
    background-color: #898989;
    overflow: hidden;
    line-height: 30px;
    vertical-align: middle;
}

.addCar_top_l {
    width: 50%;
    float: left;
}

#addCar_main .addCar_top span {
    font-size: 12px;
    color: #fff;
}

.addCar_top_r {
    width: 50px;
    float: right;
    text-align: right;
    position: relative;
    background: url(http://www.5lux.com/vendor/images/car_close.png) 5px 3px no-repeat;
    right: 5px;
    top: 2px;
    cursor: pointer;
}

.addCar_top_r span {
    position: relative;
    top: -2px;
    left: 0px;
}

.addCar_content {
    text-align: center;
}

.addCar_content_top {
    width: 387px;
    border-bottom: 1px solid #eee;
    height: 75px;
    overflow: hidden;
    margin: 0 auto;
}

.addCar_content_l {
    text-align: left;
}

.addCar_fl {
    float: left;
}

.addCar_content_l p {
    padding: 0px;
    margin: 0px;
    margin-top: 16px;
    overflow: hidden;
}

.addCar_content_l p {
    padding: 0px;
    margin: 0px;
    font-size: 12px;
}

.addCar_content_r {
    width: 60%;
}

.addCar_fr {
    float: right;
}

.addCar_content_r p {
    padding: 0px;
    margin: 0px;
    margin-left: 15px;
    margin-top: 15px;
}

.addCar_center {
    width: 417px;
    overflow: hidden;
    margin: 0 auto;
}

.addCar_center_text {
    width: 387px;
    text-align: left;
    height: 40px;
    line-height: 40px;
    vertical-align: middle;
    margin: 0 auto;
}

.addCar_good {
    width: 100%;
}

.addCar_good ul {
    width: 100%;
    overflow: hidden;
    zoom: 1;
}

.addCar_good ul li {
    float: left;
    width: 92px;
    margin-left: 10px;
}

.addCar_good ul li a {
    display: block;
    width: 92px;
}

.buy_num {
    width: 100%;
    position: relative;
    float: left;
}

.buy_num a {
    display: block;
    width: 22px;
    height: 22px;
    position: absolute;
    background-color: #c8a985;
}

.buy_ntext {
    display: block;
    width: 42px;
    height: 19px;
    line-height: 19px;
    vertical-align: middle;
    font-weight: bold;
    margin-left: 24px;
    text-align: center;
}

.btn_reduce {
    left: 0px;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -311px -292px;
}











/*æ–°v30*/

.bo_xuxian dl dd {
    line-height: 30px;
}

#gd30_pricebox dl {
    padding: 5px 13px;
}

.gd30_pb {
    position: relative;
    padding-top: 10px;
}

.gd30_pb ._s {
    color: #c8a985;
    /*    font-family: sans-serif;*/
    font-size: 14px;
    /*position: absolute;*/
    /*top: 2px;*/
    /*left: 0;*/
    vertical-align: baseline;
}

.gd30_pb ._big {
    color: #c8a985;
    font-size: 28px;
    padding-left: 5px;
    padding-right: 23px;
}

.gd30_pb ._foke {
    color: #999;
    font-size: 18px;
    /*font-family: Tohama;*/
}

#hy_price {
    color: #bfa69a;
    font-size: 13px;
    line-height: 25px;
    padding-right: 30px;
    float: right;
}

#hy_price b {
    width: 18px;
    height: 16px;
    display: inline-block;
    vertical-align: middle;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -350px -294px;
}

#gd30_promotebox {
    padding-left: 13px;
    /*height: 35px;*/
    overflow: hidden;
}

#gd30_promotebox table {
    /*position: relative;*/
}











/*#gd30_promotebox table tbody{
    position: absolute;
    top: 2px;
    left: 0;
    z-index: 1;
}*/

#gd30_promotebox thead span {
    line-height: 35px;
}

#gd30_promotebox table tr {
    vertical-align: top;
}

#gd30_promotebox table tr td {
    line-height: 35px;
}

#gd30_promotebox b {

    width: 50px;
    height: 35px;
    display: inline-block;
    float: right;
    cursor: pointer;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -369px -283px
}

.gd30pitems dl dd {
    line-height: 28px;
    color: #c8a985;
}

#gd30_promotebox tbody tr td dl {
    margin-top: -31px;
}

.btn_add {
    left: 72px;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -268px -292px;
}

#gd30_nums {
    padding-bottom: 20px;
}

.v30_storehint {
    float: left;
    margin-left: 15px;
    font-size: 13px;
}

.v30_storechose {
    float: left;
    margin-left: 20px;
    background: #c8a985;
    color: #fff;
    padding: 0px 8px;
    border-radius: 3px;
}

#gd30_hintbox dl {
    width: 100%;
    display: inline-block;
    color: #999;
}

#gd30_hintbox dl dt {
    display: block;
    padding-left: 13px;
    width: 80px;
    float: left;
}

#gd30_hintbox dl dd {
    float: left;
    display: block;
    width: 422px;
}

.add_car_btn {
    margin-left: 10px;
    position: relative;
}

.buy_btn,
.add_car_btn {
    height: 35px;
    float: left;
    _display: inline;
}

.add_car_btn .goods_add_fav span {
    display: inline-block;
    padding: 0 28px 0px 52px;
    height: 35px;
    line-height: 35px;
    vertical-align: middle;
    color: #fff;
    background: #c8a985;
    font-family: "å¾®è½¯é›…é»‘";
    font-size: 14px;
    border: 0px;
    cursor: pointer;
}

.add_car_btn b {
    width: 25px;
    height: 35px;
    left: 24px;
    top: 0;
    display: inline-block;
    position: absolute;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -270px -335px;
}

#gd30_honor {
    display: block;
    padding-top: 12px;
    padding-bottom: 12px;
    height: 35px;
    clear: both;
}

#gd30_honor dl {
    display: inline-block;
    float: left;
    overflow: hidden;
}

.gd30_favor dt {
    width: 25px;
    height: 35px;
    display: inline-block;
    float: left;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -25px -334px;
}

.gd30_share dt {
    width: 25px;
    height: 35px;
    display: inline-block;
    float: left;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -68px -334px;
}

.gd30_right dt {
    width: 25px;
    height: 35px;
    display: inline-block;
    float: left;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -228px -334px;
}

.gd30_quick dt {
    width: 28px;
    height: 35px;
    display: inline-block;
    float: left;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -105px -334px;
}

.gd30_integrity dt {
    width: 28px;
    height: 35px;
    display: inline-block;
    float: left;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -147px -334px;
}

#gd30_honor dl dd {
    float: left;
    line-height: 35px;
    padding-left: 7px;
    color: #666;
    padding-right: 22px;
}

.gd30tb_main {
    width: 1100px;
    height: 35px;
    margin: 0 auto;
}

.gd30tbm_b {
    width: 198px;
    border: 1px solid #c9c9c9;
    float: left;
}

.gd30tmb_head {
    height: 33px;
    line-height: 33px;
    text-align: center;
    color: #666;
    cursor: pointer;
    position: relative;
    /*border-bottom: 1px solid #c9c9c9;*/
}

.gd30tmb_head b {
    display: block;
    width: 20px;
    height: 33px;
    position: absolute;
    top: 0;
    right: 0;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -236px -288px;
}

.gd30tbm_i {
    width: 868px;
    float: left;
    /*overflow: hidden;*/
    margin-left: 30px;
    border: 1px solid #c9c9c9;
}

.gd30tbm_i ul li {
    display: inline-block;
    width: 198px;
    line-height: 33px;
    text-align: center;
    color: #666;
    float: left;
    cursor: pointer;
    position: relative;
}

.gd30tbm_i ul li b {
    width: 1px;
    display: block;
    height: 15px;
    top: 8px;
    right: 0;
    position: absolute;
    background: #c9c9c9;
}

.gd30tbmi_qrcode {
    width: 110px;
    line-height: 33px;
    color: #666;
    position: relative;
    float: right;
}

.gd30tbmi_qrcode i {
    display: inline-block;
    width: 25px;
    height: 33px;
    position: absolute;
    left: 61px;
    top: 0;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -190px -337px;
}

.gd30tbmi_qrcode b {
    display: inline-block;
    width: 25px;
    height: 33px;
    position: absolute;
    left: 86px;
    top: 0;
    cursor: pointer;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -229px -288px;
}

.gd30tbmi_qrcode .gd30tbmiq {
    width: 128px;
    /*height: 148px;*/
    position: absolute;
    text-align: center;
    right: -1px;
    top: 33px;
    z-index: 1;
    background: white;
    border: 1px solid #c9c9c9;
}

.gd30tbmiq span {
    color: #949494;
    padding: 2px 2px;
}

.gd30tmb_show {
    width: 198px;
    height: 122px;
    padding-top: 5px;
    text-align: center;
    border: 1px solid #c9c9c9;
    border-top: none;
    background: #fff;
}

.gd30tmb_show span {
    line-height: 25px;
    color: #666;
}

.gd30tmb_show ul {
    padding-top: 2px;
}

.gd30tmb_show ul li {
    display: inline-block;
    float: left;
    width: 50%;
}

.gd30tmb_show ul li a {
    width: 76px;
    height: 24px;
    line-height: 24px;
    color: #c8a985;
    text-align: center;
    display: block;
    border: 1px solid #c8a985;
}

.gd30tmb_show ul li a:hover {
    color: #fff;
    background: #c8a985;
    cursor: pointer;
}

.gd30_addcart a {
    float: right;
    margin-right: 8px;
}

.gd30_booking a {
    float: left;
    margin-left: 8px;
}

#gd30_main {
    width: 1100px;
    margin: 0 auto;
}

.goodsContent_left {
    width: 200px;
    float: left;
}

.goodsContent_right {
    width: 870px;
    float: left;
    padding-left: 30px;
    overflow: hidden;
}

.gd30tbm_i ._ed {
    color: #c8a985;
}

.gd30hstore {
    color: #c8a985;
    text-decoration: underline;
}

#gd30_taball {
    width: 100%;
}

.gd_tabfixed {
    border-top: 1px solid #c9c9c9;
    border-bottom: 1px solid #c9c9c9;
    -webkit-box-shadow: 0, 0, 0, 0 10px 10px green;
    /*åº•è¾¹é˜´å½±*/
    -moz-box-shadow: 0, 0, 0, 0 10px 10px green;
    /*åº•è¾¹é˜´å½±*/
    box-shadow: 0, 0, 0, 0 10px 10px green;
    /*åº•è¾¹é˜´å½±*/
    background: #fff;
}

.gd30tbm_ifixed {
    border: none;
}











/*ç¼ºè´§ç™»è®°å¼¹æ¡†start*/

.check_in_box {
    position: absolute;
    z-index: 99999;
    left: -7px;
    bottom: 30px;
    width: 530px;
    overflow: hidden;
    zoom: 1;
    background-color: #fff;
    border: 1px solid #acacac;
    -webkit-box-shadow: #a7a7a7 1px 3px 3px;
    -moz-box-shadow: #a7a7a7 1px 3px 3px;
    box-shadow: #a7a7a7 1px 3px 3px;
}

.check_info_container {
    position: relative;
    width: 530px;
    overflow: hidden;
    zoom: 1;
}

.check_info_container b {
    position: absolute;
    z-index: 9999;
    right: 0;
    top: 0;
    width: 30px;
    height: 30px;
    display: block;
    background: url(http://www.5lux.com/vendor/images/5lux/quehuo_close_bg.png) 5px 4px no-repeat;
    cursor: pointer;
}

.check_goods_info {
    padding: 30px 10px 20px 10px;
    overflow: hidden;
    zoom: 1;
    text-align: left; //font-family: "é»‘ä½“";
    font-size: 14px;
}

.check_goods_info .product_name {
    width: 100%;
    height: 20px;
    line-height: 20px;
    margin-bottom: 15px;
}

.check_goods_info .product_name span {
    float: left;
    width: 70px;
}

.check_goods_info .product_name span.goodl_info {
    float: left;
    width: 430px;
    white-space: nowrap;
    overflow: hidden;
}

.check_goods_info .product_num {
    width: 100%;
    height: 25px;
    margin-bottom: 15px;
}

.check_goods_info .product_num span {
    float: left;
    width: 70px;
    height: 25px;
    display: block;
    line-height: 25px;
}

.check_goods_info .product_num input {
    float: left;
    text-align: center;
    width: 36px;
    height: 23px;
    line-height: 23px;
    border: 1px solid #dadada;
    vertical-align: middle;
    font-family: "ä»¿å®‹";
    font-size: 14px;
    color: #000;
}

.check_goods_info .product_detail_info {
    width: 100%;
    height: 20px;
    line-height: 20px;
    margin-top: 15px;
    margin-bottom: 15px;
}

.check_goods_info .product_detail_info span {
    float: left;
}

.check_goods_info .product_detail_info span.titl {
    width: 70px;
    letter-spacing: 10px;
}

.check_goods_info .product_beizhu_info {
    width: 100%;
    height: 66px;
    margin-bottom: 15px;
}

.check_goods_info .product_beizhu_info span.text_info {
    float: left;
    line-height: 66px;
    width: 70px;
}

.check_goods_info .product_beizhu_info textarea {
    float: left;
    width: 250px;
    padding: 17px 10px;
}

.check_goods_info .product_tel_person {
    width: 100%;
    height: 30px;
    margin-bottom: 15px;
}

.check_goods_info .product_tel_person span.text_info {
    float: left;
    line-height: 30px;
    width: 70px;
}

.check_goods_info .product_tel_person input {
    float: left;
    width: 165px;
    height: 28px;
    line-height: 28px;
    vertical-align: middle;
    border: 1px solid #dadada;
}

.check_goods_info .product_tel {
    width: 100%;
    height: 30px;
    margin-bottom: 15px;
}

.check_goods_info .product_tel span.text_info {
    float: left;
    line-height: 30px;
    width: 70px;
}

.check_goods_info .product_tel input {
    float: left;
    width: 165px;
    height: 28px;
    line-height: 28px;
    vertical-align: middle;
    border: 1px solid #dadada;
}

.product_btn_box {
    margin-top: 15px;
    margin-bottom: 15px;
    width: 100%;
    height: 35px;
    text-align: center;
}

.product_btn_box a {
    margin: 0 auto;
    width: 98px;
    height: 33px;
    display: block;
    line-height: 33px;
    font-size: 16px;
    background-color: #ff4546;
    color: #fff;
    text-decoration: none;
}

.product_btn_box a:link {
    color: #fff;
}

.product_btn_box a:visited {
    color: #fff;
}

.check_info_container .successful_box {
    width: 100%;
    overflow: hidden;
    zoom: 1;
}

.successful_box p.success_tip {
    width: 100%;
    margin-top: 35px;
}

.successful_box p.success_tip strong {
    font-size: 22px;
    color: #d2191f;
}

.successful_box p {
    width: 100%;
    text-align: center;
    font-family: "é»‘ä½“";
    font-size: 15px;
    line-height: 25px;
    font-weight: bold;
}











/*ç¼ºè´§ç™»è®°å¼¹æ¡†end*/

.goods_add_popup {
    position: absolute;
    z-index: 1;
}











/*æ”¶è—æ°”æ³¡*/

#gd30_honor .gd30_favor {
    overflow: visible;
}

.gd30_favor {
    position: relative;
}











/*
#gd30_honor .gd30_favor .collect_success,#gd30_honor .gd30_favor .already_collect{
    background: #d65c1e;
    border-radius: 8px;
    text-align: center;
    height: 25px;
    line-height: 25px;
    padding-left: 15px;
    padding-right: 15px;
    color: #fff;
}
*/


/*å•†å“ä»·æ ¼*/

.fsk_goods_li table {
    border: none;
    width: 100%;
    margin: 15px auto;
}

.fsk_goods_price_td div {
    float: left;
    padding-left: 12px;
}

.fsk_goods_li .fsk_goods_price_div {}

.fsk_goods_li .fsk_goods_price {
    color: #c8a985;
    font-size: 28px;
    line-height: 34px;
}

.fsk_goods_li .fsk_goods_special_price {
    color: #999;
    font-size: 16px;
    text-decoration: line-through;
    line-height: 30px;
}

.fsk_goods_mobile_price {
    color: #333;
    font-size: 16px;
    line-height: 32px;
    position: relative;
}

.fsk_goods_mobile_price i {
    display: inline-block;
    width: 25px;
    height: 33px;
    position: absolute;
    right: -35px;
    top: 0;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -190px -337px;
}

.fsk_goods_mobile_price span {
    display: inline-block;
    margin-left: 62px;
}

.fsk_goods_mobile_price b {
    display: inline-block;
    width: 25px;
    height: 33px;
    position: absolute;
    right: -55px;
    top: 0;
    cursor: pointer;
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -229px -288px;
}











/*.fsk_goods_li .fsk_goods_price_type_td {*/


/*vertical-align: top;*/


/*}*/

.fsk_goods_li .fsk_goods_price_type {
    width: 80px;
    padding: 0px;
    text-align: center;
    height: 20px;
    line-height: 20px;
    font-size: 12px;
    color: #fff;
    background: #c8a985;
    border-radius: 10px;
    margin-top: 8px;
    position: absolute;
    left: 200px;
}

.fsk_goods_li .fsk_goods_show_price_td {
    width: 160px;
    position: relative;
    vertical-align: top;
    text-align: right;
}

.fsk_goods_li .fsk_goods_show_price {
    width: 100px;
    /*padding: 0 30px;*/
    height: 30px;
    line-height: 30px;
    text-align: center;
    color: #c8a985;
    font-size: 14px;
    display: block;
    /*margin-right: 20px;*/
    /*float: right;*/
    border-radius: 2px;
    position: absolute;
    top: 10px;
    right: 20px;
    z-index: 2;
}

.fsk_goods_add_border {
    border: 1px solid #ccc;
    border-bottom: 1px solid #fff;
}

.fsk_goods_del_border {
    border: 1px solid #fff;
}

.fsk_goods_li .fsk_goods_show_price b {
    background: url(http://www.5lux.com/vendor/images/v30/brandstore_share.png) no-repeat -350px -287px;
    width: 20px;
    height: 30px;
    display: block;
    float: left;
    margin-left: 15px;
    margin-right: 8px;
}

.fsk_goods_li .fsk_goods_show_price span {
    display: block;
    float: left;
}

.fsk_goods_li .fsk_goods_hide_price {
    width: 200px;
    background: #fff;
    position: absolute;
    top: 41px;
    right: 20px;
    padding: 10px 0;
    border: 1px solid #ccc;
    z-index: 1;
    border-radius: 2px;
}

.fsk_goods_hide_price p {
    /*width: 100%;*/
    height: 26px;
    line-height: 26px;
    font-size: 14px;
    text-align: center;
    color: #333;
}

.fsk_goods_hide_price a {

    /*padding: 0 10px;*/
    width: 110px;
    height: 24px;
    line-height: 24px;
    text-align: center;
    border: none;
    background: #c8a985;
    border-radius: 3px;
    color: #fff;
    font-size: 12px;
    display: block;
    margin: 0 auto;
    margin-top: 5px;
}

.goods_popularize {
    width: 870px;
    margin: 15px 0 12px 0;
    cursor: pointer;
}

.goods_popularize_top img {
    width: 865px;
    height: 312px;
    box-shadow: 5px 5px 10px #ccc;
}

.goods_popularize_bottom {
    padding-top: 13px;
}

.goods_popularize_bottom img {
    width: 431px;
    height: 254px;
}

.popularize_bottom_l {
    float: left;
    width: 431px;
    height: 254px;
}

.popularize_bottom_r {
    float: right;
    width: 431px;
    height: 254px;
}

.popularize_t_hide,
.popularize_b_hide {
    position: absolute;
    bottom: 0;
    left: 0;
    display: none;
}

.goods_popularize_top,
.popularize_bottom_l,
.popularize_bottom_r {
    position: relative;
}

.goods_popularize_txt {
    height: 70px;
    padding-top: 20px;
    width: 431px;
    background: url(http://www.5lux.com/vendor/images/good/txt_bg.png) repeat-x;
    color: #fff;
    text-align: center;
    position: absolute;
    left: 0;
    bottom: 0;
}

.txt_top {
    font-size: 20px;
    line-height: 30px;
}

.txt_bottom {
    font-size: 16px;
}

<!--çŒœä½ å–œæ¬¢-->.scroll {
    width: 870px;
    height: 390px;
    margin: 30px auto 0 auto;
    overflow: hidden;
}

.v_out {
    width: 870px;
    margin: 0px auto;
    overflow: hidden;
}

.v_show {
    width: 885px;
    overflow: hidden;
    position: relative;
    height: 325px;
    float: left
}

.u_lanren {
    width: 6650px;
    position: absolute;
    left: 0px;
    top: 0px;
}

.u_lanren ul {
    float: left;
    text-align: center;
    line-height: 50px;
}

.u_lanren ul li {
    width: 885px;
    float: left;
    overflow: hidden;
}

.u_lanren ul li dd img {
    width: 198px;
    height: 198px;
}

.y_love {
    width: 870px;
    margin: 0px auto;
    overflow: hidden;
}

.love_main {
    width: 870px;
    overflow: hidden;
    position: relative;
    height: 315px;
    float: left
}

.love_list {
    width: 100%;
    position: absolute;
    left: 0px;
    top: 0px;
}

.list {
    list-style: none;
    text-align: center;
    float: left;
    font-size: 12px;
    margin: 0 10px 5px;
    width: 198px;
    border: #cccccc solid 1px;
}

.love_list .list p {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    line-height: 20px;
    color: #000;
    font-size: 14px;
}

.tuijian p,
.tuijian span {
    display: inline-block;
}

.next,
.prev {
    display: inline-block;
    font-family: 'é»‘ä½“';
    font-weight: 700;
}

.new-right-content {
    padding-top: 30px;
    height: 48px;
    font-size: 0;
}

.clearfix {
    display: inline-block;
    overflow: hidden;
    zoom: 1;
}

.new-right-content .new-right-content-list {
    float: left;
    height: 48px;
    margin-right: 40px;
    cursor: pointer;
}

.new-right-content .new-right-content-list i {
    display: inline-block;
    width: 48px;
    height: 48px;
    background-repeat: no-repeat;
    background-size: 48px 48px;
    margin-right: 16px;
}

.zhp {
    background-image: url(http://www.5lux.com/vendor/images/good/detail_desc/guaranteed_warranty.png);
}

.new-right-content .new-right-content-list .new-right-content-text {
    font-size: 14px;
    color: #999;
    margin: 0;
    height: 48px;
    line-height: 48px;
}

.bs {
    background-image: url(http://www.5lux.com/vendor/images/good/detail_desc/faith_enterprise.png);
}

.wyshb {
    background-image: url(http://www.5lux.com/vendor/images/good/detail_desc/guarantee.png);
}

.new-right-content .new-right-content-list i,
.new-right-content .new-right-content-list p {
    float: left;
}

.new-left-content {
    padding: 20px;
    height: 20px;
    font-size: 0;
}

.new-left-content .new-left-content-list {
    float: left;
    height: 20px;
    margin-right: 20px;
    cursor: pointer;
}

.collect {
    background-image: url(http://www.5lux.com/vendor/images/good/detail_desc/collect.png);
}

.new-left-content .new-left-content-list .new-left-content-text {
    font-size: 12px;
    color: #999;
    margin: 0;
    height: 20px;
    line-height: 20px;
}

.new-left-content .new-left-content-list i {
    display: inline-block;
    width: 20px;
    height: 20px;
    background-repeat: no-repeat;
    background-size: 20px 20px;
    margin-right: 10px;
}

.new-left-content .new-left-content-list i,
.new-left-content .new-left-content-list p {
    float: left;
}

.share {
    background-image: url(http://www.5lux.com/vendor/images/good/detail_desc/share.png);
}

#gdetail_con {
    width: 1100px;
    margin: 0 auto;
    overflow: hidden;
    zoom: 1;
    margin-top: 15px;
}
</style>
