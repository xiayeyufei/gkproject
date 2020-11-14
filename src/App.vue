<template>

  <v-app>

    <router-view/>
  </v-app>
</template>

<script>
import HelloWorld from './views/index.vue';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
