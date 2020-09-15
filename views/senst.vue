<template>
    <div>
        <!-- 顶部返回开始-->
        <mt-header fixed title="优惠红包">
            <router-link to="/me" slot="left">
            <mt-button icon="back"></mt-button>
            </router-link>
        </mt-header>
        <!-- 顶部返回结束-->
        <!--  第1个内容区域开始-->
        <div class="lets">
            <div >
                <span class="letse">超市消费券
                    <div class="letsea">
                        <span>有效日期至2020.09.22</span>
                    </div>
                </span>
                <i class="coupon_icon"></i>
                <span class="letsed">￥9
                     <div class="letsea">
                        <span>满15可用</span>
                    </div>
                </span>
            </div>
            <div class="letsdes">
                <span class="letsdf">限商品现价+包装费满15元使用，限非到店自取订单，本账户商家首单，超市便利，医药健康，商品专售，水果商家使用，限本账户使用，不可转让使用</span>
            </div>
        </div>
        <!--第1个内容区域结束-->
        <!--第2个内容区域开始-->
        <div class="lets">
            <div >
                <span class="letse">烧烤烤鱼消费券
                    <div class="letsea">
                        <span>有效日期至2020.09.25</span>
                    </div>
                </span>
                <i class="coupon_icon"></i>
                <span class="letsed">￥16
                     <div class="letsea">
                        <span>满100可用</span>
                    </div>
                </span>
            </div>
            <div class="letsdes">
                <span class="letsdf">限商品现价+包装费满100元使用，限烧烤烤鱼商家使用，限本账户使用，不可转让使用</span>
            </div>
        </div>
        <!--第2个内容区域结束-->
         <!--第3个内容区域开始-->
        <div class="lets">
            <div >
                <span class="letse">夜宵红包
                    <div class="letsea">
                        <span>有效日期至2020.09.19</span>
                    </div>
                </span>
                <i class="coupon_icon"></i>
                <span class="letsed">￥6
                     <div class="letsea">
                        <span>满30可用</span>
                    </div>
                </span>
            </div>
            <div class="letsdes">
                <span class="letsdf">限商品现价+包装费满30元使用，限非到店自取订单，21.00——00.30可以使用，限本账户使用，不可转让使用</span>
            </div>
        </div>
        <!--第3个内容区域结束-->
        <!--第4个内容区域开始-->
        <div class="lets">
            <div >
                <span class="letse">超值联盟券
                    <div class="letsea">
                        <span>有效日期至2020.09.22</span>
                    </div>
                </span>
                <i class="coupon_icon"></i>
                <span class="letsed">￥12
                     <div class="letsea">
                        <span>满50可用</span>
                    </div>
                </span>
            </div>
            <div class="letsdes">
                <span class="letsdf">限商品现价+包装费满50元使用，限超值联盟券可以使用，限本账户使用，不可转让使用</span>
            </div>
        </div>
        <!--第4个内容区域结束-->
        <!--第5个内容区域开始-->
        <div class="lets">
            <div >
                <span class="letse">辉尚餐厅券
                    <div class="letsea">
                        <span>有效日期至2020.09.27</span>
                    </div>
                </span>
                <i class="coupon_icon"></i>
                <span class="letsed">￥15
                     <div class="letsea">
                        <span>满80可用</span>
                    </div>
                </span>
            </div>
            <div class="letsdes">
                <span class="letsdf">限商品现价+包装费满80元使用，限辉尚餐厅可以使用，优惠活动请到店查看，限本账户使用，不可转让使用</span>
            </div>
        </div>
        <!--第5个内容区域结束-->

        <!--第6个内容区域开始-->
        <div class="lets">
            <div >
                <span class="letse">自助火锅券
                    <div class="letsea">
                        <span>有效日期至2020.09.29</span>
                    </div>
                </span>
                <i class="coupon_icon"></i>
                <span class="letsed">￥19
                     <div class="letsea">
                        <span>满100可用</span>
                    </div>
                </span>
            </div>
            <div class="letsdes">
                <span class="letsdf">限商品现价+包装费满100元使用，限自助火锅可以使用，优惠活动请到店查看，限本账户使用，不可转让使用</span>
            </div>
        </div>
        <!--第6个内容区域结束-->
        <div class="newsq">
            <span>没有更多优惠券了</span>
        </div>

    </div>
</template>
<style scoped>


.mint-header {
        background-color:#ef5f58;
}
    .lets{
    margin-top: 50px;
    margin-left: 20px;
    width: 90%;
    height: 150px;
    background-color: rgb(245, 245, 245);

    }
    .letse{
        position: absolute;
        padding: 20px;
        font-size:24px;
        color: red;
    }
    .letsed{
        position: absolute;
        padding: 20px;
        font-size: 24px;
        margin-left: 70%;
        color: red;
    }
    .letsea{
        margin-top: 5px;
        color: black;
        font-size: 10px;
    }
    .letsdes{
        margin-left: 10px;
        width: 80%;
        font-size: 12px;
        color: rgba(124, 118, 118, 0.87);
        /* font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; */
        position: absolute;
        margin-top: 100px;
    }
    .newsq{
    margin-top: 60px;
    height: 100px;
    text-align: center;
    background-color: #ffffff;
}
</style>