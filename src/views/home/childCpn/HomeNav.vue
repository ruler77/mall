<template>
  <div class="home_nav">
    <nav-bar>
      <template v-slot:center><div class="nav_title">购物街</div></template>
    </nav-bar>
  </div>
</template>


<script>
import NavBar from "@/components/common/navbar/NavBar"
export default {
  name: 'HomeNav',
  components: {
    NavBar
  }
}
</script>

<style scoped>
.nav_title{
  font-weight: 400;
  color: white;
}
.home_nav{
  background-color: #ff8198;
  width: 100%;

  position: fixed;
  z-index: 9;
}
</style>
