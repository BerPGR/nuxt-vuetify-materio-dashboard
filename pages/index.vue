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
                  <v-card-subtitle class="pt-1 grey--text">
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
          <v-col cols="12" sm="8">
            <v-card>
              <v-row align="center">
                <v-col cols="12" sm="11">
                  <v-card-title class="pb-3 pt-0">Statistics Card</v-card-title>
                  <v-card-subtitle><strong>Total 48.5% Growth</strong> 😎 this month</v-card-subtitle>
                  <v-spacer></v-spacer>
                </v-col>
                <v-btn icon class="mb-10 ml-4">
                    <v-icon>
                      mdi-dots-vertical
                    </v-icon>
                  </v-btn>
              </v-row>

              
            </v-card>
          </v-col>
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