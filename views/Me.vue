<template>
  <div>
    <!-- 顶部头像开始 -->
    <div class="avater">
      <img src="../assets/avater/1.jpg" alt="">
      <div class="user-in">
        <a href="/login" class="login-in">登录</a>
        <a href="/register" class="register-in">注册</a>
      </div>
      <!-- <p>海绵宝宝,你好</p> -->
    </div>
    <!-- 顶部头像结束 -->
    <!-- 设置选项区域开始 -->
    <div class="select">
      <mt-cell title="优惠红包" isLink to="/senst">
        <img src="../assets/coupon.png" slot="icon">
      </mt-cell>
      <mt-cell title="我的消息" isLink to="/news">
        <img src="../assets/info.png" slot="icon">
      </mt-cell>      
      <mt-cell title="收货地址" isLink to="/lets">
        <img src="../assets/address.png" slot="icon">
      </mt-cell>
      <mt-cell title="邀请有礼" isLink to="/index">
        <img src="../assets/gitf.png" slot="icon">
      </mt-cell>
      <mt-cell title="联系客服" isLink to="/index">
        <img src="../assets/cell.png" slot="icon">
      </mt-cell>
      <mt-cell title="设置" isLink to="/index">
        <img src="../assets/setting.png" slot="icon">
      </mt-cell>                            
    </div>
    <!-- 设置选项区域结束 -->
    <!-- 退出登录按钮开始 -->
    <!-- <mt-button type="default" size="large">退出登录</mt-button> -->
    <!-- 退出登录按钮结束 -->
    <!-- 底部选项卡开始 -->
    <tabbar :selected="selected"></tabbar>
    <!-- 底部选项卡结束 -->
  </div>
</template>
<style scoped>
.avater{
  margin-bottom: 10px;
  text-align: center;
  background: #ef5f58;
}
.avater img{
  margin-top: 20px;
  width: 80px;
  height: 80px;
  border-radius: 100%;
}
.select{
  margin-top: 15px;
}
.login-in{
  display: block;
  width: 100px;
  height: 40px;
  background-color: #414141;
  text-decoration: none;
  color: #fff;
  line-height: 40px;
  border-radius: 20px;
  margin-left: 70px;
}
.register-in{
  display: block;
  width: 100px;
  height: 40px;
  /* background-color: #414141; */
  border: 2px solid #414141;
  text-decoration: none;
  color: #fff;
  line-height: 40px;
  border-radius: 20px;
  margin-left: 206px;
  margin-top: -40px;
}
</style>
<script>
// 导入底部选项卡子组件
import Tabbar from '../components/Tabbar.vue'
export default {
  components:{
    Tabbar
  },
  data(){
    return{
      // 默认底部被选定的选项卡
      selected:'me'
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