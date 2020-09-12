<template>
  <v-app style="background-image: linear-gradient(-45deg, #002984 50%, #f76e2a 0%);">
    <v-card width="400" class="mx-auto my-auto" style="margin-top:0">
      <v-card-title>
      <h1 class="display-1">LOGIN</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field
          label="USERNAME"
          prepend-icon="mdi-account-circle"
          />
          <v-text-field 
          :type="showPassword ? 'text':'password'" 
          label="PASSWORD" 
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye':'mdi-eye-off'"
          @click:append="showPassword = !showPassword"
          />
        </v-form>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
      <v-btn color="success">Register</v-btn>
      <v-spacer />
      <v-btn color="info">Login</v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    // HelloWorld,
  },

  data: () => ({
    showPassword:false,
  }),
};
</script>
