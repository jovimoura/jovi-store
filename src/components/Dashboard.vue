<template>
  <div>
    <!-- <navbar /> -->
    <v-container fluid>
    <v-card
      color="#3853D8"
      height="150px"
      tile
      flat
      class="d-flex align-center justify-center"
      dark
    >
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center">Modelos Masculinos</h4>
        </v-col>
        <v-col cols="12" sm="12">
          <v-breadcrumbs :items="items" class="justify-center mt-n7" dark>
            <template v-slot:divider>
              <v-icon color="#7C92FE">mdi-chevron-right</v-icon>
            </template>
          </v-breadcrumbs>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="mx-16 mt-n10 card1" color="white" tile>
      <v-row>
        <v-col cols="12" sm="8" class="pr-0">
          <v-card height="250px" tile flat color="#3890D8">
            <v-row>
              <v-col cols="12" sm="4" class="pl-8 pt-5">
                <v-btn class="withoutupercase" color="black" dark small tile>
                  novo
                </v-btn>
                <h6 class="white--text mt-8">Aluminium Rider</h6>
                <h3 class="white--text mt-5">Bike voltada para Montanhas</h3>
                <v-btn
                  rounded
                  color="#4C9CDB"
                  class="withoutupercase px-8 mt-3 white--text"
                >
                  Mais Informações
                </v-btn>
              </v-col>
              <v-col cols="12" sm="8">
                <v-img
                  class="mt-n6"
                  src="bike.png"
                  alt="imagem1"
                  max-height="400"
                  max-width="400"
                  contain
                ></v-img>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col class="pl-0" cols="12" sm="4">
          <v-card height="250px" tile flat color="#6857E1">
            <v-row>
              <v-col class="pl-8 pt-5" cols="12" sm="6">
                <v-btn color="black" dark small tile class="withoutupercase">
                  novo
                </v-btn>
                <h6 class="white--text mt-8">Jaqueta Moletom</h6>
                <h3 class="white--text mt-5">Coleção de 2022</h3>
                <v-btn
                  rounded
                  color="#6857E1"
                  class="withoutupercase px-8 mt-3 white--text"
                >
                  Mais Informações
                </v-btn>
              </v-col>
              <v-col cols="12" sm="6">
                <v-img
                  class="mt-n2"
                  src="jacket2.png"
                  max-height="400"
                  max-width="420"
                  contain
                ></v-img>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" sm="3" class="mt-n6 pr-0">
          <v-toolbar flat outlined>
            <v-toolbar-title><strong>Filtro</strong></v-toolbar-title>
            <v-spacer></v-spacer>
            <v-divider vertical></v-divider>
            <v-btn class="ml-1" icon>
              <v-icon color="#3853D8">mdi-sync</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined>
            <v-toolbar-title>
              Ordenar por: <span>Mais procurados</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="#000">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined>
            <v-toolbar-title>Exibir: <span>12</span></v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn class="mr-4" icon>
              <v-icon color="#000">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 pl-0">
          <v-toolbar flat outlined>
            <v-btn class="mr-1" icon>
              <v-icon color="#3853D8">mdi-apps</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-btn icon class="mx-1">
              <v-icon color="grey">mdi-format-list-bulleted</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-toolbar-title class="ml-2">
              <strong>Compare: </strong>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-badge class="mr-2" color="#3853D8" content="3"></v-badge>
          </v-toolbar>
        </v-col>
        <v-col class="py-0 pr-0 mt-n3" cols="3">
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon class="mr-2" color="#000">mdi-chevron-down</v-icon>
              <strong>Categorias</strong>
              <v-spacer></v-spacer>
              <v-icon small color="grey">mdi-close</v-icon>
            </v-toolbar>
            <v-list class="mt-n5" dense>
              <v-list-item v-for="(style, i) in styles" :key="i">
                <v-list-item-content class="ml-8" v-text="style.title">
                  <v-list-item-title
                    v-text="style.title"
                    class="ml-8"
                  ></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-list-item-subtitle
                    v-text="style.count"
                  ></v-list-item-subtitle>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon class="mr-2" color="#000"> msi-chevron-down </v-icon>
              <strong>PREÇO</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-toolbar flat>
              <v-text-field
                placeholder="$50"
                filled
                rounded
                dense
                class="mx-2"
              ></v-text-field>
              <v-text-field
                placeholder="$1900"
                filled
                rounded
                dense
                class="mx-2"
              ></v-text-field>
            </v-toolbar>
            <v-range-slider color="blue" max="40" min="-30"></v-range-slider>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon class="mr-2" color="#000">mdi-chevron-down</v-icon>
              <strong>Filtre</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-list dense class="mt-n5">
              <v-list-item v-for="brand in brands" :key="brand.title">
                <v-list-item-content>
                  <v-list-item-title
                    v-text="brand.title"
                    class="ml-6"
                  ></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-checkbox
                    color="primary"
                    v-model="brand.state"
                  ></v-checkbox>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card>
            <v-toolbar flat>
              <v-icon class="mr-2" color="#000">mdi-chevron-down</v-icon>
              <strong>Cores</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group multiple column>
              <v-chip
                class="ml-2"
                filter
                outlined
                color="#000"
                text-color="#000"
              ></v-chip>
              <v-chip filter color="#E6E6E6" text-color="#000"></v-chip>
              <v-chip filter color="#FFB500" text-color="#FFF"></v-chip>
              <v-chip filter color="#F27229" text-color="#FFF"></v-chip>
              <v-chip filter color="#EB3427" text-color="#FFF"></v-chip>
              <v-chip
                filter
                color="#923FA3"
                class="ml-2"
                text-color="#FFF"
              ></v-chip>
              <v-chip filter color="#3A51DF" text-color="#FFF"></v-chip>
              <v-chip filter color="#23A7F5" text-color="#FFF"></v-chip>
              <v-chip filter color="#5EB524" text-color="#FFF"></v-chip>
              <v-chip filter color="#7C5F4D" text-color="#FFF"></v-chip>
              <v-chip
                filter
                color="#000"
                class="ml-2"
                text-color="#FFF"
              ></v-chip>
              <v-chip filter color="lime" text-color="#FFF"></v-chip>
            </v-chip-group>
          </v-card>
          <v-card flat outlined>
            <v-toolbar flat>
              <v-icon class="mr-2" color="#000">mdi-chevron-down</v-icon>
              <strong>Tamanho</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group
              column
              multiple
              active-class="blue white--text"
              class="ml-2"
            >
              <v-chip
                class="size"
                v-for="size in sizes"
                :key="size"
                :value="size"
              >
                {{ size }}
              </v-chip>
            </v-chip-group>
          </v-card>
        </v-col>
        <v-col class="mt-n3" cols="9">
          <v-row>
            <v-col
              cols="12"
              sm="4"
              v-for="(clothe, i) in clothes"
              :key="i"
              :class="clothes.class"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card height="300" align="center" flat outlined tile>
                  <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="black" small dark>{{ clothe.sold }}</v-btn>
                  </v-card-actions>
                  <v-img
                    :src="clothe.image"
                    width="200"
                    height="200"
                    contain
                  ></v-img>
                  <v-card-text class="mt-n4">
                    <strong :class="hover ? 'red--text' : 'black--text'">{{
                      clothe.title
                    }}</strong>
                  </v-card-text>
                  <v-expand-transition>
                    <div
                      class="d-flex transition-fast-in-fast-out blue v-card--reveal display-3 white--text"
                      v-if="hover"
                      style="height: 100%; width: 100%"
                    >
                      <v-btn rounded color="white">
                        <v-icon>mdi-cart-outlined</v-icon>
                        Buy
                      </v-btn>
                      <v-btn class="ml-2" fab small color="white">
                        <v-icon color="#000">mdi-content-copy</v-icon>
                      </v-btn>
                      <v-btn class="ml-2" fab small color="white">
                        <v-icon color="black">mdi-heart-outline</v-icon>
                      </v-btn>
                    </div>
                  </v-expand-transition>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined> </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 px-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="grey">mdi-chevron-up</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 px-0 pb-0">
          <v-toolbar class="text-center" flat outlined>
            <v-pagination v-model="page" :length="4"></v-pagination>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pl-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="grey">mdi-chevron-down</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col>
      </v-row>
    </v-card>
    <v-card
      class="d-flex align-center justify-center mt-n10 card2"
      color="#EFF0F2"
      height="250px"
      tile
      flat
      dark
    >
      <v-row>
        <v-col cols="12" sm="12">
          <h6 class="text-center grey--text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </h6>
        </v-col>
        <v-col cols="12" sm="12">
          <v-card flat color="transparent" class="d-flex justify-center">
            <v-text-field
              placeholder="Digite seu E-mail"
              rounded
              class="shrink"
              background-color="grey"
              filled
              append-icon="mdi-email-outlined"
              dense
            ></v-text-field>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
  </div>
  
  
</template>

<script>
import Navbar from './Navbar.vue';
export default {
  components: { Navbar },
  data: () => ({
    page: 1,
    items: [
      {
        text: "Início",
        disabled: false,
        href: "breadcrumbs_home",
      },
      {
        text: "Catalogo",
        disabled: false,
        href: "breadcrumbs_catalog",
      },
      {
        text: "Masculino",
        disabled: false,
        href: "breadcrumbs_men",
      },
      {
        text: "Tênis",
        disabled: false,
        href: "breadcrumbs_shoes",
      },
    ],
    styles: [
      {
        title: "Lifestyle",
        count: "1",
      },
      {
        title: "Corrida",
        count: "23",
      },
      {
        title: "Treino e Academia",
        count: "45",
      },
      {
        title: "Basquete",
        count: "11",
      },
      {
        title: "Volei",
        count: "15",
      },
      {
        title: "Futebol",
        count: "32",
      },
      {
        title: "Basebol",
        count: "8",
      },
      {
        title: "Golf",
        count: "15",
      },
      {
        title: "Skatismo",
        count: "22",
      },
    ],
    brands: [
      {
        title: "Lifestyle",
        state: true,
      },
      {
        title: "Corrida",
        state: true,
      },
      {
        title: "Treino e Academia",
        state: true,
      },
      {
        title: "Basquete",
        state: true,
      },
    ],
    sizes: [
      "35",
      "36",
      "37",
      "38",
      "39",
      "40",
      "41",
      "42",
      "43",
      "44",
      "45",
      "46",
    ],
    clothes: [
      {
        class: "pa-0",
        sold: "-20%",
        image: "1.png",
        title: "KD 8 EXT",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-30%",
        image: "2.png",
        title: "Jordan Galaxy",
        price: "$ 599.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-17%",
        image: "3.png",
        title: "Nike SB Trainerendor Leathe",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-22%",
        image: "4.png",
        title: "Air Jordan Spike 40 iD",
        price: "$ 220.00",
      },
      {
        class: "pa-0",
        sold: "-18%",
        image: "5.png",
        title: "Nike Air Footscape Magista Flynknit",
        price: "$ 235.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-40%",
        image: "6.png",
        title: "Nike Air Zoom Huarache 2k4",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-13%",
        image: "7.png",
        title: "Jordan Horizon",
        price: "$ 230.00",
      },
      {
        class: "pa-0",
        sold: "-15%",
        image: "8.png",
        title: "Air Jordan xx9 Low",
        price: "$ 185.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-10%",
        image: "9.png",
        title: "LeBron XIII Premium AS iD",
        price: "$ 265.00",
      },
      {
        class: "pa-0",
        sold: "-19%",
        image: "10.png",
        title: "Air Jordan 1 Retro Hight Nouveau",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "11.png",
        title: "Nike Air Presto",
        price: "$ 175.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-10%",
        image: "12.png",
        title: "KD 8 Premium AS iD",
        price: "$ 245.00",
      },
    ],
  }),
};
</script>

<style>
.container {
  padding: 0px !important;
}

.v-btn.withoutupercase {
  text-decoration: none;
}

.v-chip.v-size--default {
  border-radius: 50px !important;
  font-size: 14px !important;
  height: 40px !important;
  width: 40px !important;
}

.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  widows: 100%;
}

.card1 {
  z-index: 10;
}

.card2 {
  z-index: 1;
}
</style>
