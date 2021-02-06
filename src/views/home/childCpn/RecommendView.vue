<template>
  <div id="recommendView" class="recommend">
    <div v-for="(item,index) in recommends" :key="index" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecommendView",
  props: {
    recommends: {
      type: Array,
      default(){
        return []
      }
    }
  },
  data() {
    return {

    }
  },
  components: {
  }
}
</script>

<style scoped>
  .recommend{
    display: flex;
    width: 100%;
    text-align: center;
    font-size: 14px;
    padding: 7px 0 18px;
    border-bottom: 8px solid #eee;
  }

  .recommend-item{
    flex: 1;
  }

  .recommend-item img{
    height: 64px;
    height: 64px;
    margin-bottom: 3px;
  }
</style>
