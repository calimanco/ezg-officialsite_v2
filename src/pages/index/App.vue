<template>
<div id="app1">
  <img src="../../assets/images/logo.png">
  <hello></hello>
</div>
</template>

<script>
import Hello from '../../components/Hello';

export default {
  name: 'app',
  components: {
    Hello,
  },
};
</script>

<style lang="scss">@import "index.scss";</style>
