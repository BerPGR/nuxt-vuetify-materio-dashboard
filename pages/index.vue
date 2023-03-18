<template>
  <v-container>

    <v-row>
      <v-col cols="12">
      <v-row>
        <v-col cols="12" sm="4">
          <v-card>
            <p>
              Card 1
            </p>
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