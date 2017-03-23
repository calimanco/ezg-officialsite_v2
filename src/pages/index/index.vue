<template>
<div id="app1">
  <comHeader></comHeader>
  <comNavbar></comNavbar>
</div>
</template>

<script>
import comHeader from '../../components/comHeader/comHeader';
import comNavbar from '../../components/comNavbar/comNavbar';

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
