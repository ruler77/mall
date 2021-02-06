<template>
  <div id="TabControl" class="tabControl">
    <div v-for="(item,index) in titles" 
        class="tabcontrol-item"
        :class="{active: currentIndex === index}"
        @click="itemClick(index)"
        :key="index">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabControl",
  props: {
    titles: {
      type: Array,
      default(){
        return ['流行', '新款', '精选']
      }
    }
  },
  data() {
    return {
      currentIndex: 0
    }
  },
  methods:{
    itemClick(index){
      this.currentIndex = index
    }
  }
}
</script>

<style scoped>
  .tabControl{
    display: flex;
    text-align: center;
    font-size: 15px;
    padding: 5px 0;
    line-height: 40px;
    background-color: #fff;
  }

  .tabcontrol-item{
    flex: 1;
  }

  .tabcontrol-item span{
    padding: 0 5px 3px;
  }

  .tabcontrol-item.active span{
    border-bottom: 2px solid var(--color-high-text);
    color: var(--color-high-text);
  }
</style>
