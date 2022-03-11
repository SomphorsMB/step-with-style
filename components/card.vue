<template>
  <section>
    <v-hover v-slot="{ hover }" >
      <v-img
              src="https://i.pinimg.com/originals/72/94/f9/7294f9cd2a5c891ac822acfd9153dc7e.jpg"
              class="white--text align-end"
              height="300px"
            >
 <!-- <v-overlay
                v-if="hover"
                absolute
                

            >  -->
                <!-- <v-icon class="font-weight-black">mdi-eye</v-icon> -->
            <!-- </v-overlay>   -->
            <div v-if="hover" class="mb-4 d-flex justify-center">
                <v-icon class="px-1 text-h4">mdi-heart-outline</v-icon>
              <v-icon class="px-1 text-h4" @click.stop="dialog = true">mdi-eye-outline</v-icon>   
              <v-icon class="px-1 text-h4">mdi-cart-outline</v-icon>  
            </div>     
     </v-img>
    </v-hover>
        <v-card-title class="pb-0 text-center">
            <p class="mx-auto mb-0">Nike AIR force 1</p>
        </v-card-title>
        <v-card-title class="pt-0">
            <p class="mx-auto">120 $</p>
        </v-card-title>
    <detail-dialog v-if="dialog" />
  </section>
</template>

<script>
export default {
  data(){
    return{
      dialog: false
    }
  }
}
</script>

<style>

</style>