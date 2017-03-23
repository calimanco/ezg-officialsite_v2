<template>
<header class="comHeader container">
  <div class="comHeader-logo">
    <a href="#"><img class="logo" src="../../assets/images/logo.png"></a>
  </div>
  <div class="comHeader-place">
    <a href="#" class="link">
      <i class="iconfont">+</i>
      <span>广东</span>
    </a>
  </div>
  <div class="comHeader-declare">
    <a href="#">
      <i class="hot">Hot</i>
      <span class="title">项目申报</span>
      <span class="info">政府奖励最高300万</span>
    </a>
  </div>
  <div class="comHeader-option">
    <div class="box">
      <a href="#">
        <i class="iconfont" v-bind:dataCount="cartCount">+</i>
        <span class="text">我的购物车</span>
        <i class="iconfont">+</i>
      </a>
    </div>
    <div class="box">
      <i class="iconfont">+</i>
      <span class="text" @click.stop.prevent="openMean">我的账柜</span>
      <ul v-if="isMean" class="mean">
        <li class="mean-list">我的服务</li>
        <li class="mean-list">我的订单</li>
      </ul>
      <i class="iconfont">+</i>
    </div>
  </div>
</header>
</template>

<script>
export default {
  name: 'comHeader',
  data() {
    return {
      isMean: false,
    };
  },
  props: {
    cartCount: Number,
  },
  methods: {
    openMean: function openMean() {
      if (this.isMean) {
        this.isMean = false;
      } else {
        this.isMean = true;
      }
    },
  },
  created() {
    document.addEventListener('click', (e) => {
      console.log(this.$el.querySelector('.box:last-child'));
      if (!this.$el.querySelector('.box:last-child').contains(e.target)) this.isMean = false;
    });
  },
};
</script>

<style lang="scss" scoped>@import "comHeader";</style>
