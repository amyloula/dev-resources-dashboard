<template>
  <v-app id="inspire">
    <AppToolbar></AppToolbar>
    <AppDrawer ></AppDrawer>
    <nuxt />
    <v-footer
      color="indigo"
      app
    >
      <span class="white--text">&copy; Company 2019</span>
    </v-footer>
  </v-app>
</template>

<style>

</style>

<script>
  import AppDrawer from '@/components/AppDrawer'
  import AppToolbar from '@/components/AppToolbar'

  export default {
    components: {
      AppDrawer,
      AppToolbar
    },
    data: () => ({
      expanded: true,
      rightDrawer: false,
      snackbar: {
        show: false,
        text: '',
        color: '',
      }
    }),
    methods: {
      openThemeSettings() {
        this.$vuetify.goTo(0)
        this.rightDrawer = (!this.rightDrawer)
      }
    }
  }
</script>