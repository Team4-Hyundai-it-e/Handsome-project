<template>
  <div class="d-flex">
    <v-btn class="pa-0">
      <span class="font-weight-bold">recent</span>
      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn class="pa-0">
      <span class="text-sm font-weight-bold">like</span>
      <v-icon>mdi-cards-heart-outline </v-icon>
    </v-btn>

    <v-btn class="pa-0">
      <span class="text-sm font-weight-bold">home</span>
      <v-icon>mdi-home-outline </v-icon>
    </v-btn>

    <v-btn class="pa-0">
      <span class="text-sm font-weight-bold">my</span>
      <v-icon color="gray">mdi-account-outline </v-icon>
    </v-btn>

    <v-btn class="pa-0">
      <span class="text-sm font-weight-bold">menu</span>
      <v-icon>mdi-menu</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "MainFooter",
};
</script>

<style scoped></style>
