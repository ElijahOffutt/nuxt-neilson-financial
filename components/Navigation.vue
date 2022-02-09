<template>
    <v-app-bar app fixed style="box-shadow: 0 5px 15px rgba(0,0,0,.2)" color="white" height="70px" light>
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
                        <v-btn :color="link.hover && blue" text nuxt-link >
                            <span style="font-weight: 400;">{{link.text}}</span>
                        </v-btn>
                    </v-hover>
                </template>
            </v-col>
        </v-row>
    </v-app-bar>
</template>

<script>

export default {
    data(){
        return{
            blue: require('../assets/colors.json').secondary,
            links: [
                { text: 'about us', link: '', hover: false },
                { text: 'our team', link: '', hover: false },
                { text: 'partners', link: '', hover: false },
                { text: 'our brands', link: '', hover: false },
                { text: 'our locations', link: '', hover: false },
                { text: 'join us', link: '', hover: false },
                { text: 'news & press', link: '', hover: false },
            ]
        }
    }
}
</script>