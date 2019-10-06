<template>
  <v-navigation-drawer id="appDrawer" v-model="drawer" fixed app>
    <v-list dense>
      <v-list-item href="/">
        <v-list-item-action>
          <v-icon>mdi-view-dashboard</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Dashboard</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-list-group prepend-icon="mdi-file-outline" value="true">
        <template v-slot:activator>
          <v-list-item-title>Resources</v-list-item-title>
        </template>
        <v-list-item class="sublist-item" v-for="(resource, i) in resources" :key="i" link :to="resource.link">
          <v-list-item-action>
            <v-icon v-text="resource.icon"></v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="resource.name"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>

      <v-list-item  href="/team">
        <v-list-item-action>
          <v-icon>mdi-account-multiple</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Team Members</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-list-item href="/calendar">
        <v-list-item-action>
          <v-icon>mdi-calendar</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Calendar</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
       <v-list-item  href="/ideas-board">
        <v-list-item-action>
          <v-icon>mdi-lightbulb-outline</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Ideas Board</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: 'AppDrawer',
  data: () => ({
    resources: [
      {name:'Scrum', icon:'mdi-cube-unfolded', link:'/scrum'},
      {name:'UI/UX', icon:'mdi-cursor-pointer', link:'/ui-ux'}, 
      {name:'AWS', icon:'mdi-amazon', link:'/aws'}, 
      {name:'GCP', icon:'mdi-cloud-outline', link:'/gcp'}, 
      {name:'Environments', icon:'mdi-server', link:'/environments'},
      {name:'ESO Auth', icon:'mdi-login', link:'/eso-auth'},  
      {name:'Security', icon:'mdi-security', link:'/security'},
      {name:'Service Now', icon:'mdi-headset', link:'/service-now'}, 
      {name:'PRs and Git', icon:'mdi-tumblr-reblog', link:'/prs-git'}, 
      {name:'Production Acceptance', icon:'mdi-checkbox-marked-outline', link:'/prod-acceptance'}, 
      {name:'New Joiners Resources', icon:'mdi-account-plus', link:'/new-joiners'}, 
      {name:'Team Website', icon:'mdi-web', link:'/team-website'},
      {name:'Blog', icon:'mdi-blogger', link:'/blog'},  
      {name:'Helpful ACN Links', icon:'mdi-information-outline', link:'/other'}
    ],
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

<style scoped>
 .sublist-item{
    margin-left: 2rem;
  }

</style>