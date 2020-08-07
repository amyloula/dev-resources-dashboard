<template>
  <div id="pageDashboard">
    <v-container grid-list-xl fluid>
      <v-layout row wrap>
        <!-- mini statistic start -->
        <v-flex lg3 sm6 xs12>
          <v-card max-width="344" class="mx-auto">
            <v-card-title>I'm a title</v-card-title>
            <v-card-text>I'm card text</v-card-text>
            <v-card-actions>
              <v-btn text>Click</v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
        <v-flex lg3 sm6 xs12>
          <v-card max-width="344" class="mx-auto">
            <v-card-title>I'm a title</v-card-title>
            <v-card-text>I'm card text</v-card-text>
            <v-card-actions>
              <v-btn text>Click</v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
        <v-flex lg3 sm6 xs12>
          <v-card max-width="344" class="mx-auto">
            <v-card-title>I'm a title</v-card-title>
            <v-card-text>I'm card text</v-card-text>
            <v-card-actions>
              <v-btn text>Click</v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
        <v-flex lg3 sm6 xs12>
          <v-card max-width="344" class="mx-auto">
            <v-card-title>I'm a title</v-card-title>
            <v-card-text>I'm card text</v-card-text>
            <v-card-actions>
              <v-btn text>Click</v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import Material from 'vuetify/es5/util/colors'

export default {
  layout: 'general',
  data: () => ({
    color: Material
  })
}
</script>
