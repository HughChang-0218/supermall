<template>
  <div id="tab-bar">
    <tab-bar-item v-for="(item,index) in tabBarItem" :key="index" :path="item.path" :activeColor="activeColor">
      <div slot="item-icon" class="tab-bar-icon">{{ item.icon }}</div>
      <div slot="item-text">{{ item.text }}</div>
    </tab-bar-item>
  </div>
</template>

<script>
import TabBarItem from "components/common/tabbar/TabBarItem";

export default {
  name: "TabBar",
  components: {
    TabBarItem
  },
  props: {
    tabBarItem: Array,
    activeColor: String
  }
}
</script>

<style scoped>
@import "~assets/css/tab-bar-icons.css";

#tab-bar {
  display: flex;
  background-color: #f6f6f6;
  box-shadow: 0 -1px 1px rgba(100, 100, 100, 0.1);

  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
}
</style>
