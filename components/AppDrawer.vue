<template>
  <v-navigation-drawer id="appDrawer" v-model="drawer" fixed app>
    <v-list dense>
      <v-list-item @click>
        <v-list-item-action>
          <v-icon>mdi-view-dashboard</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Dashboard</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-list-group prepend-icon="mdi-home" value="true">
        <template v-slot:activator>
          <v-list-item-title>Resources</v-list-item-title>
        </template>

        <v-list-item v-for="(resource, i) in resources" :key="i" link>
          <v-list-item-action>
            <v-icon v-text="resource[1]"></v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="resource[0]"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>

      <v-list-item @click>
        <v-list-item-action>
          <v-icon>mdi-account-multiple</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Team Members</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: 'AppDrawer',
  data: () => ({
    resources: [['UI/UX', 'mdi-cursor-pointer'], ['DevOps', 'mdi-polymer'], ]
  }),
  computed: {
    drawer: {
      get() {
        return this.$store.state.drawer
      },
      set(val) {
        this.$store.commit('drawer', val)
      }
    }
  }
}
</script>