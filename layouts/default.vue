<template>
  <v-app dark>
    <v-navigation-drawer
    color="transparent"
      true
      fixed
      floating
      app
    >
      <v-toolbar color="transparent" elevation="0">
        <v-img :src="require('../assets/help/logo.png')" contain height="20" width="0"></v-img>
        <v-toolbar-title class="font-weight-bold">MATERIO</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-icon small>
          mdi-circle-double
        </v-icon>
      </v-toolbar>

      <v-expansion-panels flat class="transparent">
      <v-expansion-panel>
        <v-expansion-panel-header class="pl-0">
          <v-icon class="mr-4">mdi-home</v-icon>
          <p class="mb-0 mr-6">Dashboards</p>
        </v-expansion-panel-header>
        <v-expansion-panel-content>
          <v-list>
            <v-list-item-group>
              <v-list-item v-for="(item, i) in dashboards" :key="i">
                <v-list-item-icon>
                  <v-icon small>mdi-circle-outline</v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>

      <v-list nav dense>
        <v-list-item-group>
          <v-list-item v-for="(item, i) in apps" :key="i" link>
            <v-list-item-icon>
              <v-icon>
                {{ item.icon }}
              </v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

        </v-list-item-group>

      </v-list>
    </v-navigation-drawer>

    <v-app-bar color="transparent" flat app>
      <v-row>
        <v-col cols="12" sm="7">
          <v-text-field color="purple" filled rounded outlined dense prepend-inner-icon="mdi-magnify" class="mt-7"></v-text-field>
        </v-col>
      </v-row>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>
          mdi-github
        </v-icon>
      </v-btn>
      <v-btn icon @click="$vuetify.theme.dark = !$vuetify.theme.dark">
        <v-icon>
          mdi-weather-night
        </v-icon>
      </v-btn>
      <v-btn icon class="mr-2">
        <v-icon>
          mdi-bell-outline
        </v-icon>
      </v-btn>
      <v-badge dot overlap bottom color="green">
        <v-avatar size="40">
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
      apps: [
        { icon: 'mdi-calendar', title: "Calendar" },
        { icon: 'mdi-message-text', title: "Chat" },
        { icon: 'mdi-email', title: "Email" },
        { icon: 'mdi-receipt', title: "Invoice" },
        { icon: 'mdi-account', title: "User" },
        { icon: 'mdi-file', title: "Pages" },
      ],

      dashboards: [
        { title: "CRM"},
        { title: "Analytics"},
        { title: "eCommerce"},
      ]
    }
  },
}
</script>

<style>
.v-list-item--active {
  background: rgb(77,8,156);
background: linear-gradient(257deg, rgba(77,8,156,1) 0%, rgba(176,109,177,1) 100%);
}

.v-list--nav .v-list-item, .v-list--nav .v-list-item:before, 
.v-list-item-group .v-list-item--active {
  border-radius: 5px 40px 40px 5px;
  background-color: transparent;
}
</style>
