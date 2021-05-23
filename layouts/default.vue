<template>
  <!--  Vuetify有两个主要布局组件， v-app 和 v-main。 v-app 组件是您的应用程序的根节点，直接替换默认的 Vue 入口<div id="app">。 -->
  <!--  v-main 组件是替换 main HTML 元素和您应用程序的根节点 内容 的语义替代。 -->
  <!--  当Vue挂载到DOM时，作为布局一部分的任何Vuetify组件都会将其当前高度和/或宽度注册到框架核心。-->
  <!--  v-main 组件接下来需要这些值并调整容器的大小。-->
  <v-app>
    <!--    https://vuetifyjs.com/zh-Hans/features/layouts/#section-75284f8b-->

    <v-navigation-drawer v-model="drawer" app class="primary">
      <!-- 这里 primary变成了紫色     主题 编辑 https://vuetifyjs.com/en/features/theme/#customizing-->
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          router
          :to="item.to"
          exact
        >
          <v-list-item-action>
            <v-icon color="white">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title class="white--text" v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!--注意在不同大小的时候，navigation-drawer 盖不盖住toolbar的行为是不同的。窗口变大的时候，是推开的！-->
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
      <v-container class="mx-4 mb-4">
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
      drawer: true,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Darshborad',
          to: '/',
        },
        {
          icon: 'mdi-projector-screen-outline',
          title: 'my projects',
          to: '/projects',
        },
        {
          icon: 'mdi-microsoft-teams',
          title: 'team',
          to: '/team',
        },
        {
          icon: 'mdi-card-text',
          title: 'p04-text-and-color',
          to: '/p04-text-and-color',
        },
        {
          icon: 'mdi-gesture-tap-button',
          title: 'p05-button-and-icons',
          to: '/p05-button-and-icons',
        },
        {
          icon: 'mdi-format-page-break',
          title: 'p06-breakpoints',
          to: '/p06-breakpoints',
        },
        {
          icon: 'mdi-format-page-break',
          title: '居中',
          to: '/center',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
    }
  },
}
</script>
