<template>
  <div>
    <div class="mx-3 mt-3 mb-0">
      <v-progress-linear
      :value="how * 10"
      color="light-green darken-4"
      height="25"
      striped
      rounded
      dark
    >
      <template v-slot="{ value }">
        <strong>Ilość miast: {{ how }}/10</strong>
      </template>
    </v-progress-linear>
    </div>
    <v-container fluid>
      <transition-group
        enter-active-class="animated zoomIn"
        leave-active-class="animated zoomOut"
        tag="v-layout"
        class="ma-3 row wrap justify-space-around"
      >
        <template v-for="(i, index) in how">
          <v-flex xs12 md6 :key="indexes[index]" class="pa-2">
            <widget></widget>
          </v-flex>
        </template>

        <v-flex xs12 md6 class="pa-2" key="addTown" v-if="how < 10">
          <v-hover v-slot:default="{ hover }">
            <v-card
              @click.native="how++"
              style="cursor: pointer"
              class="add pa-2"
              :class="{'animated pulse infinite slow': hover}"
            >
              <v-container>
                <v-layout justify-center align-center>
                  <v-flex xs2 class="d-none d-sm-block">
                    <v-icon large class="display-3">mdi-playlist-plus</v-icon>
                  </v-flex>
                  <v-flex xd12 sm10>
                    <v-row justify="center" class="display-2 font-weight-bold">Dodaj miasto</v-row>
                  </v-flex>
                </v-layout>
              </v-container>
            </v-card>
          </v-hover>
        </v-flex>
      </transition-group>
    </v-container>
  </div>
</template>

<script>
export default {
  components: {
    widget: () => import(/* webpackChunkName: "Index" */ "./Widget")
  },
  data: () => {
    return {
      add: true,
      how: 0,
      indexes: ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j"]
    };
  }
};
</script>

<style scoped>
.add {
  border: 10px dashed #3a3a3a;
  border-radius: 10px;
}
</style>