<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div>
        <h1>To do List</h1>
      </div>
      <v-spacer></v-spacer>
      <v-btn href="https://vuetifyjs.com/en/components/all/" target="_blank" text>
        <span class="mr-2">Vuetify</span>
        <v-icon>mdi-vuetify</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App"
};
</script>
