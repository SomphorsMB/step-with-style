<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
    
      <!-- <v-tab v-for="item of items" :key="item.to" :to="item.to" class="menu">{{ item.title }}</v-tab> -->
      <v-tabs
      background-color="transparent"
      color="teal"
    
    >
      <v-tab to="/home">Home</v-tab>
      <v-tab to="/shopping">Shop</v-tab>
      <!-- <v-tab to="/women">Women</v-tab>
      <v-tab to="/men">Men</v-tab> -->
      <v-tab to="/blog">About Us</v-tab>
      <v-tab to="/contact">Contact Us</v-tab>
    </v-tabs>

      <v-spacer />
      <v-tab to="/auth/login" class=" mx-2 px-0">
        <v-icon class="mr-1">mdi-account-circle-outline</v-icon>
        Log In
      </v-tab>
      <v-tab to="/auth/register" class=" mx-2">Register</v-tab>
      
    </v-app-bar>
    <v-main>
      <!-- <v-container> -->
        <Nuxt />
      <!-- </v-container> -->
    </v-main>
    

    <v-footer
      class="mt-16 footer"
    >
      <v-row>
        <v-col cols="4" class="text-center">
          <img src="https://www.designfreelogoonline.com/wp-content/uploads/2021/05/00379-shoes-02.png" width="50%" alt="">
          <v-card-text class="white--text"> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore dolore magna aliqua.</v-card-text>
        </v-col>
        <v-col cols="3">
          <h3 >Menus</h3>
          <v-list-item class="pl-0">
            <v-list-item-content class="pl-0">
              <v-list-item-title class="list">Home</v-list-item-title>
              <v-list-item-title class="list">Shop </v-list-item-title>
              <!-- <v-list-item-title class="list">Women</v-list-item-title>
              <v-list-item-title class="list">Men</v-list-item-title> -->
              <v-list-item-title class="list">About Us</v-list-item-title>
              <v-list-item-title class="list">Contact Us</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col cols="5">
          <h3 >Contact</h3>
          <v-list-item class="pl-0">
            <v-list-item-content class="pl-0">
              <v-list-item-title class="list">
                <v-icon class="pr-2">mdi-home-outline</v-icon>
                Phnom Penh, Cambodia
              </v-list-item-title>
              <v-list-item-title class="list">
                <v-icon class="pr-2">mdi-phone-outline</v-icon>
                +855 (097) 49 11 250
              </v-list-item-title>
              <v-list-item-title class="list">
                <v-icon class="pr-2">mdi-email-outline</v-icon>
                somphors@mango-byte.com
              </v-list-item-title>
              <v-spacer></v-spacer>  
                   
            </v-list-item-content>
          </v-list-item>
          <v-row class="mt-16">
            <v-col cols="2"><v-icon class="white--text">mdi-facebook</v-icon></v-col>
            <v-col cols="2"><v-icon class="white--text">mdi-chat-outline</v-icon></v-col>
            <v-col cols="2"><v-icon class="white--text">mdi-instagram</v-icon></v-col>
            <v-col cols="2"><v-icon class="white--text">mdi-twitter</v-icon></v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/home'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Shop',
          to: '/shopping'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'Women',
          to: '/women'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'Men',
          to: '/men'
        },
         {
          icon: 'mdi-chart-bubble',
          title: 'Blog',
          to: '/blog'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Contact',
          to: '/contact'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style scoped>
  .menu{
    cursor: pointer;
  }
  .menu:hover{
    text-decoration: underline;

  }
  .list{
    margin-bottom: 5px;
  }
  .list:hover{
    text-decoration: underline;
    cursor: pointer;
  }
  .footer{
    background: teal;
  }
</style>