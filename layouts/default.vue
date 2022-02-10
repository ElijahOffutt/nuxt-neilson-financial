<template>
  <v-app dark>
    <Navigation />
    <MobileMenu />
    <v-main>
      <Nuxt />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  mounted(){
    this.$nuxt.$baseURL = 'https://www.neilsonfs.com'
  }
}
</script>
