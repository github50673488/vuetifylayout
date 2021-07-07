<template>
  <div>
    <!--    <div class="subheading grey&#45;&#45;text">Dashboard</div>-->
    <v-subheader class="grey--text">Dashboard</v-subheader>
    <v-container>
      <!--      #v-row-->
      <!--      v-row 是 v-col 的容器组件。 它使用 flex 属性来控制其内栏的布局和流。 -->
      <!--      它使用的是 24px 的标准间隔。 这可以用 dense 属性来减小，或者用 no-gutters 来完全去除。 -->
      <!--      这是 2.x 版本对 1.x 版本中 v-layout 的替代。-->
      <v-row dense>
        <!--        新版本的vuetify不能写xs="12" 而是写 cols="12"-->
        <v-col cols="12" md="6">
          <!--          添加block 属性，按钮将延占满可用的宽度-->
          <v-card outlined class="text-center">row1-col1</v-card>
        </v-col>
        <!--        不能在 v-col中加间隙 （如 class= 'pa-1'），这将破坏网格布局-->
        <v-col cols="4" md="2">
          <v-card outlined>row1-col2</v-card>
        </v-col>
        <v-col cols="4" md="2">
          <!--        可以统一在在 v-col中的元素中加间隙调整布局，但是一般不这么做，
          因为 ma1 已经相当于·v-row中的dence -->
          <v-card outlined>row1-col3</v-card>
        </v-col>
        <v-col cols="4" md="2">
          <v-card outlined>row1-col4</v-card>
        </v-col>
      </v-row>

      <v-row dense class="flex-row-reverse justify-space-around">
        <v-col cols="4" md="3">
          <v-card outlined class="success">row2-col1</v-card>
        </v-col>
        <v-col cols="4" md="3">
          <v-card outlined class="success">row2-col2</v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {}
</script>

<style scoped></style>
