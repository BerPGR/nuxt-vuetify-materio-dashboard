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
                <v-col cols="12" sm="3" class="pb-3" v-for="(item, i) in statistics" :key="i">
                  <div class="d-flex flex-row">
                    <v-sheet rounded elevation="0" width="50" height="50" :color="item.color" class="ml-4 d-flex justify-center">
                      <v-icon large>
                        {{ item.icon }}
                      </v-icon>
                    </v-sheet>
                    <div class="d-flex flex-column ml-3">
                      <p class="mb-0 body-2 grey--text">{{ item.title }}</p>
                      <h2>{{ item.subtitle }}</h2>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-card>
          </v-col>

          <v-col cols="12" sm="4">
            <v-card>
              <v-row align="center" class="ma-0">
                <v-card-title class="font-weight-regular">Weekly Overview</v-card-title>
                <v-spacer></v-spacer>
                <v-btn icon>
                  <v-icon>
                    mdi-dots-vertical
                  </v-icon>
                </v-btn>
              </v-row>
              <v-card-text>
                <v-sparkline class="mt-4" line-width="5" height="120" smooth="10" :value="sparkline" color="#4d0f99" type="bar" auto-draw>
                  <template v-slot:label="item">${{ item.value }}</template>
                </v-sparkline>
                <v-row align="center" class=" mt-7 d-flex align-center">
                  <p class="text-h5 mr-4 ml-4 font-weight-bold">45%</p>
                  <p class="ml-2">Your sales performance in 45% 😛<br /> better compare to last month</p>
                </v-row>
                <v-btn outlined color="deep-purple" width="100%" class="mt-5">details</v-btn>
              </v-card-text>

            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card>
              <v-row align="center" class="ma-0">
                <v-card-title class="font-weight-regular">
                  Total Earning
                </v-card-title>
                <v-spacer></v-spacer>
                <v-btn icon>
                  <v-icon>
                    mdi-dots-vertical
                  </v-icon>
                </v-btn>
              </v-row>
              <v-row class="ma-0" align="center">
                <v-card-title class="text-h4">$24,895</v-card-title>
                <v-icon class="mt-2" color="green" small>
                  mdi-triangle
                </v-icon>
                <p class="green--text mt-6 ml-1">10%</p>
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
  data: () => ({
    statistics: [
      {color: 'deep-purple lighten-1', icon: 'mdi-arrow-top-right', title: 'Sales', subtitle: '245k'},
      {color: 'light-green accent-3', icon: 'mdi-account-outline', title: 'Customers', subtitle: '12.5k'},
      {color: 'amber lighten-1', icon: 'mdi-tag-outline', title: 'Product', subtitle: '1.54k'},
      {color: 'cyan accent-2', icon: 'mdi-currency-usd', title: 'Revenue', subtitle: '$88k'},
    ],
    sparkline: [
      42,
      59,
      51,
      60,
      74,
      33,
      57
    ]
  }),
}
</script>

<style>
.container {
  margin-left: 0;
  max-width: 100%;
}
</style>