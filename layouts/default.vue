<template>
  <v-app style="background-color: #F8F8F8;" dark>
    <v-navigation-drawer
      true
      fixed
      app
    >
    </v-navigation-drawer>
    <v-app-bar color="transparent" flat app>
      <v-row>
        <v-col cols="12" sm="7">
          <v-text-field filled rounded outlined dense prepend-inner-icon="mdi-magnify" class="mt-7"></v-text-field>
        </v-col>
      </v-row>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>
          mdi-github
        </v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>
          mdi-weather-night
        </v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>
          mdi-bell-outline
        </v-icon>
      </v-btn>
      <v-badge overlap bottom color="green">
        <v-avatar size="50">
        <v-img :src="require('../assets/help/eu.png')"></v-img>
      </v-avatar>
      </v-badge>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
    }
  },
}
</script>
