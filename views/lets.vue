<template>
    <div>
         <!-- 顶部返回开始-->
        <mt-header fixed title="我的钱包">
            <router-link to="/Me" slot="left" style="color:black">
            <mt-button icon="back"></mt-button>
            </router-link>
        </mt-header>
        <!-- 顶部返回结束-->
        <!-- 内容开始 -->
        <div class="bseds">
            <div class="bsedsw">
                <div>
                      <img src="" alt="">
                </div>
                <div>
                    <span>￥0.05</span>
                    <div>
                         <span>当前余额</span>
                    </div>
                </div>
            </div>
            <div class="bsedser">
                <div>
                      <img src="" alt="">
                </div>
                <div>
                    <span>￥0.05</span>
                   <div>
                         <span>当前余额</span>
                    </div>
                </div>
            </div>
        </div>
        <!-- 内容结束 -->
        <!-- 选项卡开始 -->
        <div>
            <img src="" alt="">
        </div>
        <div>
            <mt-cell title="充值" is-link></mt-cell>
            <mt-cell title="提现" is-link></mt-cell>
            <mt-cell title="资金明细" is-link></mt-cell>
        </div>
        
        <!-- 选项卡结束-->


    </div>
</template>
<style  scoped>
    .mint-header {
        background-color:#fff;
        color: black;
    }
    .bseds{
        display: flex;
        height: 200px;
        background: -moz-linear-gradient(top, #dfaa78 0%,#f78d03 100%);
        background: -webkit-gradient(linear, left top, left bottom, color-stop(0%, #dfaa78), color-stop(100%,#f78d03));
        background: -webkit-linear-gradient(top,  #dfaa78 0%,#f78d03 100%);
        background: -o-linear-gradient(top,  #dfaa78 0%,#f78d03 100%);
        background: -ms-linear-gradient(top,  #dfaa78 0%#f78d03 100%);
        background: linear-gradient(to bottom,  #dfaa78 0%,#f78d03 100%);
    }
    .bsedsw{
        padding: 10px;
        margin-top: 80px;
        margin-left: 50px;
    }
    .bsedser{
        padding: 10px;
        margin-top: 80px;
         margin-left: 50px;
    }
</style>