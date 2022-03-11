<template>
  <section>
      <div class="main-home">
          <h1 class="title white--text">Find Shoes</h1>
          <v-btn class="btn rounded-0 px-6 font-weight-bold py-6 white--text">Shop Now</v-btn>
          <div class="d-flex justify-end">
              <img src="../static/nike-air-force-1-shadow-photon-dust-malachite-ci0919-004_w900-removebg-preview.png" class="image" width="55%"/>
          </div>
      </div>
    <v-card-text class="text-center mt-12">
        <h1 class="text-h4 font-weight-bold">The Best Brand</h1>
    </v-card-text>
    <v-row class="mx-4 mt-6">
        <v-col cols="3" xs="12" sm="6" md="4" lg="3" xl="3" v-for="brand of brands" :key="brand.title">
            <v-img
              :src="brand.image"
              class="white--text align-center"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title >
                  <h3 class="mx-auto">{{ brand.title }}</h3>
              </v-card-title>
            </v-img>
        </v-col>
    </v-row>

    <v-card-text class="text-center mt-12">
        <h1 class="text-h4 font-weight-bold">Arrivable Product</h1>
    </v-card-text>
    <v-row class="mx-4 mt-6">
        <v-col cols="3" xs="12" sm="6" md="4" lg="3" xl="3"  v-for="brand of 8" :key="brand">
            <card />
        </v-col>
    </v-row>
    <v-card-actions>
            <v-btn class="ma-2 mx-auto rounded-0 py-4 mt-6" width="18%" outlined color="teal">
                View All
            </v-btn>
        </v-card-actions>

    <v-card color="mx-auto mt-12" width="80%" >
        <v-row>
            <v-col cols="3" v-for="item of items" :key="item.title">
                <v-card-text class="text-center ">
                    <v-icon class="teal--text text-h4" >{{ item.icon }}</v-icon>
                    <v-card-title class="text-center">
                        <span class="mx-auto">{{ item.title }}</span>
                    </v-card-title>
                    <v-card-subtitle>{{ item.subTitle }}</v-card-subtitle>


                </v-card-text>
            </v-col>
        </v-row>
    </v-card>
  </section>
</template>

<script>
import card from '~/components/card.vue'
export default {
  components: { card },
    data(){
        return{
            brands:[
                {
                    title: "Nike AIR",
                    image: 'https://cdn.thesolewomens.co.uk/2021/11/nike-air-force-1-shadow-photon-dust-malachite-ci0919-004_w900.jpeg'
                },
                {
                    title: "Jordan",
                    image: 'https://hypescrape.com/wp-content/uploads/2021/03/Wethenew-Sneakers-France-Air-Jordan-1-Mid-Yellow-Toe-1_2000x_63ac01d5-c8c4-479b-9847-c9e3e81c2bbe.png'
                },
                {
                    title: "Addidas",
                    image: 'https://png.pngitem.com/pimgs/s/124-1243527_transparent-adidas-png-adidas-yeezy-boost-350-v2.png'
                },
                {
                    title: "Puma",
                    image: 'https://pbs.twimg.com/media/EYUaRkaUMAATPvA.jpg'
                },
            ],
            items:[
                {
                    title: "Free Shipping",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-truck-outline'
                },
                {
                    title: "Return Policy",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-switch'
                },
                {
                    title: "24/7 Support",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-headset'
                },
                {
                    title: "Seurce Payment",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-database'
                },
            ]
        }
    }
}
</script>

<style scoped>
    .main-home{
        height: 82vh;
        width: 100%;
        background: teal;
    }
    .title{
        font-size: 13rem !important;
        font-family: Roboto;
        z-index: 1;
        position: absolute;
        top: 8%;
        left: 8%;
    }
    .image{
        z-index: 2;
        margin-top: 130px;
    }
    .btn{
        position: absolute;
        top: 18%;
        left: 25%;
        border: 2px solid white;
        background: teal !important;
    }
</style>