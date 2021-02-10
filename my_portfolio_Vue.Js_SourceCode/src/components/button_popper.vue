<template>
    <div>
        
  <v-card
    v-click-outside="onClickOutside"
    :color="active ? 'primary' : undefined"
    :dark="active"
    class="mx-auto"
    :height="active ? 256 : 30"
    rounded="xl"
    :width="active ? 256 : 100"
    @click="active = true"
    
  >
  
    <div class="text-h3 text-md-h1 fill-height d-flex align-center justify-center">
      {{ active ? 'Click Outside' : 'Click Me' }}
    </div>
    
  </v-card>

    </div>
</template>

<script>
  export default {
    data: () => ({
      active: false,
    }),

    methods: {
      onClickOutside () {
        this.active = false
      },
    },
  }
</script>

<style scoped>

</style>