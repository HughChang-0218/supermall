<template>
  <div>
    <tab-bar :tabBarItem="tabBarItem" :activeColor="activeColor"></tab-bar>
  </div>
</template>

<script>
import TabBar from "components/common/tabbar/TabBar";

export default {
  name: "MainTabBar",
  components: {TabBar},
  data() {
    return {
      activeColor: "red",
      tabBarItem: [
        {
          icon: "\ue7a7",
          text: "首页",
          path: "/home"
        },
        {
          icon: "\ue6ef",
          text: "分类",
          path: "/category"
        },
        {
          icon: "\ue747",
          text: "购物车",
          path: "/cart"
        },
        {
          icon: "\ue7d4",
          text: "我的",
          path: "/profile"

        }]
    }
  }
}
</script>

<style scoped>

</style>
