<template>
<div>
  <v-card class="overflow-hidden">
  <v-app-bar 
      color="#002984"
      inverted-scroll
      collapse-on-scroll
      elevate-on-scroll
      absolute
      extension-height
      dark
      bottom
  >
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
    <v-toolbar-title>
      APP TITLE
    </v-toolbar-title>
      <!-- <v-card-actions />
      <v-card-actions>
    <v-btn rounded>Home</v-btn>
      </v-card-actions>

      <v-card-actions>
    <v-btn rounded>Login</v-btn>
      </v-card-actions> -->
      <v-spacer />
      <v-checkbox
        v-model="collapseOnScroll"
        color="white"
        hide-details
      ></v-checkbox>
  </v-app-bar>
  </v-card>
  
  <Login />
  <div style="height:50vh;background:blue;">sd</div>
</div>
</template>

<script>
import Login from './components/Login';

export default {
  name: 'App',

  components: {
    Login,
  },

  data: () => ({
    // collapseOnScroll: true,
    
  }),
};
</script>
