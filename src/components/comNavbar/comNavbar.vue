<template>
<nav class="comNavbar container clearfix">
  <div class="comNavbar-item mean" @mouseenter="openMean" @mouseleave="hideMean"> <span>帐柜服务</span>
    <ul class="comNavbar-mean" v-show="isShowMean">
      <li class="comNavbar-mean-item" v-for="(item, index) in meanItems" @mouseenter="openBox(index)" @mouseleave="closeBox(index)">
        <div class="link">
          <svg class="iconfont" aria-hidden="true">
            <use :xlink:href="item.icon"></use>
        </svg> {{ item.name }}
        </div>
        <div class="comNavbar-mean-box" v-show="index === showIndex">
          <div class="main">
            <div class="row" v-for="item in item.list">
              <div class="title"> <span>{{item.name}}</span> </div>
              <div class="list"> <a class="link" :href="item.link" v-for="item in item.list">{{item.name}}</a> </div>
            </div>
          </div>
          <div class="aside"> 这里是广告图 </div>
        </div>
      </li>
    </ul>
  </div>
  <div class="comNavbar-item important"> <a href="#" class="link">首页</a> </div>
  <div class="comNavbar-item hot"> <a href="#" class="link">限时优惠</a> </div>
  <div class="comNavbar-item new"> <a href="#" class="link">企业管家咨询</a> </div>
  <div class="comNavbar-item"> <a href="#" class="link">e动态</a> </div>
  <div class="comNavbar-item"> <a href="#" class="link">关于我们</a> </div>
  <div class="comNavbar-tel"> <svg class="iconfont" aria-hidden="true">
        <use xlink:href="#icon-more"></use>
    </svg> <span class="number">400-88-12580</span> </div>
</nav>
</template>

<script>
export default {
  name: 'comNavbar',
  data() {
    return {
      isShowMean: false,
      showIndex: -1,
      meanItems: [{
        name: '创办公司',
        icon: '#icon-more',
        list: [{
          name: '公司注册',
          list: [{
            name: '内资公司注册',
            link: '#',
          }, {
            name: '内资集团公司注册',
            link: '#',
          }, {
            name: '外贸公司注册',
            link: '#',
          }, {
            name: '合资公司注册',
            link: '#',
          }, {
            name: '香港公司注册',
            link: '#',
          }],
        }],
      }, {
        name: '财税服务',
        icon: '#icon-more',
        list: [{
          name: '公司注册',
          list: [{
            name: '内资公司注册',
            link: '#',
          }, {
            name: '内资集团公司注册',
            link: '#',
          }, {
            name: '外贸公司注册',
            link: '#',
          }, {
            name: '合资公司注册',
            link: '#',
          }],
        }],
      }, {
        name: '知识产权',
        icon: '#icon-more',
        list: [{
          name: '公司注册',
          list: [{
            name: '内资公司注册',
            link: '#',
          }, {
            name: '内资集团公司注册',
            link: '#',
          }, {
            name: '外贸公司注册',
            link: '#',
          }, {
            name: '合资公司注册',
            link: '#',
          }],
        }],
      }, {
        name: '资质办理',
        icon: '#icon-more',
        list: [{
          name: '公司注册',
          link: '#',
        }],
      }, {
        name: '代办中心',
        icon: '#icon-more',
        list: [{
          name: '公司注册',
          list: [{
            name: '内资公司注册',
            link: '#',
          }, {
            name: '内资集团公司注册',
            link: '#',
          }, {
            name: '外贸公司注册',
            link: '#',
          }, {
            name: '合资公司注册',
            link: '#',
          }, {
            name: '香港公司注册',
            link: '#',
          }, {
            name: '特殊核名',
            link: '#',
          }, {
            name: '刻章',
            link: '#',
          }],
        }],
      }],
    };
  },
  methods: {
    openMean() {
      this.isShowMean = true;
    },
    hideMean() {
      this.isShowMean = false;
    },
    openBox(index) {
      this.showIndex = index;
    },
    closeBox() {
      this.showIndex = -1;
    },
  },
};
</script>

<style lang="scss" scoped>@import "comNavbar";</style>
