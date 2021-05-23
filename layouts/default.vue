<template>
  <!--  Vuetify有两个主要布局组件， v-app 和 v-main。 v-app 组件是您的应用程序的根节点，直接替换默认的 Vue 入口<div id="app">。 -->
  <!--  v-main 组件是替换 main HTML 元素和您应用程序的根节点 内容 的语义替代。 -->
  <!--  当Vue挂载到DOM时，作为布局一部分的任何Vuetify组件都会将其当前高度和/或宽度注册到框架核心。-->
  <!--  v-main 组件接下来需要这些值并调整容器的大小。-->
  <v-app>
    <!--    https://vuetifyjs.com/zh-Hans/features/layouts/#section-75284f8b-->

    <v-app-bar fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">Todo</span>
        <span>Ninja</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <!--      text 变透明-->
      <v-btn text color="grey">
        <span>Sign Out</span>
        <v-icon right>mdi-location-exit</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
        {
          icon: 'mdi-home',
          title: 'layout-test',
          to: '/layout-test',
        },
        {
          icon: 'mdi-apps',
          title: 'form-test',
          to: '/form-test',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
    }
  },
}
</script>
