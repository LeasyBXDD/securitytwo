<template>
  <a-layout class="layout">
    <a-layout-header :style="{ position: 'fixed', zIndex: 1, width: '100%' }">

      <a-menu v-model:selectedKeys="selectedKeys" theme="dark" mode="horizontal" :style="{ lineHeight: '64px' }">
        <a-menu-item key="1">
          <router-link to="/">介绍</router-link>
        </a-menu-item>
        <a-menu-item key="2">
          <router-link to="/vp">【我们】VP Sentinel 安全声纹识别模型</router-link>
        </a-menu-item>
        <a-menu-item key="3">
          <router-link to="/ogone">【其他】ECAPA-TDNN 声纹识别模型</router-link>
        </a-menu-item>
        <a-menu-item key="4">
          <router-link to="/ogtwo">【其他】x-vector 声纹识别模型</router-link>
        </a-menu-item>
        <a-menu-item key="5">
          <router-link to="/ogthree">【其他】r-vector 声纹识别模型</router-link>
        </a-menu-item>
        <a-menu-item key="6">
          <router-link to="/ogfour">【其他】ResNet 声纹识别模型</router-link>
        </a-menu-item>
        <a-menu-item key="7" style="margin-left: 0px;">
          <router-link to="/login">登录</router-link>
        </a-menu-item>
        <a-menu-item key="8">
          <router-link to="/register">注册</router-link>
        </a-menu-item>
      </a-menu>

    </a-layout-header>


    <a-layout-content style="padding: 0 50px; margin-top: 80px;">
      <div :style="{ background: '#fff', padding: '24px', minHeight: '660px' }">
        <div>
          <router-view />
        </div>
      </div>
    </a-layout-content>


    <a-layout-footer style="text-align: center">
      <p>VP Sentinel：基于GAN的安全声纹识别系统</p>
      <p>第十六届全国大学生信息安全竞赛</p>
    </a-layout-footer>


  </a-layout>
</template>
<script>
import { defineComponent, ref } from 'vue';
export default defineComponent({
  
  setup() {
    return {
      selectedKeys: ref(['1']),
    };
  },
});
</script>
<style>
.site-layout-content {
  min-height: 280px;
  padding: 24px;
  background: #fff;
}

#components-layout-demo-top .logo {
  float: left;
  width: 120px;
  height: 31px;
  margin: 16px 24px 16px 0;
  background: rgba(255, 255, 255, 0.3);
}

.ant-row-rtl #components-layout-demo-top .logo {
  float: right;
  margin: 16px 0 16px 24px;
}

[data-theme='dark'] .site-layout-content {
  background: #141414;
}
</style>