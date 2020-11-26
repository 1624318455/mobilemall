<template>
  <div class="nav-bar">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>
  </div>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style>
  .nav-bar {
    display: flex;
    line-height: 44px;
    height: 44px;
    text-align: center;
    box-shadow: 0 2px 4px rgba(100, 100, 100, 0.1);
  }

  .left, .right {
    width: 60px;
    /* background-color: aquamarine; */
  }

  .center {
    /* 左右设置了具宽，flex:1自动填满剩下的空白 */
    flex: 1;
    /* background-color: aqua; */
  }
</style>