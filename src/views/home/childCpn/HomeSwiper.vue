<template>
  <van-swipe :autoplay="3000">
    <van-swipe-item v-for="(item, index) in banners" :key="index" class="home_swiper_item">
      <a :href="item.link" class="myswiper">
        <img :src="item.image" class="swipe_item_img"/>
      </a>
    </van-swipe-item>
  </van-swipe>
</template>

<script>
import { Swipe,SwipeItem } from "vant"

  export default {
    name: "HomeSwiper",
    props: {
      banners: {
        type: Array,
        default() {
          return []
        }
      }
    },
    components: {
      [Swipe.name]: Swipe,
      [SwipeItem.name]: SwipeItem
    }
  }
</script>

<style scoped>
.swipe_item_img{
  width: 100%;
}
</style>
