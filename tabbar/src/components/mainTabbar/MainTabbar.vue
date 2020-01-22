<template>
  <tabbar>
    <tabbar-item path="/home" activeColor="red">
      <img slot="tabbar-icon" src="~assets/imgs/logo.png">
      <img src="~assets/imgs/avatar2.jpg" alt="" slot="tabbar-icon-active">
      <div slot="tabbar-text">首页</div>
    </tabbar-item>
    <tabbar-item path="/category" activeColor="blue">
      <img slot="tabbar-icon" src="~assets/imgs/logo.png">
      <img src="~assets/imgs/avatar2.jpg" alt="" slot="tabbar-icon-active">
      <div slot="tabbar-text">分类</div>
    </tabbar-item>
    <tabbar-item path="/cart" activeColor="blue">
      <img slot="tabbar-icon" src="~assets/imgs/logo.png">
      <img src="~assets/imgs/avatar2.jpg" alt="" slot="tabbar-icon-active">
      <div slot="tabbar-text">购物车</div>
    </tabbar-item>
    <tabbar-item path="/profile" activeColor="blue">
      <img slot="tabbar-icon" src="~assets/imgs/logo.png">
      <img src="~assets/imgs/avatar2.jpg" alt="" slot="tabbar-icon-active">
      <div slot="tabbar-text">我的</div>
    </tabbar-item>
  </tabbar>

</template>

<script>
  import Tabbar from "../TabBar/Tabbar"
  import TabbarItem from "../TabBar/TabbarItem"
    export default {
        name: "MainTabbar",
        components:{
          TabbarItem,
          Tabbar
        }
    }
</script>

<style scoped>

</style>
