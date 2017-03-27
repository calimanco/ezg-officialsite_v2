<template>
<header class="comHeader container">
  <div class="comHeader-logo">
    <a href="#"><img class="logo" src="../../assets/images/logo.png"></a>
    <p class="text">292529</p>
  </div>
  <div class="comHeader-place">
    <a href="#" class="link">
      <svg class="iconfont" aria-hidden="true">
            <use xlink:href="#icon-more"></use>
        </svg>
      <span class="text">广东</span>
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
        <i class="cart" :data-count="cartCount">
            <svg class="iconfont cart" aria-hidden="true">
                <use xlink:href="#icon-cart"></use>
            </svg>
        </i>
        <span class="text">我的购物车</span>
        <svg class="iconfont" aria-hidden="true">
            <use xlink:href="#icon-more"></use>
        </svg>
      </a>
    </div>
    <div class="box" @click.stop.prevent="openMean">
      <svg class="iconfont" aria-hidden="true">
          <use xlink:href="#icon-more"></use>
      </svg>
      <span class="text">我的账柜</span>
      <ul v-if="isMean" class="mean">
        <li class="mean-list"><a href="#">我的服务</a></li>
        <li class="mean-list"><a href="#">我的订单</a></li>
      </ul>
      <svg class="iconfont" aria-hidden="true">
          <use xlink:href="#icon-more"></use>
      </svg>
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
    openMean() {
      if (this.isMean) {
        this.isMean = false;
      } else {
        this.isMean = true;
      }
    },
  },
  created() {
    document.addEventListener('click', (e) => {
      if (!this.$el.querySelector('.box:last-child').contains(e.target)) this.isMean = false;
    });
  },
};
</script>

<style lang="scss" scoped>@import "comHeader";</style>
