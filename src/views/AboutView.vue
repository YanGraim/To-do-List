<template>
  <v-container style="max-width: 500px; border: 1px solid black;">
    <v-col>
      <v-rol class="d-flex flex-column justify-center align-center" style="margin: 2rem">
        <h1>To do List</h1>
        <h3>Lista do Claudio Jr 🎉</h3>
      </v-rol>
      <v-row class="d-flex justify-center align-end">
        <v-col cols="8" style="display: flex; align-items: center; justify-content: center;">
          <v-text-field density="compact" variant="outlined" label="Algo para fazer" append-inner-icon="mdi-magnify"
            single-line hide-details clearable v-model="coisa"></v-text-field>
        </v-col>
        <v-col cols="1" class="d-flex flex-column justify-end align-center" style="margin-left: 1rem;" v-model="coisa">
          <v-btn :disabled="habilitaBtn" color="success" @click="addCoisa"> <v-icon>mdi-thumb-up</v-icon> </v-btn>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <div v-for="item in coisas" disabled class="d-flex">
            {{ item.message }}
          </div>
        </v-col>

      </v-row>
    </v-col>
  </v-container>
</template>

<script>
export default {
  name: "AboutView",

  data: () => ({
    coisa: null,
    coisas: []
  }),
  computed:{
    corItem(status){
      if(status){
        return 'success'
      } else {
        return 'error'
      }
    },
    habilitaBtn(){
      if(this.coisa){
        return false
      } else {
        return true
      }
    }
  },
  methods: {
    addCoisa() {
      if (this.coisa != null) {
        this.coisas.push({ status: false, message: this.coisa })
      }
    }
  }
};
</script>
