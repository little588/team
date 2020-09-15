<template>
    <div>
        <!-- 头部标签开始 -->
        <mt-header class="header">
        <div class="peak" slot="left">
            <router-link to="/" >
                <img src="../assets/images/back.png" id="back">
            </router-link>
            
           <span id="dian">恰是那年火锅冒菜</span>
           <router-link to="/" >
                <img src="../assets/images/shop.png" id="shop">
            </router-link>
             <router-link to="/" >
                <img src="../assets/images/more.png" id="more">
            </router-link>
        </div>
        </mt-header>
        <!-- 头部标签结束 -->
        <!-- 遮挡栏 -->
        <div class="y"></div>
        <!-- 面板选项卡 -->
        <mt-navbar v-model="active" fixed id="navbar"> 
            <input type="text" placeholder="请输入商品名" class="search">
            <mt-tab-item id="1">点菜</mt-tab-item>
            <mt-tab-item id="2">评价</mt-tab-item>
            <mt-tab-item id="3">商家</mt-tab-item>
        </mt-navbar>
        <!-- 面板内容区 -->
        <mt-tab-container v-model="active" id="container">
            <mt-tab-container-item v-model="select" id="1">
                <div class="left">
                        <router-link id="0" data-btn="tab" data-divid="content1" to="/">买过</router-link>
                        <router-link id="1" data-btn="tab" data-divid="content2" to="/">折扣</router-link>  
                        <router-link id="2" data-btn="tab" data-divid="content3" to="/">米饭</router-link>
                        <router-link id="3" data-btn="tab" data-divid="content4" to="/">买过</router-link>
                        <router-link id="4" data-btn="tab" data-divid="content5" to="/">折扣</router-link>  
                        <router-link id="5" data-btn="tab" data-divid="content6" to="/">米饭</router-link>
                </div>
                <div>
                    <div class="right" id="content1" v-for="(k,v) of 7" :key='v'>
                        <router-link to="/firste">
                        <div>
                            <img src="../assets/images/ms.png" id="img" alt="">
                            <div class="wen">
                                <b>香酥鸡排+什锦时蔬+黄金蛋饺1只+赠饮</b>
                                <span>门店销售第一</span>
                                <p class="month">月售：17373</p>
                                <p class="price">￥13.88</p>
                                <mt-button size="small" plain class="add">
                                    <img src="../assets/images/add.png" slot="icon">
                                </mt-button>
                            </div>
                        </div>
                        </router-link>
                    </div>   
                </div> 
                <div id="car">
                    <img src="../assets/images/car.png" alt=""><span>￥0     |</span>
                    <div>￥15起送</div>
                </div>
            </mt-tab-container-item>
            <mt-tab-container-item id="2">折扣</mt-tab-container-item>
            <mt-tab-container-item id="3">
                <div class="introduce">
                    <div id="merchants">
                        <router-link to="">
                            <img src="../assets/images/positioning.png">
                            <span>重庆市渝北区金开大道西段296号附近91号</span>
                        </router-link>
                        <mt-button size="small" plain id="phone">
                            <img src="../assets/images/phone.png" slot="icon" class="phone">
                        </mt-button>
                    </div>
                    <div id="imgs">
                        <img src="../assets/images/1.jpg" alt="">
                        <img src="../assets/images/2.jpg" alt="">
                        <img src="../assets/images/3.jpg" alt="">
                        <img src="../assets/images/4.jpg" alt="">
                    </div>
                    <div class="pei">
                        <img src="../assets/images/text.png"><span>配送服务：由美团快送提供配送服务</span><br><hr>
                        <img src="../assets/images/time.png" class="yi"><span>10:00-23:00</span>
                    </div>
                    <div class="pei">
                        <img src="../assets/images/sound.png"><span>辣年售后rexian：183838s73883</span><br><hr>
                        <img src="../assets/images/success.png"><span >商家服务  <img  src="../assets/images/ding.png" alt="">跨天预定</span>
                       
                    </div>
                     <div class="jian">
                        <p>商家公告</p>
                        <p><b>欢迎来到XXX店，在此感谢小主们对本店一直以来的支持和信任，为了回馈小主们，我们坚持追求用心，责任，高品质，高效率，让小主们看到我们的努力，打心底觉得吃的安全，放心！</b></p>
                        <p><b>温馨提醒:</b>高峰期提前下单，保障用餐时间。下雨天稍有延误请谅解。</p>
                        <p>疑问和建议请与本店联系，谢谢</p>
                    </div>
                </div>
            </mt-tab-container-item>
        </mt-tab-container>
     
    </div>
</template>
<style scoped>
.y{
    width: 500px;
    height:58px;
    background-color: rgb(255, 255, 255);
    position: fixed;
    top: 40px;
    left: 0px;
    z-index: 10;
}
.header{
    background-color: #ffffff;
    z-index: 99;
  }
#back{
    position: relative;
    top: 4px;
    left: 9px;
  }
.search{
    width: 260px;
    height: 25px;
    position: relative;
    top: -40px;
    left: 40px;
    background-image: url(../assets/images/search.png);
    background-position-y: 2px;
    background-repeat:no-repeat;
    border: 1px solid #dddddd;
    padding-left: 35px;
    border-radius: 10px;
    outline:none;
 }
.mint-navbar .mint-tab-item{
    position: relative;
    left: -280px;
    margin-left: 20px;
 }
.peak{
    width: 100%;
    height: 40px;
    background-color: #414141;
    position: fixed;
    left: 0px;
    top: 0px;
}
#more{
    position: relative;
    left: 140px;
    top: 5px;
}
#shop{
    position: relative;
    left: 120px;
    top: 1px;
}
#dian{
    color: #ffffff;
    position: relative;
    left: 67px;
    top: -5px;
}
.back{
    color: #ffffff;
    font-size: 14px;
    position: relative;
    top: -6px;
    left: 2px;
}
#navbar{
    position: fixed;
    width: 115%;
    height: -200px;
    top: 96px;
    z-index: 99;
}
#container{
    position: relative;
    top: 96px;
}
/* #navbar a div{
    display: inline-block;
    width: 20px;
    height: 20px;
} */
.left{
    width: 100px;
    height: 150px;
    margin-top: 10px;
    position: fixed;
    top: 140px;
    left: 9px;
}
.left a{
    display:block ;
    width: 60px;
    height: 40px;
    line-height: 40px;
    text-align: center;
    font-size: 14px;
    color: #858080;
    background-color: rgb(235, 235, 235);
    border-bottom: 1px dashed #ddffff;
    text-decoration: none;
}
.left a:first-child{
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
}
.left a:last-child{
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
}
.right{
    float: right;
    position: relative;
    top: 10px;
    width: 290px;
    height: 120px;
}
#img{
    width: 125px;
    height: 97px;
}
.wen{
    float: right;
}
.wen b{
    display: block;
    width: 140px;
    height: 39px;
    line-height: 19px;
    position: relative;
    left: -8px;
    color: black;
    font-size: 14px;
    overflow: hidden;/*超出部分隐藏*/
}
/* .wen b::after{
    content:"...";
    font-weight: bold;
    position: relative;
    bottom: 0;
    right: -10px;
    padding: 0 20px 1px 45px;
} */
.wen span{
    display: inline-block;
    color:#ffe656;
    font-size:12px;
    background-color:#fff9d4 ;
}
.month{
    /* display: inline-block; */
    color: #d1cece;
    font-size: 12px;
    margin: 6px 0 6px 0;
}
.price{
    font-size: 16px;
    color: #ff8282;
    margin-top: 0px;
}
.wen .mint-button--default.is-plain{
    border: 0px;
}
.wen .add{
    position: relative;
    top: -45px;
    left: 70px;
}
#car{
    width:250px; 
    height: 35px;
    background-color: rgba(5, 5, 5, 0.7);
    border-radius:20px ; 
    position: fixed;  
    top: 513px;
    left: 80px;
}
#car img{
    margin: 6px 0 0 16px;
}
#car span{
    color: #ffffff;
    font-size: 16px;
    position: relative;
    top: -4px;
    left: 5px;
}
#car div{
    float: right;
    margin: 6px 12px 0 0;
    color: #ffffff;
}
.introduce{
    width: 100%;
    height: 600px;
    background-color: #f0f0f0;
}
#merchants{
    width: 100%;
    height: 80px;
    position: relative;
    top: 8px;
    background-color: #fffefa;
    border-bottom: 1px solid #eeeeee;
}
#merchants img{
    position: relative;
    top: 23px;
    left: -1px;
}
#merchants a{
    color: #000000;
    text-decoration: none;
    font-size: 12px;
}
#merchants span{
    display: block;
    width: 227px;
    height: 20px;
    margin-left: 25px;
}
#phone{
    border: 0;
    position: relative;
    top: -28px;
    left:  290px;
}
#phone .phone{
    position: relative;
    top:2px;
    left:0px;
}
#imgs{
    width: 100%;
    height: 80px;
    margin-top: 3px;
    padding: 8px 0 5px 0;
    border-bottom: 1px solid #eeeeee;
    background-color: #fffefa;
}
#imgs img{
    width: 22%;
    height: 75px;
    margin-left: 10px;
}
.pei{
    width: 100%;
    height: 80px;
    background-color:#fffefa;
    margin-top: 8px;
    
}
.pei img{
    position: relative;
    top: 5px;
    margin-left:20px;
}
.pei span{
    font-size: 12px;
    margin-left: 5px;
}
.pei .yi{
    position: relative;
    top: -5px;
}
.pei span:last-child{
    position: relative;
    top: -12px;
}
.jian{
    width: 100%;
    height: 600px;
    background-color: #fffefa;
}
.jian p:first-child{
    display: block;
    margin: 12px 125px;
    padding-top:5px ;
    font-size: 22px;
}
.jian p{
    display: block;
    width: 200px;
    font-size: 12px;
    margin: 10px 75px;
}
</style>
<script>
export default{
    data() {
        return{
            loading:false,
            active:"1",
            select:"1" 
        }
    },
}
/* // var tabs=document.querySelectorAll(`[data-btn=tab]`);
// for(var tab of tabs){
//     tab.onclick=function(){
//         var divid=this.getAttribute("data-divid");
//         var div=document.getElementById(divid);
//         div.style.display=none;
//         div.style.backgroundColor=white;
//     }
//  } */
</script>