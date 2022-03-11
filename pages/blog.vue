<template>
  <section>
      <div class="main-about text-center">
      <h1 class="title white--text text-wrap pt-16">
        Contact Us
      </h1>
    </div>
    <v-container>
      <v-card-text class="text-center">
      <v-card-subtitle class="pb-0">ABOUT.</v-card-subtitle>
      <!-- <div class="text-center"> -->
      <h2 class="mx-auto pt-0 text-h4 font-weight-medium text-uppercase">WELCOME TO OUR WEBSITE</h2>

      <!-- </div> -->
      <v-card-subtitle>Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi veritatis ullam veniam nesciunt officiis culpa saepe. Aliquam modi facere fuga blanditiis quisquam? Nihil tempore ipsam fugiat eius quae repellat sit earum doloremque, nobis fugit ut saepe, officia veniam accusantium cupiditate molestiae? Ex sint cum praesentium vel tempora repellendus commodi delectus? Vel itaque eum aliquid explicabo nulla odio. Placeat vitae praesentium ex eveniet tenetur suscipit? Et, quam excepturi deserunt modi veritatis quo eaque ratione ex eum neque nesciunt sit, quos consectetur tenetur commodi maiores beatae non molestias illo fuga libero debitis laborum rerum. Inventore nulla iusto voluptas necessitatibus ut optio assumenda.</v-card-subtitle>

    </v-card-text>
    </v-container>

    <v-card-text class="text-center ">
    <h2 class=" pt-0 text-h4 font-weight-medium text-uppercase">WHAT WE OFFER</h2>

    </v-card-text>
    <v-card color="mx-auto" width="80%" class="mt-6">
        <v-row>
            <v-col cols="3" v-for="item of items" :key="item.title" class="px-0">
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

    <v-card-text class="text-center pt-10">
      <h2 class="text-h4 font-weight-medium text-uppercase">Our brands partner</h2>

    </v-card-text>
    <v-card color="mx-auto" width="80%" class="mt-6">
        <v-row>
            <v-col cols="3" v-for="item of brands" :key="item.title" class="px-0">
                <v-card-text class="text-center ">
                    <v-img :src="item.image" ></v-img>


                </v-card-text>
            </v-col>
        </v-row>
    </v-card>
  </section>
</template>

<script>
export default {
  data(){
    return{
      items:[
                {
                    title: "Free Shipping",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-truck-outline'
                },
                {
                    title: "Free Return",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-switch'
                },
                {
                    title: "24/7 Support",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-headset'
                },
                {
                    title: "Customers Discount",
                    subTitle: "Free shipping on all order",
                    icon: 'mdi-gift-outline'
                },
            ],
            brands:[
                {
                    image: "https://logos-world.net/wp-content/uploads/2020/04/Nike-Logo.png",
                },
                {
                    image: "https://logos-world.net/wp-content/uploads/2020/04/Air-Jordan-Symbol.png",
                },
                {
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/Adidas_Logo.svg/2560px-Adidas_Logo.svg.png",
                },
                {
                    image: "https://logos-world.net/wp-content/uploads/2020/04/Puma-Logo.png",
                },
            ]
    }
  }
}
</script>

<style scoped>
  .main-about {
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
</style>