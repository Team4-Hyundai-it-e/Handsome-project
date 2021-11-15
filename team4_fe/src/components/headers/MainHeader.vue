<template>
  <v-app-bar app color="black" dark hide-on-scroll>
    <v-spacer></v-spacer>

    <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>mdi-shopping-outline</v-icon>
    </v-btn>

    <template v-slot:extension>
      <v-tabs class="sticky" show-arrows >
        <v-tab :value="1">Home</v-tab>
        <v-tab :value="2">Best</v-tab>
        <v-tab :value="3">New</v-tab>
        <v-tab :value="4">Tab 4</v-tab>
        <v-tab :value="5">Tab 5</v-tab>
        <v-tab :value="6">Tab 6</v-tab>
      </v-tabs>
    </template>
  </v-app-bar>
</template>

<script>
export default {
  name: "MainHeader",
};
</script>

<style></style>
