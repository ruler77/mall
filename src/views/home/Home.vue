<template>
  <div class="home">
    <home-nav></home-nav>
    <home-swiper :banners="banners"></home-swiper>
    <recommend-view :recommends="recommends"></recommend-view>
  </div>
</template>

<script>
import HomeNav from "@/views/home/childCpn/HomeNav"
import HomeSwiper from "@/views/home/childCpn/HomeSwiper"
import RecommendView from "@/views/home/childCpn/RecommendView"


import {getHomeMultidata} from "network/home"
export default {
  name: 'Home',
  data() {
    return {
      banners: [],
      recommends: []
    }
  },
  components: {
    HomeNav,
    HomeSwiper,
    RecommendView
  },
  created() {
    // 1.请求多个数据
    getHomeMultidata().then(res => {
      // this.result = res;
      // console.log(res)
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    })
  }
}
</script>

<style scoped>

</style>
