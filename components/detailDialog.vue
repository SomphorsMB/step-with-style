<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" max-width="80%" height="80vh" class="dialog">
      <v-card>
        <v-card-title class="pr-0 pt-0 pb-0">
          <v-spacer></v-spacer>
          <v-avatar>
            <v-btn text class="rounded-circle py-4" @click="$emit('close')">
              <v-icon> mdi-close </v-icon>
            </v-btn>
          </v-avatar>
        </v-card-title>
        <v-card-text>
          <v-container class="pt-0 mt-0">
            <v-row>
              <v-col cols="5" xl="6" lg="6" md="6" sm="12" xs="12" class="pa-0">
                <v-card-text class="black white--text pa-1 cardDiscount"
                  >23%</v-card-text
                >
                <v-img
                  src="https://static.nike.com/a/images/t_PDP_1280_v1/f_auto,q_auto:eco/c56e3f1b-3f3d-4800-ae60-8964e08938e1/air-force-1-shadow-shoes-8q0vxX.png"
                  height="52vh"
                ></v-img>
              <!-- </v-col> -->
              <!-- <v-col cols="7" xl="6" lg="6" md="6" sm="12" xs="12" class=""> -->
                <v-row class="mb-2">
                  <v-col cols="4" xs="12" sm="6" md="4" lg="4" xl="4" class="pt-0">
                    <v-img
                      src="https://storage.googleapis.com/sportshowroom.sg/products/ec91840faf3ff74ae5a0d1a4942656d6.jpg"
                      class="white--text align-center"
                      height="150px"
                       :style="isClick ? 'border: 1px solid black;' : 'border: 1px solid white;'"
                    >
                    </v-img>
                  </v-col>
                  <v-col cols="4" xs="12" sm="6" md="4" lg="4" xl="4" class="pt-0">
                    <v-img
                      src="https://postuzapas.com/1232/nike-air-force-1-shadow-beige-reflect.jpg"
                      class="white--text align-center"
                      height="150px"
                    >
                    </v-img>
                  </v-col>
                  <v-col cols="4" xs="12" sm="6" md="4" lg="4" xl="4" class="pt-0">
                    <v-img
                      src="https://zapasgo.com/wp-content/uploads/2021/05/Diseno-sin-titulo-1-17.png"
                      class="white--text align-center"
                      height="150px"
                    >
                    </v-img>
                  </v-col>
                </v-row>
                </v-col>
              <v-col cols="7" xl="6" lg="6" md="6" sm="12" xs="12" class="pl-6">
                <h1 class="black--text text-uppercase">n fnjnjrnej</h1>
                <v-card-text class="d-flex px-0">
                  <span class="green--text font-weight-bold">
                    <v-icon class="green--text">mdi-check-circle</v-icon>
                    In Stock
                  </span>
                  <span class="red--text font-weight-bold">
                    <v-icon class="red--text">mdi-close-circle</v-icon>
                    Out Stock
                  </span>
                </v-card-text>
                <v-card-text class="pa-0 text-h7">
                  <span class="black--text font-weight-bold">Type: </span>
                  <span class="grey--text">nwkenfk</span>
                </v-card-text>
                <v-card-text class="pa-0 text-h7">
                  <span class="black--text font-weight-bold">Size: </span>
                  <span class="grey--text">mndkffnwn</span>
                </v-card-text>
                <v-card-text class="pa-0 text-h7">
                  <span class="black--text font-weight-bold">Total Unit: </span>
                  <span class="grey--text">12</span>
                </v-card-text>

                <v-card-text class="px-0 d-flex">
                  <!-- <v-card-title class="pa-0 text-h4 font-weight-bold black--text orange--text" v-if="product.discount_discount !== null">${{ product.productDetail_price-product.productDetail_price*product.discount_discount/100 }}</v-card-title> -->
                  <!-- <v-card-title class="pa-0 text-h4 font-weight-bold black--text orange--text" v-if="product.discount_discount === null">${{ product.productDetail_price }}</v-card-title> -->
                  <v-card-title
                    class="
                      py-0
                      text-h4
                      font-weight-bold
                      black--text
                      text-decoration-line-through
                      orange--text
                    "
                    >$ 23</v-card-title
                  >
                </v-card-text>
                <v-card-text class="pa-0">
                  <span class="font-weight-bold black--text">QTY</span>
                  <div class="minusplusnumber">
                    <div class="mpbtn minus text-h6 px-3" v-on:click="minus()">
                      -
                    </div>
                    <div id="field_container">
                      <input
                        type="text"
                        v-model="newValue"
                        class="text-center"
                      />
                    </div>
                    <div class="mpbtn plus text-h6" v-on:click="plus()">+</div>
                  </div>
                </v-card-text>
                <v-card-text class="px-0 d-flex justify-space-between">
                  <v-btn width="49%" class="rounded-0" dark>
                      <v-icon class="mr-2">mdi-heart-outline</v-icon>
                      Add to Favorite
                    </v-btn>
                  <v-btn width="49%" class="rounded-0" dark>
                      <v-icon class="mr-2">mdi-cart-outline</v-icon>
                      Add to Cart
                    t</v-btn>
                  <!-- <v-btn width="49%">Add to cart</v-btn> -->
                </v-card-text>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      min: 1,
      newValue: 1,
      dialog: true,
      isClick: true,
            array:[
          'https://static.nike.com/a/images/t_default/1af277c6-00f8-4259-bbb8-50e2639d46a5/air-force-1-shadow-womens-shoes-kTgn9J.png',
          'https://bitsneakers.es/storage/images/image?remote=https://bitsneakers.es/WebRoot/Store24/Shops/6348acfb-5c89-40db-b383-64a5a277d0eb/5EBE/C18B/5313/298A/6F40/0A48/3541/D2D2/14032342-1-washedcoral.jpeg&shop=6348acfb-5c89-40db-b383-64a5a277d0eb&width=600',
          'https://zapasgo.com/wp-content/uploads/2021/05/Diseno-sin-titulo-1-17.png',
          'https://postuzapas.com/1232/nike-air-force-1-shadow-beige-reflect.jpg',
          'https://storage.googleapis.com/sportshowroom.sg/products/ec91840faf3ff74ae5a0d1a4942656d6.jpg'
      ]
    };
  },
};
</script>

<style scoped>
.dialog {
  border: 0.5px solid gray;
}
.minusplusnumber {
  border: 1px solid silver;
  border-radius: 5px;
  background-color: #fff;
  margin: 0 5px 0 5px;
  display: inline-block;
  user-select: none;
}
.minusplusnumber div {
  display: inline-block;
}
.minusplusnumber #field_container input {
  width: 50px;
  text-align: center;
  font-size: 15px;
  padding: 3px;
  border: none;
}
.minusplusnumber .mpbtn {
  padding: 3px 10px 3px 10px;
  cursor: pointer;
  border-radius: 5px;
}
.minusplusnumber .mpbtn:hover {
  background-color: #ddd;
}
.minusplusnumber .mpbtn:active {
  background-color: #c5c5c5;
}
.company-info {
  width: 50%;
}
.cardDiscount {
  width: 80px;
  position: absolute;
  top: 50px;
  left: 25px;
  z-index: 2;
  text-align: center;
}
</style>