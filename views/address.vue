<template>
    <div class="container">
        <mt-header title="新增地址" fixed id="header">
            <div slot="left">
                <router-link to="/" class="header">
                    <img src="../assets/images/back(b).png" id="back">
                </router-link>
            </div>
        </mt-header>
        <div id="tab">
            <mt-field type="text" label="收货人" placeholder="请输入有效姓名"><img src="../assets/images/right.png" alt=""></mt-field>
            <mt-field type="`number`" label="联系电话" placeholder="请输入有效联系电话"><img src="../assets/images/right.png" alt=""></mt-field>
            <mt-field type="text" label="所在地区" placeholder=""><img src="../assets/images/right.png" alt=""></mt-field>
            <mt-field type="text" label="详细地址" placeholder="请详细填写收货地址"><img src="../assets/images/right.png" alt=""></mt-field>
            <mt-button size="normal" plain class="btn">设为默认</mt-button>
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
     /* 内容区域样式 */
    .container{
        width: 100%;
        height: 400px;
        background-color: #f3f3f3;
        border: 0;
    }
    #tab{
        width: 100%;
        height: 90px;
        background-color: white;
        position: relative;
        top: 55px; 
        left: -1px;
        border: 0;   
       }
       #tab mt-field{
           padding-left:5px ;
       }
       .btn{
           width: 100%;
           margin-top: 20px;
       }
       .mint-button--default.is-plain{
            border: 0;
            background-color: #ffffff;
       }
</style>
