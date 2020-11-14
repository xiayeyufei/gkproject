<template>

  <v-app>

    <router-view></router-view>
  </v-app>
</template>

<script>
import xx from './views/index.vue';

export default {
  name: 'App',

  components: {
    xx,
  },

  data: () => ({
    //
  }),
};
</script>
