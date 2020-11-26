<template>
  <swiper>
      <swiper-item v-for="item in banners" :key="item.background">
        <a :href="item.link">
        <img :src="item.image" alt="">
      </a>
      </swiper-item>
    </swiper>
</template>

<script>
import {Swiper,SwiperItem} from 'components/common/swiper'

export default {
  name: 'HomeSwiper',
  props: {
    // 子组件用这个banners拿到父组件Home里的banners的参数
    banners: {
      type: Array,
      default() {
        return []
      }
    }
  },
  components: {
    Swiper,
    SwiperItem
  }
}
</script>

<style>

</style>