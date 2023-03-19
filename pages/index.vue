<template>
  <v-container>

    <v-row>
      <v-col cols="12">
        <v-row>
          <v-col cols="12" sm="4">
            <v-card>
              <v-row>
                <v-col cols="12" sm="9">
                  <v-card-title class="pb-3 pt-0 pl-4">
                    Congratulations, Bernardo!
                  </v-card-title>
                  <v-card-subtitle class="pt-1">
                    You have won a trophy!
                  </v-card-subtitle>

                  <v-card-title class="font-weight-bold h6 purple--text pb-2 pt-0">
                    $42.8k
                  </v-card-title>
                  <v-btn class="ml-4 white--text" color="purple darken-3">
                    View Sales
                  </v-btn>
                </v-col>
                <v-col cols="12" sm="3" class="d-flex align-center pl-0 pr-5">
                  <v-img :src="require('../assets/help/trophy.png')" contain></v-img>
                </v-col>
              </v-row>
            </v-card>

          </v-col>
          <v-col cols="12" sm="8"><v-card>
            <p>
              Card 2
            </p>
          </v-card></v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style>
.container {
  margin-left: 0;
  max-width: 100%;
}
</style>