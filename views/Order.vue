<template>
  <div>
    <p>蟹老板</p>
    <!-- 底部选项卡开始 -->
    <tabbar :selected="selected"></tabbar>
    <!-- 底部选项卡结束 -->
  </div>
</template>
<script>
// 导入子组件
import Tabbar from '../components/Tabbar.vue'

export default {
  components:{
    Tabbar
  },
  data(){
    return{
    // 默认被选中的底部选项卡
    selected:'order',
      
    }
  }
}
</script>