<template>
  <div class="btn-and-icon">
    <h1>btn and icon</h1>
    <v-btn class="pink white--text">click me</v-btn>
    <v-btn depressed dark color="pink">click me</v-btn>
    <!--    <v-btn flat color="pink">click me</v-btn>  2.0 flat 不用了 改成 outlined ？ 移除卡片的海拔-->
    <v-btn flat color="pink" outlined>click me</v-btn>

    <!--    https://materialdesignicons.com/-->
    <v-btn depressed class="pink white--text">
      <v-icon left>mdi-email-outline</v-icon>
      <span>email me</span>
    </v-btn>

    <v-btn depressed small class="pink white--text">
      <v-icon left small>mdi-email-outline</v-icon>
      <span>email me</span>
    </v-btn>

    <v-btn depressed large class="pink white--text">
      <span>email me </span>
      <v-icon right large>mdi-email-outline</v-icon>
    </v-btn>

    <!-- fab   Designates the button as a floating-action-button. Button will become round.-->
    <v-btn fab dark small depressed color="purple">
      <v-icon dark>mdi-heart-outline</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  name: 'P05ButtonAndIcons',
}
</script>

<style scoped></style>
