<template>
<div>
  <v-app-bar hide-on-scroll color="#002984">
    <v-toolbar-title>
      APP TITLE
    </v-toolbar-title>
      <v-card-actions />
      <v-card-actions>
    <v-btn>Home</v-btn>
      </v-card-actions>

      <v-card-actions>
    <v-btn>Login</v-btn>
      </v-card-actions>
  </v-app-bar>
  <Login />
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
    showPassword:false,
  }),
};
</script>
