<template>
  <section>
      <div class="main-contact text-center">
      <h1 class="title white--text text-wrap pt-16">
        Contact Us
      </h1>
    </div>
    <v-container class="mx-auto mt-4">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3909.013908283856!2d104.8808949142562!3d11.550859791798853!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x310951add5e2cd81%3A0x171e0b69c7c6f7ba!2sPasserelles%20Num%C3%A9riques%20Cambodia%20(PNC)!5e0!3m2!1sen!2skh!4v1583125279177!5m2!1sen!2skh" width="100%" frameborder="0"></iframe>
      <v-row class="mt-4">
        <v-col cols="4">
          <v-card class="infor-card">
            <v-card-text class="text-center ">
                    <v-icon class="teal--text text-h4" >mdi-map-marker-outline</v-icon>
                    <v-card-title class="text-center">
                        <span class="mx-auto"> BP 511, Phum Tropeang Chhuk (Borey Sorla) Sangtak, Street 371, Phnom Penh </span>
                    </v-card-title>
                    <v-card-subtitle>Santa monica bullevard</v-card-subtitle>
                </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card class="infor-card">
            <v-card-text class="text-center ">
                    <v-icon class="teal--text text-h4" >mdi-phone-outline</v-icon>
                    <v-card-title class="text-center">
                        <span class="mx-auto"> +855 (097) 49 11 250 </span>
                        <span class="mx-auto"> +855 (097) 49 11 250 </span>
                    </v-card-title>
                    <v-card-subtitle>Mon to Fri 9am to 6 pm</v-card-subtitle>
                </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card class="infor-card">
            <v-card-text class="text-center ">
                    <v-icon class="teal--text text-h4" >mdi-email-outline</v-icon>
                    <v-card-title class="text-center">
                        <span class="mx-auto">somphors@mango-byte.com</span>
                        <span class="mx-auto">somphors@mango-byte.com</span>
                    </v-card-title>
                    <v-card-subtitle>end us your query anytime!</v-card-subtitle>
                </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-card-text class="d-flex justify-center">
        <v-card-title class="mx-auto teal--text">Let's Talk</v-card-title>
      </v-card-text>
      <v-row>
        <v-col cols="6">
          <v-text-field
            label="Enter Your Name"
            outlined
          ></v-text-field>
          <v-text-field
            label="Enter Email Address"
            outlined
          ></v-text-field>
          <v-text-field
            label="Enter Subject"
            outlined
          ></v-text-field>
        </v-col>
        <v-col cols="6">
<v-textarea
          outlined
          name="input-7-10"
          rows="8"
          label="Enter Message"
        ></v-textarea>
        <v-card-text class="pa-0 d-flex justify-end">
          <!-- <v-btn class="teal darken-1 pt-4 pb-4">Send Message</v-btn> -->
          <v-btn class=" px-6 font-weight-bold py-6 white--text teal darken-1">Send Message</v-btn>

        </v-card-text>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>
.main-contact {
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
iframe{
    height: 400px;
    border-radius: 5px;
    
}
.infor-card{
  height: 13rem;
}
.message-btn{
  background: teal;
}
</style>