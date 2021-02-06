<template>
  <div class="home">
    <home-nav></home-nav>
    <home-swiper :banners="banners"></home-swiper>
    <recommend-view :recommends="recommends"></recommend-view>
    <feature-view></feature-view>
    <tab-control :titles="['流行', '新款', '精选']" class="tab_control_auto"></tab-control>
    <ul>
      <li>text001</li>
      <li>text002</li>
      <li>text003</li>
      <li>text004</li>
      <li>text005</li>
      <li>text006</li>
      <li>text007</li>
      <li>text008</li>
      <li>text009</li>
      <li>text010</li>
      <li>text011</li>
      <li>text012</li>
      <li>text013</li>
      <li>text014</li>
      <li>text015</li>
      <li>text016</li>
      <li>text017</li>
      <li>text018</li>
      <li>text019</li>
      <li>text020</li>
      <li>text021</li>
      <li>text022</li>
      <li>text023</li>
      <li>text024</li>
      <li>text025</li>
      <li>text026</li>
      <li>text027</li>
      <li>text028</li>
      <li>text029</li>
      <li>text030</li>
      <li>text031</li>
      <li>text032</li>
      <li>text033</li>
      <li>text034</li>
      <li>text035</li>
      <li>text036</li>
      <li>text037</li>
      <li>text038</li>
      <li>text039</li>
      <li>text040</li>
      <li>text041</li>
      <li>text042</li>
      <li>text043</li>
      <li>text044</li>
      <li>text045</li>
      <li>text046</li>
      <li>text047</li>
      <li>text048</li>
      <li>text049</li>
      <li>text050</li>
      <li>text051</li>
      <li>text052</li>
      <li>text053</li>
      <li>text054</li>
      <li>text055</li>
      <li>text056</li>
      <li>text057</li>
      <li>text058</li>
      <li>text059</li>
      <li>text060</li>
      <li>text061</li>
      <li>text062</li>
      <li>text063</li>
      <li>text064</li>
      <li>text065</li>
      <li>text066</li>
      <li>text067</li>
      <li>text068</li>
      <li>text069</li>
      <li>text070</li>
      <li>text071</li>
      <li>text072</li>
      <li>text073</li>
      <li>text074</li>
      <li>text075</li>
      <li>text076</li>
      <li>text077</li>
      <li>text078</li>
      <li>text079</li>
      <li>text080</li>
      <li>text081</li>
      <li>text082</li>
      <li>text083</li>
      <li>text084</li>
      <li>text085</li>
      <li>text086</li>
      <li>text087</li>
      <li>text088</li>
      <li>text089</li>
      <li>text090</li>
      <li>text091</li>
      <li>text092</li>
      <li>text093</li>
      <li>text094</li>
      <li>text095</li>
      <li>text096</li>
      <li>text097</li>
      <li>text098</li>
      <li>text099</li>
      <li>text100</li>
    </ul>
  </div>
</template>

<script>
import HomeNav from "@/views/home/childCpn/HomeNav"
import HomeSwiper from "@/views/home/childCpn/HomeSwiper"
import RecommendView from "@/views/home/childCpn/RecommendView"
import FeatureView from "@/views/home/childCpn/FeatureView"

import TabControl from "@/components/content/tabcontrol/TabControl"

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
    RecommendView,
    FeatureView,
    TabControl
  },
  created() {
    // 1.请求多个数据
    getHomeMultidata().then(res => {
      // this.result = res;
      console.log(res)
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    })
  }
}
</script>

<style scoped>
.tab_control_auto{
  position: sticky;
  top: 44px;
}
</style>
