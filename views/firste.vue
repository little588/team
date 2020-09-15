<template>
    <div>
        <!-- 顶部返回开始-->
        <mt-header fixed title="">
            <router-link to="/min" slot="left" style="color:black">
            <mt-button icon="back"></mt-button>
            </router-link>
        </mt-header>
        <!-- 顶部返回结束-->

        <!-- 美食图片开始 -->
        <div class="fifth">
            <img src="../assets/asset/6.png" alt="" class="swipe">
        </div>
        <!-- 美食图片结束 -->

        <!-- 美食描述开始 -->
        <div class="fiftha">
            <div class="fifthas">
                <h2 class="fifthb">老山城火锅鸡单人套餐+三种配菜+米饭</h2>
                <span class="fif">月售231</span>
                <div class="fifthube">
                    <span class="fifthubes">16.8</span>
                    <s class="fifthubeser">￥36.8</s>
                    <span class="fifthubeser">/约800克</span>
                    <span class="fift">4.57折/限10份</span>
                    <button class="Thesixth">加入购物车</button>
                </div>
            </div>
            
        </div>
        <!-- 美食描述结束 -->

        <!-- 美食详情开始 -->
        <div class="eighth">
            <ul>
                <li>
                    <span>商品详情</span></li>
                <li>
                    <span>主料:新鲜鸡</span></li>
                <li>
                    <span>辅料：土豆,辣椒,鸡麻</span></li>
                <li>
                    <span>菜系：川菜</span></li>
                <li>
                    <span>口味：微辣</span></li>
            </ul>  
        </div>
        <!-- 美食详情结束 -->
        <div class="fifsw">
            <h4 class="spane">没有更多了，快快下单吧</h4>
        </div>
    </div>
</template>
<style scoped>
    /*  顶部返回 */
    .mint-header{
        background-color: rgb(248, 248, 248);
    }
    /*图片样式 */
    .fifth{
        width:90% ;
        height: 240px;
        margin: 15px auto;    
    }
    .swipe{
        width:100%;
        height: 240px;
    }
    /* 美食描述 */
    .fiftha{
        height:220px ;
        background-color: rgb(249, 250, 253);
    }
    .fifthas{
        height: 200px;
        margin-left: 10px;
    }
    .fifthb{
         color: rgb(90, 79, 79);
    }
    .fif{
        color: rgb(148, 149, 151);
    }
    .fifthube{
        height: 50px;
        line-height: 50px;
    }
    .fifthubes{
        font-size: 22px;
        color: red;
    }
    .fifthubeser{
        color: rgb(148, 149, 151);
    }
    .fift{
        color: red;
        margin-left: 15px;
    }
    .Thesixth{
        height: 40px;
        width: 100px;
        border: 1px solid #ffffff;
        border-radius:20px;
        background-color: #ef5f58;
        margin-left: 60%; 
        color: #fff;      
    }
    /* 美食详情开始 */
    .eighth{
        height: 150px;
        background-color: rgb(249, 250, 253);
        margin-top: 10px;
        padding-top:10px;
    }
   .eighth ul li{
        list-style: none ;
        margin-top: 10px;
    }
    ul{
        padding-inline-start: 20px;
    }
    .fifsw{
        margin-top: 5px;
        padding: 20px;
        text-align: center;
        background-color: rgb(249, 250, 253);
        height: 100px;
    }
   
</style>