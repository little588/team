<template>
    <div id="tab">
        <mt-header title="邀请好友" fixed id="header">
            <div slot="left">
                <router-link to="/" class="header">
                    <img src="../assets/images/back(b).png" id="back">
                </router-link>
            </div>
        </mt-header>
        <div id="tab-item">
            <img src="../assets/images/invitation.jpg" class="image">
            <span id="divider"></span>
            <mt-button size="normal" class="btn">去邀请好友</mt-button>
        </div>
            <span class="wen">邀请奖励</span>
        <p class="introduce">好友在兼职栏目做任务时，你可获得赏金的<span>13.3%</span>奖励</p>
        <div id="end">
           <p><b>我的好友</b></p>
           <span>0</span><span>0</span><br>
           <span>所有会员</span><span>正式会员</span>
           <mt-button class="btn1">查看记录</mt-button>
        </div>
    </div>
</template>
<style scoped>
 /* 头部样式 */
    #header{
        background-color: white;
        color: black;
        font-size:16px;
    }
    /* 背景色 */
    #tab{
        width: 100%;
        height: 600px;
        background-color: #fffd7d;
    }
    /* 活动图片 */
    #tab-item{
        width: 300px;
        height: 320px;
        background-color: #ffffff;
        margin: 38px auto;
        position: relative;
        top: 10px;
    }
    .image{
        width:270px;
        height: 220px;
        display: block;
        position: relative;
        top: 20px;
        left: 15px;
    }
    #divider{
        display: block;
        border-top: 1px solid #c9c9c9;
        width: 75%;
        position: relative; 
        top: 40px;
        margin: 0 auto;
    }
    /* 活动按钮 */
    .btn{
        width: 80%;
        height: 40px;
        margin: 50px 0 0 30px;
        color: #ffffff;
        border-radius: 5px;
        background-image: linear-gradient(top,rgb(255, 118, 118),rgb(255, 80, 80));
    }
    /* 邀请奖励 */
    .wen{
        display: inline-block;
        margin-left:40%;
    }
    .introduce{
        margin: 10px auto;
        width: 90%;
        height: 70px;
        padding: 15px 0 0 10px;
        font-size: 16px;
        background-color: #ffffff;
    }
    .introduce span{
        color: red;
        font-weight: bold;
    }
    /* 尾部 */
    #end{
        width: 100%;
        height:250px;
        background-color: #ffffff;
    }
    #end p b{
        display: inline-block;
        margin: 10px 0 0 40%;
    }
    #end span{
        display: inline-block;
        width: 70px;
        height: 10px;
        text-align: center;
        margin-left: 72px;
        color: #797979;
    }
    .btn1{
        width: 60%;
        height: 35px;
        margin: 10px 0 0 17%;
        color: #ffffff;
        background-image: linear-gradient(top,rgb(248, 63, 63),rgb(255, 4, 4))
    }
</style>