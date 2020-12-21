<template>
  <tab-bar>
    <!--      activeColor="blue" 可以改字体颜色 不写的时候，会显示默认颜色 -->
    <!--      <tab-bar-item path="/category" activeColor="blue" >-->
    <tab-bar-item path="/home" >
      <img slot="item-icon" src="../assets/imgs/tabbar/home.svg" alt="">
      <img slot="active-item-icon" src="../assets/imgs/tabbar/active-home.svg" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>

    <tab-bar-item path="/category"  >
      <img slot="item-icon" src="../assets/imgs/tabbar/category.svg" alt="">
      <img slot="active-item-icon" src="../assets/imgs/tabbar/active-category.svg" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>

    <tab-bar-item path="/cart" >
      <img slot="item-icon" src="../assets/imgs/tabbar/cart.svg" alt="">
      <img slot="active-item-icon" src="../assets/imgs/tabbar/active-cart.svg" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>

    <tab-bar-item path="/profile" >
      <img slot="item-icon" src="../assets/imgs/tabbar/profile.svg" alt="">
      <img slot="active-item-icon" src="../assets/imgs/tabbar/active-profile.svg" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>

  </tab-bar>
</template>

<script>
import TabBar from '../components/tabbar/TabBar'
import TabBarItem from "../components/tabbar/TabBarItem";

export default {
name: "MainTabBar",
components:{
  TabBar,
  TabBarItem
}
}
</script>

<style scoped>

</style>
