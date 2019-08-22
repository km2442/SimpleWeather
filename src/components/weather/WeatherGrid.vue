<template>
  <div>
    <v-container fluid>
      <v-layout row wrap justify-space-around class="ma-3">
        <v-flex xs12 md6 class="pa-2">
          <v-card class="add pa-5" @click.native="add = false" style="cursor: pointer">
            <v-container>
              <v-layout justify-center align-center>
                <v-flex xs2>
                  <v-icon large right class="display-3">mdi-plus</v-icon>
                </v-flex>
                <v-flex xs10>
                  <v-row justify="center" class="display-2">Dodaj miasto</v-row>
                </v-flex>
              </v-layout>
            </v-container>
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
  },
  data: () => {
    return {
      add: true
    }
  }
};
</script>

<style scoped>
.add {
  border: 10px dashed #3a3a3a;
  border-radius: 10px;
}
</style>