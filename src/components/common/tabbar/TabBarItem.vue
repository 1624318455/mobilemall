<template>
    <div class="tab-bar-item" @click="itemClick">
      <!-- //因为slot会被到时候的内容替换掉所以绑定在slot上的属性有可能无法保存 -->
      <!-- <slot :class="{active:isActive}" name="item-text"></slot> -->
      <!-- 在slot外面包裹一层div 把不用替换的固定属性绑定到div上  这样的话 替换掉了插槽 属性也不会掉 -->
      <div v-if="!isActive"><slot name="item-icon"></slot></div>
      <div v-else><slot name="item-icon-focus"></slot></div>
      <!-- <div :class="{active: isActive}"><slot name="item-text"></slot></div> -->
      <div :style="activeStyle"><slot name="item-text"></slot></div>

        <!-- <img src="../../assets/img/tabbar/home.svg" alt=""> -->
        <!-- <div>首页</div> -->
    </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'red'
    }
  },
  data() {
    return {
      // isActive: true
    }
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle() {
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    itemClick() {
      // console.log('itemClick');
      this.$router.push(this.path)
    }
  }
}
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}

.tab-bar-item img {
  margin-top: 3px;
  width: 24px;
  height: 24px;
  vertical-align: middle;
}

/* .tab-bar-item .active{
  color: red;
} */
</style>