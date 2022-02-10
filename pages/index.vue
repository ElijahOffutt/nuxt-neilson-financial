<template>
  <div class="content">
    <Marquee />
    <v-container class="py-10">
      <v-row>
        <v-col cols="6">
          <p>Neilson Financial Services is a global specialist provider of life insurance. In the UK and Canada, Neilson provides insurance products directly to consumers via our retail brands, as well as through advised and partnership channels.</p>
          <p>Our ambition is to protect and help as many people as possible by making products available however they want to buy them - whether online or offline, with guided or full advice or in conjunction with our corporate partners.</p>
          <v-row>
            <v-col>
              <p>To find out more contact us at </p>
              <a href="mailto:enquiries@neilsonfs.com"><b>enquiries@neilsonfs.com</b></a>
              <v-btn>Contact Us</v-btn>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="6">
          <v-card class="elevation-5">
            <img src="https://www.neilsonfs.com/media/lpqhuv2x/home-protect-future.jpg" />
            <v-card-title>
              We've put the building <br /> blocks in place 
            </v-card-title>
            <v-card-content>
              <p>We’ve invested in building a wide range of capabilities in-house to give us maximum flexibility and control over how we design, develop, and deliver protection products for our customers and those of our partners.</p>
            </v-card-content>
            <v-card-actions>
              <v-btn :color="accent">our capabilities</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){return{
    accent: require('../assets/colors.json').accent
  }}
}
</script>
