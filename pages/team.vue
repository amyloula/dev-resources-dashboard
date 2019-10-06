<template>
  <div id="pageTeam">
    <v-container grid-list-xl fluid>
      <v-layout row wrap>
        <!-- mini statistic start -->
        <v-flex v-for="(member, i) in team" :key="i" lg3 sm6 xs12>
          <v-card max-width="344" class="mx-auto my-8">
            <div class="v-offset" style="top: -24px; margin-bottom: -24px;">
              <div class="v-avatar mx-auto d-block">
                <img src="../static/avatar/naomi.JPG" alt="Naomi Quinn"/>
              </div>
            </div>
           <div class="v-card__text text-center">
             <h6 class="category text-gray font-weight-thin mb-3" v-text="member.role"></h6>
             <h4 class="card-title font-weight-light" v-text="member.name"></h4>
             <p class="card-description font-weight-light">Work work work...</p>
              <v-btn class="ma-2 v-btn--round pa-1" color="purple" dark>
                <v-icon dark>mdi-account</v-icon>
              </v-btn>  
          </div>
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
    color: Material,
    team: [
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'},
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}, 
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}, 
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}, 
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'},
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'},  
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'},
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}, 
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}, 
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}, 
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}, 
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'},
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'},  
      {name:'Naomi Quinn', role:'Software Engineering Senior Manager', motto:'My life motto'}
    ],
  })
}
</script>

<style scoped>
.v-card{
 background-color:white;  
}
.v-avatar{
height: 6rem;
width: 6rem;
box-shadow: 0 10px 30px -12px rgba(0,0,0,.42)
}
.v-offset {
    margin: 0 auto;
    max-width: calc(100% - 32px);
    position: relative;
}
</style>
