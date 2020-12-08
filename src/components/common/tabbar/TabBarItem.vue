<template>
  <div id="tab-bar-item" @click="itemClick" :style="activeStyle">
    <slot name="item-icon"></slot>
    <slot name="item-text"></slot>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    path: String,
    activeColor: {
      type: String,
      default: "red"
    }
  },
  computed: {
    activeStyle() {
      return this.$route.path.indexOf(this.path) !== -1 ? {color: this.activeColor} : {};
    }
  },
  methods: {
    itemClick() {
      if (this.$route.path.indexOf(this.path) === -1) {
        this.$router.replace(this.path);
      }
    }
  }
}
</script>

<style scoped>
#tab-bar-item {
  flex: 1;
  height: 49px;
  text-align: center;
  margin-bottom: 2px;
}

#tab-bar-item .tab-bar-icon {
  font-size: 24px;
  margin-top: 2px;
  margin-bottom: 2px;
  vertical-align: middle;
}
</style>
