<template>
  <v-dialog max-width="600px" app v-model="bool">
    <v-card>
      <v-card-title style="background-color: #3890D8" class="text-h5 white--text lighten-2 center">
        {{ title }}
      </v-card-title>
      <div style="display:flex; align-items: center; justify-content:center;"> 
        <v-img
          class="mt-n2"
          :src="image"
          max-height="350"
          max-width="400"
          contain
        ></v-img>
        <div style="margin: 20px; padding: 1rem">
          <span style="font-size: 1.8rem">{{ price }}</span>
          <v-btn color="black" @click="fakeStore" dark  tile class="withoutupercase">Comprar</v-btn>
        </div>
        
      </div>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  name: 'Dialog',
  props: {
    bool: {
      type: Boolean
    },
    title: {
      type: String
    },
    price: {
      type: String
    },
    image: {
      type: String
    }
  },
  methods: {
    fakeStore() {
      alert("Esta loja é apenas um projeto de estudos, ela não existe! :)");
    },
  }
};
</script>
