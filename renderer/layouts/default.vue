<template>
  <v-app :dark="ubahGan">
    <v-toolbar color="primary" dark>
      <v-toolbar-side-icon @click.native.stop="drawer = !drawer" />
      <v-toolbar-title @click="ubahGan=!ubahGan">Go Market Place</v-toolbar-title>
    </v-toolbar>
    <v-navigation-drawer v-model="drawer" left fixed app>
      <v-list>
        <v-list-tile router nuxt :href="resolve('home')">
          <v-list-tile-title>Home</v-list-tile-title>
        </v-list-tile>
        <v-list-tile router nuxt :href="resolve('about')">
          <v-list-tile-title>About</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <main>
      <v-content>
        <v-container fluid>
          <nuxt />
        </v-container>
      </v-content>
    </main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      ubahGan: false
    };
  },
}
</script>

<style scoped>
  .title {
    padding-left: 20px;
  }
</style>
