<template>
    <div id="appRoot">
    <template>
        <v-app id="inspire">
            <AppToolbar></AppToolbar>
            <AppDrawer ></AppDrawer>
             <v-content>
          <!-- Page Header -->
          <div class="page-wrapper">
            <nuxt/>
          </div>
          <!-- App Footer -->
           <v-footer
            color="indigo"
            app
            >
            <span class="white--text">&copy; Company 2019</span>
            </v-footer>
        </v-content>
        </v-app>
    </template>
    </div>
</template>


<style>
 .page-wrapper{
    min-height: calc(100vh - 64px - 50px - 81px);
    margin-bottom: 50px;
 }
   
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