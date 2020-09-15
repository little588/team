<template>
<div> 
    <!--顶部导航开始-->
    <div>
        <mt-header title="我的订单" fixed>
            <router-link to="" slot="right">
                <mt-button icon="">
                    <img src="../assets/search.png" alt="" icon="slot">
                </mt-button>
            </router-link>
        </mt-header>
    </div>
     <!--顶部导航结束-->
     <!--顶部选项卡开始-->
     <div class="nav_to">
         <mt-navbar  v-model="active" class="active">
             <mt-tab-item id="1">全部</mt-tab-item>
             <mt-tab-item id="2">待付款</mt-tab-item>
             <mt-tab-item id="3">待发货</mt-tab-item>
             <mt-tab-item id="4">待收货</mt-tab-item>
         </mt-navbar>
     </div>
     <div class="TabContainer">
         <mt-tab-container v-model="active">
             <mt-tab-container-item id="1">
                <div class="first" v-for="(k,i) of 20" :key="i">
                    <div class="title">
                        <span class="title_left">重庆麻辣烫</span>
                        <span class="title_right">商家已接单</span>
                    </div>
                    <div class="IMgss">
                        <img src="../assets/asset/1.png" alt="">
                    </div>
                    <div class="price">
                        <p>￥128.00</p>
                        <p class="time">2020-9-15 10：30：00</p>
                    </div>
                    <div class="sum">
                         <p>1份，共128.00元</p>
                         <router-link to="/">
                            <button class="btn1">再来一单</button>   
                         </router-link>
                         <router-link to="/">
                            <button class="btn2">去评价</button>   
                         </router-link>
                        
                    </div>
                </div>
             </mt-tab-container-item>
             <mt-tab-container-item id="2">
                 <div class="first" v-for="(k,i) of 20" :key="i">
                    <div class="title">
                        <span class="title_left">重庆麻辣烫</span>
                        <span class="title_right">未支付</span>
                    </div>
                    <div class="IMgss">
                        <img src="../assets/asset/1.png" alt="">
                    </div>
                    <div class="price">
                        <p>￥128.00</p>
                    </div>
                </div>
             </mt-tab-container-item>
             <mt-tab-container-item id="3">
                 <div class="first" v-for="(k,i) of 20" :key="i">
                    <div class="title">
                        <span class="title_left">重庆麻辣烫</span>
                        <span class="title_right">待商家发货</span>
                    </div>
                    <div class="IMgss">
                        <img src="../assets/asset/1.png" alt="">
                    </div>
                     <div class="price">
                        <p>￥128.00</p>
                    </div>
                </div>
             </mt-tab-container-item>
             <mt-tab-container-item id="4">
                 <div class="first" v-for="(k,i) of 20" :key="i">
                    <div class="title">
                        <span class="title_left">重庆麻辣烫</span>
                        <span class="title_right">待收货</span>
                    </div>
                    <div class="IMgss">
                        <img src="../assets/asset/1.png" alt="">
                    </div>
                    <div class="price">
                        <p>￥128.00</p>
                    </div>
                </div>
             </mt-tab-container-item>
         </mt-tab-container>
     </div>
     <div>
         <tabbar :selected="selected"></tabbar>
     </div>
</div>
</template>
<script>
import Tabbar from '../components/Tabbar.vue'
export default {
  components:{
    Tabbar
  },
    data(){
        return{
            active:'1',
            selected:'OrderForm',
        }
    },
     watch:{
    // 监听底部选项卡的变化
    selected(Value){
      switch(value){
        case 'index':
          this.$router.push('/');
          break;
        case 'OrderForm':
          this.$router.push('/OrderForm');
          break;
        case 'me':
          this.$router.push('/me');
          break;
      }
    }
  }
}
</script>
<style>
    .nav_to{
        border: 1px solid #ececec;
        margin-top:50px;
        border-radius:10px;
    }
    .active{
        border-radius: 50px !important;
    }
    .TabContainer{
        margin-top:10px;
    }
    /**内容 */
    .first{
        position: relative;
        width: 100%;
        height:160px;
        border: 1px solid #ececec;
    }
    /**标题 */
    .title{
        position: relative;
        width: 100%;
        height: 40px;
        line-height: 40px;
        border: 1px solid #ececec;
    }
    /**重庆麻辣烫 */
    .title_left{
        position: absolute;
       display: inline-block;
       width:100px;
       top: 0px;
       left:5%;
      
    }
    /*商家处理 */
    .title_right{
        position: absolute;
        display: inline-block;
        width:80px; 
        top:0px;
        left:75%;
        
    }
    /**图片 */
    .IMgss{
        position: absolute;
        width: 120px;
        height:80px;
        top: 50px;
        left: 10px;
    }
    .IMgss img{
        width: 120px;
        height:80px;
    }
    /**价格 */
    .price{
        position: absolute;
        width:130px;
        height:80;
        color: #f00;
        left: 140px;
        top:80px;
    }
    /**下单时间 */
    .time{
        font-size:5px;
        color: darkgray;
    }
    /**总计 */
    .sum{
        position: absolute;
        width:150px;
        left: 60%;
        top:110px;
    }
    .sum p{
        font-size:10px;
        margin-left:40px;
        margin-bottom: 10px;
    }
    .sum button{
        width:70px;
        height:20px;
        font-size:6px; 
        border:1px solid #ececec;
        outline-style: none;
    }
    .btn1{
        
        background-color: #ffffff;
        margin-right:5px;
    }
    .btn2{
        background-color: #ef5f58;
    }
</style>