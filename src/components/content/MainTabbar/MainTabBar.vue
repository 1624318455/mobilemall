<template>
  <tab-bar>
    <tab-bar-item path="/home" activeColor="blue">
      <!-- 将内容填充到对应slot属性的地方 -->
      <img slot="item-icon" src="~assets/img/tabbar/home.svg" alt="" />
      <img slot="item-icon-focus" src="~assets/img/tabbar/home_focus.svg" alt="" />
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" activeColor="blue">
      <img slot="item-icon" src="~assets/img/tabbar/category.svg" alt="" />
      <img slot="item-icon-focus" src="~assets/img/tabbar/category_focus.svg" alt="" />
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/shopcart" activeColor="blue">
      <img slot="item-icon" src="~assets/img/tabbar/shopcart.svg" alt="" />
      <img slot="item-icon-focus" src="~assets/img/tabbar/shopcart_focus.svg" alt="" />
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile" activeColor="blue">
      <img slot="item-icon" src="~assets/img/tabbar/profile.svg" alt="" />
      <img slot="item-icon-focus" src="~assets/img/tabbar/profile_focus.svg" alt="" />
      <div slot="item-text">我的</div>
    </tab-bar-item>
    <tab-bar>
</template>

<script>
import TabBar from "components/common/tabbar/TabBar";
import TabBarItem from "components/common/tabbar/TabBarItem";

export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem,
  },
};
</script>

<style>
/* 在style里引用要用 @import */
/* @import "./assets/css/base.css"; */
</style>