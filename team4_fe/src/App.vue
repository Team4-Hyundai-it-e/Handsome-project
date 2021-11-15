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

    <v-bottom-navigation app color="indigo" v-if="flag">
      <v-btn>
        <span>Recents</span>

        <v-icon>mdi-history</v-icon>
      </v-btn>

      <v-btn>
        <span>Favorites</span>

        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn>
        <span>Nearby</span>

        <v-icon>mdi-map-marker</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
import MainHeader from "./components/headers/MainHeader.vue";
export default {
  name: "App",

  data: () => ({
    swipeDirection: "None",
    flag : true
  }),
  components: { MainHeader },
  methods: {
    swipe(direction) {
      this.swipeDirection = direction;
      if(this.swipeDirection === "Down"){
        this.flag = true;
      }else{
        this.flag = false;
      }
    },
  },
};
</script>
