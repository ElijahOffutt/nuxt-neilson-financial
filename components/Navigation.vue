<template>
    <v-app-bar app fixed style="box-shadow: 0 5px 15px rgba(0,0,0,.2)" color="white" height="70px" light>
        <div style="width: 1180px; margin: 0 auto;">
            <v-row align-center>
                <v-col class="shrink">
                    <nuxt-link to="/">
                        <img height="27.5px" src="https://www.neilsonfs.com/media/aqzdjho2/neilson-fs.png" />
                    </nuxt-link>
                </v-col>
                <v-spacer />
                <v-col class="shrink" style="white-space: nowrap !important;">
                    <template v-for="(link, i) in links">
                        <v-hover v-model="link.hover" :key="i">
                            <v-btn @click="$router.push('/'+link.link)" :color="link.hover && blue" text nuxt-link >
                                <span style="font-weight: 400;">{{link.text}}</span>
                            </v-btn>
                        </v-hover>
                    </template>
                </v-col>
            </v-row>
        </div>
    </v-app-bar>
</template>

<script>

export default {
    data(){
        return{
            blue: require('../assets/colors.json').secondary,
            links: [
                { text: 'about us', link: 'AboutUs', hover: false },
                { text: 'our team', link: 'OurTeam', hover: false },
                { text: 'partners', link: 'Partners', hover: false },
                { text: 'our brands', link: 'OurBrands', hover: false },
                { text: 'our locations', link: 'OurLocations', hover: false },
                { text: 'join us', link: 'JoinUse', hover: false },
                { text: 'news & press', link: 'NewsAndPress', hover: false },
            ]
        }
    }
}
</script>