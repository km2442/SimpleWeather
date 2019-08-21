<template>
  <div>
    <v-container fluid>
      <v-layout row wrap justify-space-around class="ma-3">
        <v-flex xs12 md6 class="px-2">
          <v-card class="add pa-5">
            <h1>Dodaj miasto</h1>
            <h2>Ładne</h2>
            <h3>Piękne</h3>
          </v-card>
        </v-flex>
        <v-flex xs12 md6 class="px-2">
          <v-card class="add pa-5">
            <h1>Dodaj miasto</h1>
            <h2>Ładne</h2>
            <h3>Piękne</h3>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  components: {
    //widget: () => import(/* webpackChunkName: "Index" */ './Widget')
  }
  // data: () => {
  //     widgets: []
  // }
};
</script>

<style scoped>
.add {
  border: 10px dashed #3a3a3a;
  border-radius: 10px;
}
</style>