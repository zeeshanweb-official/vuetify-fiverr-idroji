<template>
  <v-app :class="{'biggerscreen': $vuetify.breakpoint.lgAndUp}">
    <appNavbar></appNavbar>
    <v-content style="padding:0px;">
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import navbar from "@/components/navbar.vue";
export default {
  name: "App",
  components: {
    appNavbar: navbar
  },
  data: () => ({
    //
  })
};
</script>
<style scoped>
.v-content {
  padding-bottom: 0% !important;
}
.biggerscreen {
  width: 80%;
  margin-left: 20%;
}
</style>
