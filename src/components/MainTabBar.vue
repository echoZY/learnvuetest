<template>
  <div class="main-tabbar">
    <tab-bar>
      <tab-bar-item path="/home" defaultColor="deeppink">
        <img slot="item-icon" src="~assets/imgs/tabbar/home.svg" alt=""> 
        <img slot="item-icon-active" src="~assets/imgs/tabbar/home_active.svg" alt=""> 
        <div slot="item-content">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" defaultColor="deeppink">
        <img slot="item-icon" src="~assets/imgs/tabbar/category.svg" alt="">
        <img slot="item-icon-active" src="~assets/imgs/tabbar/category_active.svg" alt="">
        <div slot="item-content">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/shop" defaultColor="deeppink">
        <img slot="item-icon" src="~assets/imgs/tabbar/shopcart.svg" alt="">
        <img slot="item-icon-active" src="~assets/imgs/tabbar/shopcart_active.svg" alt="">
        <div slot="item-content">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" defaultColor="deeppink">
        <img slot="item-icon" src="~assets/imgs/tabbar/profile.svg" alt="">
        <img slot="item-icon-active" src="~assets/imgs/tabbar/profile_active.svg" alt="">
        <div slot="item-content">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>
<script>
import TabBar from '@/components/common/tabbar/TabBar';
import TabBarItem from '@/components/common/tabbar/TabBarItem';
export default {
name: 'MainTabBar',
  data() {
    return {
  }
},
  methods: {
},
  components: {
    TabBar,
    TabBarItem
  },
  created() {},
  mounted() {}
}
</script>
<style scoped>
</style>