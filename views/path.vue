<template>
    <div>
        <mt-header title="地址管理" fixed>
            <div slot="left">
                <router-link to="/" class="header">
                    <img src="../assets/images/back.png" id="back">
                </router-link></div>
            <mt-button slot="right" icon="more"><router-link to="" class="header">添加新地址</router-link></mt-button>
        </mt-header>
        <mt-tab-container>
            <mt-cell isLink to="/" class="cell">
                <div>
                    <b>yiyi</b>
                    <span>12345667</span><br>
                    <p>重庆市渝北区，重庆互联网学院</p>
                </div>
            </mt-cell>
        </mt-tab-container>
    </div>
</template>
<style  scoped>
/* 顶部导航栏样式 */
    .header{
        color: #ffffff;
        text-decoration: none;
    }
    /* 面板区域样式 */
    .mint-tab-container{
        top: 47px;
    }
    .cell{
        width: 100%;
        height: 60px;
    }

    .cell b,span{
        font-size: 14px;
        margin-left: 5px;
        position: relative;
        top: 5px;
        left: -84px;
    }
    .cell p{
        position: relative;
        font-size: 15px;
        margin: 12px 0;
        left: -80px;
    }
</style>>