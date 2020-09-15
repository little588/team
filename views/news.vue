<template>
    <div>
         <!-- 顶部返回开始-->
        <mt-header fixed title="我的信息">
            <router-link to="/me" slot="left" style="color:black">
            <mt-button icon="back"></mt-button>
            </router-link>
        </mt-header>
        <!-- 顶部返回结束-->
        <!-- 内容区域开始 -->
        <div>
            <div class="newsd">
                <div class="newsde">
                    <img src="../assets/avater/1.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">超市优惠活动小店</span>
                    <div class="newsdws">
                        <span>超市促销活动更多优惠等着你来，快点来抢购吧</span>
                    </div>
                </div>                
            </div>
        <!--第二个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/60.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">德本家韩国年糕火锅</span>
                    <div class="newsdws">
                        <span>本火锅店推出了最新的优惠，满100送价值20元的代金卷，还不心动吗？</span>
                    </div>
                </div>                
            </div>
        <!--第二个结束  -->
        <!--第三个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/75.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">九村烧烤烤鱼</span>
                    <div class="newsdws">
                        <span>九村烧烤烤鱼期待您的再次光临。祝您生活愉快~~~</span>
                    </div>
                </div>                
            </div>
        <!--第三个结束  -->
        <!--第四个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/00183a5ab206aea80120be1472a6f5.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">M·鲜烤大师·鲜货烧烤</span>
                    <div class="newsdws">
                        <span>感谢亲的支持，欢迎亲的再次光临！</span>
                    </div>
                </div>                
            </div>
        <!--第四个结束  -->
        <!--第五个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/0120cd5dc0e038a801209e1fc96ef7.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">花满庭中餐厅</span>
                    <div class="newsdws">
                        <span>感谢亲对我们本店菜品的认可！祝您健康快乐！么么哒！</span>
                    </div>
                </div>                
            </div>
        <!--第五个结束  -->
        <!--第6个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/96.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">韩香阁</span>
                    <div class="newsdws">
                        <span>本店现在推出自助新套餐，希望让亲每一次都有不同的体验哦</span>
                    </div>
                </div>                
            </div>
        <!--第6个结束  -->
        <!--第7个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/106.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">OH BAR（清吧）</span>
                    <div class="newsdws">
                        <span>推出最新价格，节假日优惠活动，期待亲的到来</span>
                    </div>
                </div>                
            </div>
        <!--第7个结束  -->
        <!--第8个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/0172ab5c63a267a801203d22e6502c.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">Botanica重·林餐厅</span>
                    <div class="newsdws">
                        <span美味是我们回馈所有客户的目标，欢迎您再次光临品鉴！</span>
                    </div>
                </div>                
            </div>
        <!--第8个结束  -->
         <!--第9个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/54.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">嘉格精酿啤酒吧</span>
                    <div class="newsdws">
                        <span>对不起亲，下次我们一定会注意这个问题的，真心的表示歉意！</span>
                    </div>
                </div>                
            </div>
        <!--第9个结束  -->
        <!--第9个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/86.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">金可阳澄湖大闸蟹</span>
                    <div class="newsdws">
                        <span>感谢您的支持和认可，我们将不断改价，期待下次更好</span>
                    </div>
                </div>                
            </div>
        <!--第9个结束  -->
        <!--第10个开始  -->
            <div class="newsds">
                <div class="newsde">
                    <img src="../assets/avater/82.jpg" alt="">
                </div>
                <div class="newsdw">
                    <span class="newsdww">渝唯鲜酸汤乌鱼府</span>
                    <div class="newsdws">
                        <span>感谢您的认可，你的满意是我们前进的动力！</span>
                    </div>
                </div>                
            </div>
        <!--第10个结束  -->
        
        </div>
        <div class="newsq">
            <span>没有更多消息了</span>
        </div>
        <!-- 内容区域结束-->

    </div>
</template>
<style scoped>
.mint-header {
        background-color:#ef5f58;
}
.newsd{
    display: flex;
    margin-top: 40px;
}
.newsds{
    display: flex;
    border-top: 1px dashed #7FFFD4;
}

.newsde img{
    padding: 10px;
    height: 50px;
    widows: 50px;
    margin-top: 10px;
    border: 1px solid #ffffff;
    border-radius: 50px;
}
.newsdw{
    padding: 20px;
    height: 55px;
}
.newsdww{
    font-size: 20px;
    margin-top: 20px;
}
.newsdws{
    height: 50px;
    margin-top: 10px;
    font-size: 14px;
}
.newsq{
    margin-top: 20px;
    height: 100px;
    text-align: center;
    background-color: #ffffff;
}
</style>