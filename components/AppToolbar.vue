<template>
  <v-app-bar app color="indigo" dark>
    <v-app-bar-nav-icon @click.stop="toggleDrawer()"></v-app-bar-nav-icon>
    <v-toolbar-title>CSE Resources Platform</v-toolbar-title>
     <v-spacer></v-spacer>
    <v-btn icon href="https://github.com/amyloula/dev-resources-dashboard">
      <v-icon>mdi-github-circle</v-icon>
    </v-btn>
    <v-btn icon @click="">
      <v-icon>mdi-settings</v-icon>
    </v-btn>
     <v-btn icon>
        <v-avatar size="30px">
          <img src="../static/avatar/naomi.JPG" alt="Naomi Quinn"/>
        </v-avatar>
      </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: 'AppToolbar',

  methods: {
    toggleDrawer() {
      this.$store.commit('toggleDrawer')
    }
  }
}
</script>