<template>
  <v-app
    v-touch="{
      left: () => swipe('Left'),
      right: () => swipe('Right'),
      up: () => swipe('Up'),
      down: () => swipe('Down'),
    }"
  >
    <main-header />

    <v-main>
      <v-container fluid>
        <router-view />
      </v-container>
    </v-main>

    <v-bottom-navigation app v-if="flag">
      <main-footer />
    </v-bottom-navigation>
  </v-app>
</template>

<script>
import MainFooter from "./components/footer/MainFooter.vue";
import MainHeader from "./components/headers/MainHeader.vue";
export default {
  name: "App",

  data: () => ({
    swipeDirection: "None",
    flag: true,
  }),
  components: { MainHeader, MainFooter },
  methods: {
    swipe(direction) {
      this.swipeDirection = direction;
      if (this.swipeDirection === "Down") {
        this.flag = true;
      } else {
        this.flag = false;
      }
    },
  },
};
</script>
