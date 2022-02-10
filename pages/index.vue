<template>
  <div class="content">
    <v-carousel cycle hide-delimiters :show-arrows="false">
      <v-carousel-item transition="fade-transition" height="auto" v-for="(slide, i) in slides" :key="i">
        <div class="background" :style="`background-image: url('${slide.image}')`">
          <div class="content">
            <p></p>
          </div>
        </div>
      </v-carousel-item>
    </v-carousel>
    <v-container class="py-10">
      <v-row style="width: 1180px; margin: 0 auto;">
        <v-col cols="6" class="pr-10">
          <p style="font-size: 1.25em;">Neilson Financial Services is a global specialist provider of life insurance. In the UK and Canada, Neilson provides insurance products directly to consumers via our retail brands, as well as through advised and partnership channels.</p>
          <br />
          <p style="font-size: 1.25em;">Our ambition is to protect and help as many people as possible by making products available however they want to buy them - whether online or offline, with guided or full advice or in conjunction with our corporate partners.</p>
          <v-row justify="center" class="rounded-lg py-6 mt-7" :style="`background-color: ${secondary}`">
            <v-col class="shrink" style="white-space: nowrap;">
              <p style="color: white; font-size: 1.5em;">To find out more contact us at</p>
              <a class="mb-5" style="width: 100%; display: inline-block; color: white; text-align: center; font-size: 1.5em;" href="mailto:enquiries@neilsonfs.com"><b>enquiries@neilsonfs.com</b></a> <br>
              <v-btn block dark x-large :color="primary">Contact Us</v-btn>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-5">
            <img width="100%" src="https://www.neilsonfs.com/media/lpqhuv2x/home-protect-future.jpg" />
            <v-card-title :style="`color: ${primary}`">
              We've put the building <br /> blocks in place 
            </v-card-title>
            <v-card-content>
              <p class="px-5">We’ve invested in building a wide range of capabilities in-house to give us maximum flexibility and control over how we design, develop, and deliver protection products for our customers and those of our partners.</p>
              <v-btn class="ml-5 mb-8" dark :color="accent">our capabilities</v-btn>
            </v-card-content>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
let color = require('../assets/colors.json');
let base = require('../assets/urls.json').base;
export default {
  name: 'IndexPage',
  data(){return{
    secondary: color.secondary,
    primary: color.primary,
    accent: require('../assets/colors.json').accent,
    slides: [
      {
        image: base+'/media/cmkdaa5d/home-page-1600x515.jpg'
      },
      {
        image: base+'/media/vftid1k5/banner-bg-home-2-1600.jpg'
      }
    ]
  }}
}
</script>

<style lang="scss">
.background{
  background-position: center;
  background-size: cover;
  height: 100%;
  width: 100vw;
  .content{
    margin: 0 auto;
  }
}
</style>