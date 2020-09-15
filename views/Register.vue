<template>
  <div>
    <!-- 顶部导航 -->
    <mt-header title="注册">
      <router-link to="me" slot="left">
        <mt-button icon="back"></mt-button>
      </router-link>
    </mt-header>    
    <!-- 手机验证码开始 -->
    <h1 class="text">请输入手机号,加入蟹老板</h1>
    <mt-field
      type="text"
      placeholder="输入手机号"
      style="border:1px solid #ccc;margin-top:30px"
      state="phoneState"
      disableClear
      v-model="phone"
      @blur.native.capture="checkPhone">
      </mt-field>
    <!-- 手机验证码结束 -->
    <!-- 验证码输入框开始 -->
    <mt-field
      type="number"
      placeholder="输入验证码"
      style="border:1px solid #ccc;margin-top:30px"
      state="codeState"
      disableClear
      v-model="codenumber"
      @blur.native.capture="checkCode"
    >
      <!-- <mt-button type="danger" size="small" @click ="code">获取验证码</mt-button> -->
    <span class="codetxt" type="button" :disabled="disabled" @click="code">{{btntxt}}</span>
    </mt-field>
    <!-- 验证码输入框结束 -->
    <!-- 注册按钮 -->
    <mt-button type="danger" size="large" @click ="handle">快速注册</mt-button>
  </div>
</template>
<script>
export default {
  data(){
    return{
      // 手机号的初始值
      phone:"",
      // 验证码的初始值
      codenumber:"",
      // 手机号输入框的状态
      phoneState:"",
      // 验证码输入框的状态
      codeState:"",
      // 验证码的值
      btntxt:"获取验证码",
      // 禁用状态
      disabled:false,
      // 倒计时
      time:0,
    };
  },
  methods:{
    // 单击按钮时完成用户注册的信息的校验
    checkPhone(){
      // 1.校验手机号是否合法,规则为:1-11位的数字组成
      let phoneRegExp = /^((13[0-9])|(15[^4,\\D])|(18[0,0-9]))\\d{8}$/;
      if(phoneRegExp.test(this.phone)){
        this.phoneState = 'success';
        this.disabled=true;
        return true;
      } else {
        this.phoneState = 'error';
        this.$toast({
          message:'手机号输入不正确',
          position:'middle',
          duration:3000
        });
        return false;
      }
    },
    //验证验证码正确性
    checkCode(){
      // 校验手机号是否正确,规则为4为数字
      let codenumberRegExp = /$\d{4}$/;
      if(codenumberRegExp.test(this.codenumber)){
        return true;
      } else{
        this.$toast({
          message:'验证码不正确',
          position:'middle',
          duration:3000
        });
        return false;
      }
    },

    // 验证手机号码格式正确后才能点击 获取验证码按钮

    code(){
      if (this.time > 0) {
        this.time--;
        this.btntxt = this.time + "s后获取";
        setTimeout(this.timer, 1000);
      } else {
        this.time = 0;
        this.btntxt = "获取验证码";
        this.disabled = false;
      }
    },
    // 提交注册按钮
    handle(){
      // if (
      //   this.checkPhone() &&
      // ) {
      //   //将相关的信息提交到服务器
      //   this.axios
      //     .post(
      //       "/register",
      //       "phone=" + this.phone + "&codeState=" + this.codenumber
      //     )
      //     .then((res) => {
      //       //服务器响应信息中的code为0的情况下表示用户名已经存在
      //       if (res.data.codenumber == 0) {
      //         this.$messagebox("注册提示", "用户名已经被占用");
      //       } else {
              // this.$router.push("/");
            }
          // });
      }
    // },
    }

//   }
// }
</script>
<style scoped>
.text{
  font-size: 20px;
  text-align: center;
  color: #211d1d;
  margin-top: 30px;
}
</style>