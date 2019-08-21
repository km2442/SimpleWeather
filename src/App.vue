<template>
  <v-app>
    <Navbar></Navbar>
    <router-view></router-view>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  components: {
    Navbar: () => import(/* webpackChunkName: "Index" */ './components/Navigation/Navbar')
  },
  data: () => ({
    
  }),
};
</script>
