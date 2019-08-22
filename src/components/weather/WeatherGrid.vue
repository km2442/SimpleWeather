<template>
  <div>
    <v-container fluid>
      <v-layout row wrap justify-space-around class="ma-3">
        <v-flex xs12 md6 class="pa-2">
          <v-hover v-slot:default="{ hover }">
            <v-card
              @click.native="add = false"
              style="cursor: pointer"
              class="add pa-5"
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