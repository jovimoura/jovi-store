<template>
  <v-footer dark padless>
    <v-card flat tile class="black white--text py-12 px-5" width="100%">
      <v-row>
        <v-col cols="12" sm="4">
          <v-card-text class="white--text pt-0">
            <h3>Jovi Store</h3>
          </v-card-text>
          <v-card-text class="grey--text pt-0">
            Projeto desenvolvido para aprendizado de funções básicas do Vue.js + Vuetify.
            Project developed to learn basic functions of Vue.js + Vuetify.
          </v-card-text>
          <v-toolbar flat color="transparent">
            <h5>Guides</h5>
            <h5 class="ml-4">Terms of Use</h5>
            <h5 class="ml-4">Privacy Policy</h5>
          </v-toolbar>
          <v-card-text class="grey--text">
            &#169; 2022
          </v-card-text>
        </v-col>
        <v-col cols="12" sm="2">
          <v-card-text class="white--text pt-0">
            <h3>Get Help</h3>
          </v-card-text>
          <v-card-text class="grey--text">
            Order Status
          </v-card-text>
          <v-card-text class="grey--text mt-n4">
            Shipping and Delivery
          </v-card-text>
          <v-card-text class="grey--text">
            Payment Options
          </v-card-text>
          <v-card-text class="grey--text">
            Contact US
          </v-card-text>
        </v-col>
        <v-col cols="12" sm="2">
          <v-card-text class="white--text pt-0">
            <h3>About US</h3>
          </v-card-text>
          <v-card-text class="grey--text">
            Careers
          </v-card-text>
          <v-card-text class="grey--text mt-n4">
            Sustentability
          </v-card-text>
          <v-card-text class="grey--text">
            Service
          </v-card-text>
          <v-card-text class="grey--text">
            CA Supply Chains Act
          </v-card-text>
        </v-col>
        <v-col cols="12" sm="4">
          <v-card-text class="pt-0">
            <v-btn class="mx-1 white--text" icon v-for="icon in icons" :key="icon">
              <v-icon size="24px">{{ icon }}</v-icon>
            </v-btn>
          </v-card-text>
          <v-card-text class="grey--text mt-14">
            Payment Methods:
          </v-card-text>
          <v-toolbar flat color="transparent">
            <v-spacer></v-spacer>
            <v-icon large>fab fa-cc-visa</v-icon>
            <v-icon class="mx-2" large>fab fa-cc-paypal</v-icon>
          </v-toolbar>
        </v-col>
      </v-row>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    icons: [
      'mdi-instagram',
      'mdi-gmail',
      'mdi-linkedin',
      'mdi-github'
    ]
  })
}
</script>

<style>
  
</style>