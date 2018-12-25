<template>
  <div class="indexPage">
    <header>{{msg}}</header>
    <mt-swipe class="mt-swipe" @change="handleChange">
      <mt-swipe-item class="mt-swipe-item">
        <img src="../../static/img/banner.png" alt>
      </mt-swipe-item>
    </mt-swipe>
    <div class="weather">
      <div class="icon-zelvgongyongyonghuzhongxinz003">
        <p>智能天气推送</p>
        <p>智能天气推送</p>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import { Swipe, SwipeItem } from "mint-ui";

Vue.component(Swipe.name, Swipe);
Vue.component(SwipeItem.name, SwipeItem);

export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "悦农通",
      banner: ["../../static/img/banner.png"]
    };
  },
  methods: {
    handleChange(index) {
      console.log(index);
    }
  }
};
</script>

<style lang='less' scoped>
.indexPage {
  header {
    width: 100%;
    height: 88px;
    text-align: center;
    line-height: 88px;
    background: linear-gradient(30deg, #1b9de1, #38bbf0, #4dc5f4);
    color: #fff;
    font-size: 28px;
  }
  .mt-swipe {
    height: 300px;
    overflow: hidden;
    .mt-swipe-item {
      height: 300px;
      background: #1b9de1;
      img {
        width: 100%;
      }
    }
  }
  .weather {
    .left {
      overflow: hidden;
      width: 750px;
      height: 80px;
      width: green;
      p {
        width: 670px;
        background: orange;
      }
    }
    
  }
}
</style>
