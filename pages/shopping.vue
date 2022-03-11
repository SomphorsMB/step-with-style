<template>
  <section>
    <div class="main-shop text-center">
      <h1 class="title white--text text-wrap pt-16">
        Shop your favorite shoes
      </h1>
    </div>
    <v-row class="mt-16 mx-14">
      <v-col cols="3" class="">
        <v-card class="pa-2">
          <v-card-title>Short by</v-card-title>
          <hr />
          <v-combobox
            v-model="select"
            :items="items"
            label="Gender"
            outlined
            hide-details
            dense
            class="mt-3"
          ></v-combobox>
          <v-combobox
            v-model="select"
            :items="items"
            label="Category"
            outlined
            hide-details
            dense
            class="mt-3"
          ></v-combobox>
          <v-card-subtitle class="pl-0 pb-1">Color <hr></v-card-subtitle>
          <v-checkbox
          v-for="color of colors" :key="color"
            :label="color"
            class="py-0"
            hide-details
          ></v-checkbox>
          <v-card-subtitle class="pl-0 pb-1">Arange Price <hr></v-card-subtitle>
          <v-radio-group v-model="radioGroup">
        <v-radio
          v-for="price in prices"
          :key="price"
          :label="price.min + '$ - ' + price.max + '$'"
          :value="price"
        ></v-radio>
      </v-radio-group>
        </v-card>
      </v-col>




      <v-col cols="9" class="">
        <v-card class="pa-2 d-flex">
          <v-tabs
            background-color="transparent"
            color="teal"
            fixed-tabs
            class="tabs"
          >
            <v-tab to="/home">Nike</v-tab>
            <v-tab to="/shopping">Jordan</v-tab>
            <v-tab to="/blog">Addidas</v-tab>
            <v-tab to="/contact">Puma</v-tab>
          </v-tabs>
          <v-spacer></v-spacer>
          <v-card-title class="pa-0">20 products</v-card-title>
          <div class="combobox pl-2">
            <v-combobox
              v-model="select"
              :items="items"
              label="Product sell"
              outlined
              hide-details
              dense
              class=""
            ></v-combobox>
          </div>
        </v-card>

        <v-row class="pt-4">
          <v-col cols="4" v-for="n in 6" :key="n">
            <card />
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </section>
</template>

<script>
import card from '~/components/card.vue';
export default {
  components: { card },
  data() {
    return {
      select: 'All',
      items: ["All", "Most Popular", "Best sell"],
      colors: ['Red', "Green", 'Blue', 'Grey', 'Yellow', 'White', 'Black'],
      select: "",
      prices:[
        {
          min: 5,
          max: 50
        },
        {
          min: 51,
          max: 100
        },
        {
          min: 101,
          max: 200
        },
        {
          min: 201,
          max: 500
        },
        {
          min: 501,
          max: 'Up'
        },
      ]
    };
  },
};
</script>

<style scoped>
.main-shop {
  height: 30vh;
  width: 100%;
  background: teal;
}
.title {
  font-size: 8rem !important;
  font-family: Roboto;
  z-index: 1;
  /* position: absolute;
        top: 8%;
        left: 8%; */
}
.tabs {
  width: 40%;
}
.combobox {
  width: 20%;
}
</style>