<template>
  <v-app class="grey lighten-4">
    <navbar />
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
  import navbar from './components/navbar'
export default {
  name: 'App',
  components: { navbar },
  data: () => ({
    //
  }),
};
</script>
