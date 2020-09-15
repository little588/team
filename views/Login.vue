<template>
  <div>
    <!-- 顶部导航栏开始 -->
    <mt-header title="登录">
      <router-link to="/me" slot="left">
        <mt-button icon="back"></mt-button>
      </router-link>
    </mt-header>
    <!-- 顶部导航栏结束 -->
    <!-- 用户名 -->
    <mt-field
      class="field"
      type="text"
      :state="usernameState"
      placeholder="请输入用户名/邮箱/手机号"
      @blur.native.capture="checkUsername"
      disableClear
      v-model="username">
    </mt-field>
    <!-- 密码框 -->
    <mt-field
      type="password"
      placeholder="密码"
      :state="passwordState"
      :attr="{maxlength:'20',autocomplete:'off'}"
      v-model="password"
      @blur.native.capture="checkPassword"
    ></mt-field>
    <!-- 注册文本框结束 -->
    <!-- 忘记密码 -->
    <div style="margin-bottom: 20px;border-top:1px solid rgb(190 183 183)">
    <a href="/me" class="forget">忘记密码</a>    
    </div> 
    <!-- 注册按钮开始 -->
    <mt-button type="danger" size="large" @click="handle">登录</mt-button>
    <!-- 注册按钮结束 -->
    <!-- 蟹老板协议 -->
    <div class="login">
      <label class="login-cd">
        <input id="login" type="checkbox" class="login-cd">
          同意
          <a href="/me">&lt;&lt;蟹老板用户协议&gt;&gt;</a>
          和
          <a href="/me">&lt;&lt;隐私政策&gt;&gt;</a>
        <!-- </input> -->
      </label>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      // 用户名的初始值
      username:'',
      // 密码的初始值
      password:'',
      // 用户名输入框的状态
      usernameState:'',
      // 密码输入框的状态
      passwordState:'',
    }
  },
  methods:{
    // 检测用户名
    checkUsername(){
      let usernameRexExp = /^[a-zA-Z0-9_]{6,12}$/;
      if(usernameRexExp.test(this.username)){
        this.usernameState = 'success';
        return true;
      }else{
        this.usernameState = 'error';
        this.$totast({
          message:"用户名错误",
          position:"middle",
          duration:5000
        });
        return false;
      }
    },

      // 检测密码
      checkPassword(){
      let passwordRegExp = /^[a-zA-Z0-9_]{8,20}$/;
      if (passwordRegExp.test(this.password)) {
        this.passwordState = "success";
        return true;
      } else {
        this.passwordState = "error";
        this.$toast({
          message: "密码错误",
          position: "middle",
          duration: 3000,
        });
        return false;
      }
    },

    // 单击按钮是完成用户登录的信息的校验
    handle(){
      if(this.checkUsername() && this.checkPassword()){
        // 将相关的信息提交到服务器
        this.axios.post("/login","Username=" + this.username + "&password=" + this.password)
        .then((res)=>{
          if(res.data.code == 0){
            this.$messagebox("登录提示","用户登录失败");
          }else{
            this.$router.push("/");
          }
        });
      }
    }
  },
}
</script>
<style scoped>
.i{
  width:40px;
  height: 40px;
}
.p{
  font-size: 20px;
  color: #414141;
  margin-left: 25px;
}
.field{
  margin-top: 50px;
}
.forget{
  margin-top: 10px;
  text-decoration: none;
  color: #414141;
  font-size: 18px;
}
.login{
  margin-top: 335px;
  font-size: 17px;
}
.login-cd>a{
  text-decoration: none;
  color: #ef5f58;
}
</style>