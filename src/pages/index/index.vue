<template>
<div id="app1">
  <comHeader v-bind:cart-count="cartCount"></comHeader>
  <comNavbar></comNavbar>
  <div class="">
      <svg class="iconfont withShadow" aria-hidden="true">
          <use xlink:href="#icon-xxx"></use>
      </svg>
  </div>


</div>
</template>

<script>
import comHeader from '../../components/comHeader/comHeader';
import comNavbar from '../../components/comNavbar/comNavbar';
import '../../assets/scripts/iconfont.exec';

export default {
  name: 'app',
  data() {
    return {
      cartCount: 5,
    };
  },
  components: {
    comHeader,
    comNavbar,
  },

};
</script>

<style lang="scss">@import "index.scss";</style>
